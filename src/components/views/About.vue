<template>
    <div>
        <p>
            Hi! I’m Joe, the face (and camera!) behind Not Your Average Joe Photos.
        </p>
        <div class="grid">
            <img src="../../assets/photos/joe.jpg" />
        </div>
    </div>
</template>

<script setup>
import { onMounted, onUnmounted } from 'vue';

let x = new Audio(require('../../assets/dial-up-modem-01.mp3'));

onMounted(() => {
    x.play();
});

onUnmounted(() => {
    x.pause();
    x.currentTime = 0;
});
</script>

<style scoped>
.p {
    margin: 0;
    padding: 0;
}

.grid {
    column-count: 2;
    column-gap: 0.5em;
    margin-top: auto;
    margin-bottom: auto;
    padding: 20px;
}

img {
    background-color: #eee;
    display: inline-block;
    margin: 0 0 0.5em;
    width: 100%;
}

@media screen and (max-width: 600px) {
    .grid {
        column-count: 1;
    }
}
</style>

