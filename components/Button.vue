<template>
    <div :data-button-type="type" :data-button-placement="placement" class="appointment-button">
        <NuxtLink to="/">
            <p class="appointment-button-text">
                <span class="material-symbols-outlined">calendar_month</span>
                <span>&nbsp;Book an appointment</span>
            </p>
        </NuxtLink>
    </div>
</template>

<script>
    export default {
        name: 'Button',
        props:{
            type: String,
            placement: String
        }
    }
</script>

<style lang="scss">
    .appointment-button{
        width: fit-content ;
        overflow: hidden;
        border-radius: 6px;
        align-self: center;
        transition: 0.25s all ease-in-out;

        &[data-button-type="dark"]{
            background-color: #1D5982;

            &:hover{
                background-color: #2A7FBA;
            }

            &:active{
                background-color: #5599C8;
            }

            .appointment-button-text{
                color: white ;
            }
        }

        &[data-button-type="light"]{
            background-color: #C8CBCE ;

            &:hover{
                background-color: #D4E5F1;
            }

            &:active{
                background-color: #AACCE3;
            }
            
            .appointment-button-text{
                color: #1D5982 ;
            }
        }

        &[data-button-placement="header"]{

            .appointment-button-text{
                font-size: 13px;
                padding: 10px 20px ;

                .material-symbols-outlined{
                    font-size: 16px;
                }
            }
        }
    }
    .appointment-button-text{
        font-size: 14px ;
        font-weight: 500 ;
        font-family: var(--font-family);
        padding: 12px 24px ;

        .material-symbols-outlined{
            font-size: 17px;
            transform: translateY(-1px);
        }

        span{
            display: inline-block ;
            vertical-align: middle;
        }
    }
</style>