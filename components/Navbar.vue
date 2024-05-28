<template>
    <nav class="glassy-bg position-fixed">
        <div style="max-width: 1400px" class="d-flex justify-space-between align-center mx-auto">
            <div class="primary-gradient text-white px-4 rounded rotate3d">Unappli</div>
            <div class="d-flex" style="gap: 20px">
                <div>Accueil</div>
                <div>Services</div>
                <div>A propos</div>
                <div>Contact</div>
            </div>
        </div>
    </nav>
</template>

<script setup>

</script>

<style scoped lang="scss">
nav {
    height: 60px;
    width: 100%;
    z-index: 999;
    border-radius: 0;
    .rotate3d {
        animation: rotate3d 10s infinite;
    };
}

@keyframes rotate3d {
    0% {
        transform: rotateY(0deg);
    }
    90% {
        transform: rotateY(0deg);

    }
    100% {
        transform: rotateY(360deg);
    }
}
</style>