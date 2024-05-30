<template>
    <section class="d-flex align-center">
        <div class="container pa-16 d-flex justify-center align-center flex-column" style="gap: 30px">
            <h3 style="font-size: 72px" class="text-center">Accessibilité et Simplicité</h3>
            <h2 class="text-center">Des outils puissants, accessibles à tous</h2>
            <p class="text-center mt-8">Nos services sont conçus pour être utilisés par tous, même sans compétences en programmation. Grâce à des interfaces intuitives et des outils drag-and-drop, vous pouvez facilement concevoir des applications professionnelles et fonctionnelles. Vous n'avez plus besoin de dépendre de développeurs coûteux ou de consacrer du temps à apprendre à coder. Avec nous, tout le monde peut devenir créateur d'applications.</p>
        </div>
    </section>

</template>

<style scoped lang="scss">
section {
    min-height: 100vh;

    .wave {
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