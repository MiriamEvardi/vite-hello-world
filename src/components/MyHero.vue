<script>
export default {
    name: 'MyHero',
}
</script>

<template>
    <section class="hero">
        <div class="content">
        </div>
        <div class="waves"></div>
    </section>
</template>

<style>
:root {
    --color: #ab76fe;
}

body {
    margin: 0;
    padding: 0;
}

.content {
    max-width: 600px;
    margin: 0 auto;
    padding: 0 20px;
}

.hero {
    position: relative;
    background: #960ef0;
    color: white;
    height: 100vh;
    display: flex;
    align-items: center;
    overflow: hidden;
}

.waves {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 300px;
    background-color: var(--color);
    box-shadow: inset 0 0 50px rgba(0, 0, 0, 0.5);
    transition: 500ms;
}

.waves::before,
.waves::after {
    content: '';
    position: absolute;
    width: 300vw;
    height: 300vw;
    top: -65vw;
    left: 50%;
    transform: translate(-50%, -75%);
}

.waves::before {
    border-radius: 44%;
    background: rgba(51, 51, 51, 1);
    animation: waves 8s linear infinite;
}

.waves::after {
    border-radius: 44%;
    background: rgba(51, 51, 51, 0.5);
    animation: waves 15s linear infinite;
}

@keyframes waves {
    0% {
        transform: translate(-50%, -75%) rotate(0deg);
    }

    100% {
        transform: translate(-50%, -75%) rotate(360deg);
    }
}
</style>