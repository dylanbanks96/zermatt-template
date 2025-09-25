<template>
    <section>
        <h2 class="header2 text-center">Our Services</h2>
        <p class="muted text-center">We offer a range of services to help you achieve the results you're after.</p>
        <div class="services-alt">
            <div v-for="image in services2" :key="image.id" class="service-card-alt">
                <div class="service-card-inner">
                    <div class="service-text">
                        <h3 class="text-alt">{{ image.title }}</h3>
                        <p class="text-alt">{{ image.desc }}</p>
                    </div>
                    <img :src="image.icon" :alt="image.title" class="service-img" />
                </div>

            </div>

        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue'
import ai1 from '@/assets/ai1.jpg'
import ai2 from '@/assets/ai2.jpg'
import ai3 from '@/assets/ai3.jpg'

const services2 = ref([
    { id: 1, title: 'Personalized Ski Planning', desc: 'Plan your perfect day on the slopes with our AI-driven itinerary.', icon: ai1 },
    { id: 2, title: 'Skill Tracking & Improvement', desc: 'Track your progress and improve faster with AI analytics.', icon: ai2 },
    { id: 3, title: 'Community & Sharing', desc: 'Connect with fellow skiers, share your runs, and discover new adventures', icon: ai3 }
])
</script>