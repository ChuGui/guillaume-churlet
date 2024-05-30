<template>
    <section class="position-relative">
        <div class="container pa-16">
            <h3 style="font-size: 72px" class="text-center">Personnalisation et Innovation</h3>
            <h2 class="text-center">Des solutions sur mesure, propulsées par l'IA</h2>
            <p class="text-center mt-8">Nous comprenons que chaque entreprise a des besoins uniques. C'est pourquoi nos outils nocode et IA permettent une personnalisation poussée de vos applications. En utilisant l'intelligence artificielle, nous vous aidons à intégrer des fonctionnalités avancées telles que l'analyse prédictive, la reconnaissance vocale ou l'automatisation des tâches, pour que votre application soit non seulement adaptée à vos besoins, mais aussi à la pointe de l'innovation technologique.</p>
        </div>
    </section>

</template>

<style scoped lang="scss">
section {
    min-height: 100vh;

    .wave {
        filter: blur(4px);
        animation: rotateY 120s infinite;
    }

    @keyframes rotateY {
        0% {
            transform: rotateZ(0);
        }
        100% {
            transform: rotateZ(360deg);
        }
    }
}
</style>

<script setup lang="ts">
</script>