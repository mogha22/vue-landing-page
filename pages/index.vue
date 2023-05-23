<template>
    <div class="main-wrapper">
        <IndexHeroSection />
        <IndexAboutSection />
        <IndexTestimonials />
        <IndexPackages />
        <IndexTests />
    </div>
</template>

<script>
    export default {
        name: 'IndexPage',
        setup(){
            useServerSeoMeta({
                title: 'Dr. Jane Doe\'s Clinic Get your Aviation Class II Medical',
                ogTitle: 'Dr. Jane Doe\'s Clinic Get your Aviation Class II Medical',
                description: 'Dr. Jane is a highly educated and experienced female doctor who is renowned for her exceptional medical expertise. She is a certified medical examiner by the Directorate General of Civil Aviation, providing Class 2 medical certifications to cabin crews in a seamless and hassle-free manner, providing reports within 24-48 hours',
                ogDescription: 'Dr. Jane is a highly educated and experienced female doctor who is renowned for her exceptional medical expertise. She is a certified medical examiner by the Directorate General of Civil Aviation, providing Class 2 medical certifications to cabin crews in a seamless and hassle-free manner, providing reports within 24-48 hours',
                ogImage: '/assets/images/home/hero/doc-image-1.jpg',
                twitterCard: 'summary_large_image',
            })
        }
    }
</script>