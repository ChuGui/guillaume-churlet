<template>
    <section class="container d-flex justify-center align-center w-100">
        <v-row class="position-relative">
            <v-col cols="7" class="d-flex flex-column justify-center">
                <h1 class="main-title">Bienvenue chez <span class="primary-gradient text-white px-2 rounded d-inline-block slide-from-top" style="transform: rotate(-5deg)">Unappli</span> <br> Votre développeur web rapide et abordable</h1>
                <h3>Nous créons des sites web de qualité, rapidement et à un prix compétitif. <br> Contactez-nous dès maintenant pour discuter de votre projet.</h3>
                <div class="d-flex w-100 mt-8" style="gap: 24px">
                    <v-btn color="primary" variant="elevated" rounded="xl">En savoir plus</v-btn>
                    <v-btn color="secondary" variant="elevated" rounded="xl">Nous contacter</v-btn>
                </div>
            </v-col>
            <v-col cols="5" class="d-flex align-center justify-center">
                <v-img
                    width="100%"
                    max-width="550"
                    aspect-ratio="16/9"
                    src="/Web.webp"
                ></v-img>
            </v-col>
        </v-row>
    </section>
    <div class="gradient-bg">
        <svg xmlns="http://www.w3.org/2000/svg">
            <defs>
                <filter id="goo">
                    <feGaussianBlur in="SourceGraphic" stdDeviation="10" result="blur"/>
                    <feColorMatrix in="blur" mode="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 18 -8" result="goo"/>
                    <feBlend in="SourceGraphic" in2="goo"/>
                </filter>
            </defs>
        </svg>
        <div class="gradients-container">
            <div class="g1"></div>
            <div class="g2"></div>
            <div class="g3"></div>
            <div class="g4"></div>
            <div class="g5"></div>
            <div class="interactive" ref="interactive"></div>
        </div>
    </div>

</template>

<script lang="ts" setup>
import {ref, onMounted} from 'vue';

// les animations background
const interactive = ref<HTMLElement | null>(null)

onMounted(() => {
    let curX = 0;
    let curY = 0;
    let tgX = 0;
    let tgY = 0;

    const move = () => {
        curX += (tgX - curX) / 20;
        curY += (tgY - curY) / 20;
        if (interactive.value) {
            interactive.value.style.transform = `translate(${Math.round(curX)}px, ${Math.round(curY)}px)`;
        }
        requestAnimationFrame(() => {
            move()
        })
    }

    window.addEventListener('mousemove', (event) => {
        tgX = event.clientX;
        tgY = event.clientY;
    })

    move()
})


</script>

<style scoped lang="scss">

// Background animation
@keyframes moveInCircle {
    0% {
        transform: rotate(0deg);
    }
    50% {
        transform: rotate(180deg);
    }
    100% {
        transform: rotate(360deg);
    }
}

@keyframes moveVertical {
    0% {
        transform: translateY(-50%);
    }
    50% {
        transform: translateY(50%);
    }
    100% {
        transform: translateY(-50%);
    }
}

@keyframes moveHorizontal {
    0% {
        transform: translateX(-50%) translateY(-10%);
    }
    50% {
        transform: translateX(50%) translateY(10%);
    }
    100% {
        transform: translateX(-50%) translateY(-10%);
    }
}

section {
    z-index: 100;
    height: 100vh;
    width: 100vh;

    .main-title {
        font-size: 48px;
    }
}

.gradient-bg {
    width: 100vw;
    height: 100vh;
    position: absolute;
    overflow: hidden;
    top: 0;
    left: 0;
    background: white;

    svg {
        display: none;
    }

    .gradients-container {
        filter: url(#goo) blur(40px);
        width: 100%;
        height: 100%;
    }

    .g1 {
        position: absolute;
        background: radial-gradient(circle at center, rgba(var(--color1), 0.8) 0, rgba(var(--color1), 0) 50%) no-repeat;
        mix-blend-mode: var(--blending);

        width: var(--circle-size);
        height: var(--circle-size);
        top: calc(50% - var(--circle-size) / 2);
        left: calc(50% - var(--circle-size) / 2);

        transform-origin: center center;
        animation: moveVertical 30s ease infinite;

        opacity: 1;
    }

    .g2 {
        position: absolute;
        background: radial-gradient(circle at center, rgba(var(--color2), 0.8) 0, rgba(var(--color2), 0) 50%) no-repeat;
        mix-blend-mode: var(--blending);

        width: var(--circle-size);
        height: var(--circle-size);
        top: calc(50% - var(--circle-size) / 2);
        left: calc(50% - var(--circle-size) / 2);

        transform-origin: calc(50% - 400px);
        animation: moveInCircle 20s reverse infinite;

        opacity: 1;
    }

    .g3 {
        position: absolute;
        background: radial-gradient(circle at center, rgba(var(--color3), 0.8) 0, rgba(var(--color3), 0) 50%) no-repeat;
        mix-blend-mode: var(--blending);

        width: var(--circle-size);
        height: var(--circle-size);
        top: calc(50% - var(--circle-size) / 2 + 200px);
        left: calc(50% - var(--circle-size) / 2 - 500px);

        transform-origin: calc(50% - 400px);
        animation: moveInCircle 40s linear infinite;

        opacity: 1;
    }

    .g4 {
        position: absolute;
        background: radial-gradient(circle at center, rgba(var(--color4), 0.8) 0, rgba(var(--color4), 0) 50%) no-repeat;
        mix-blend-mode: var(--blending);

        width: var(--circle-size);
        height: var(--circle-size);
        top: calc(50% - var(--circle-size) / 2);
        left: calc(50% - var(--circle-size) / 2);

        transform-origin: calc(50% - 200px);
        animation: moveHorizontal 40s ease infinite;

        opacity: 0.7;
    }

    .g5 {
        position: absolute;
        background: radial-gradient(circle at center, rgba(var(--color5), 0.8) 0, rgba(var(--color5), 0) 50%) no-repeat;
        mix-blend-mode: var(--blending);

        width: var(--circle-size);
        height: var(--circle-size);
        top: calc(50% - var(--circle-size));
        left: calc(50% - var(--circle-size));

        transform-origin: calc(50% - 200px);
        animation: moveInCircle 20s ease infinite;

        opacity: 1;
    }

    .interactive {
        position: absolute;
        background: radial-gradient(circle at center, rgba(var(--color-interactive), 0.8) 0, rgba(var(--color-interactive), 0) 50%) no-repeat;
        mix-blend-mode: var(--blending);

        width: 100%;
        height: 100%;

        top: -50%;
        left: -50%;

        opacity: 0.7;
    }
}
</style>