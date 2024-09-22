<template>
    <div class="card">
        <div class="inner-card">
            <div class="card-face front">
                <slot name="front"></slot>
            </div>
            <div class="card-face back">
                <slot name="back"></slot>
            </div>
        </div>
    </div>

</template>
<style scoped>
.card {
    width: 200px;
    height: 300px;
    perspective: 1000px;
}

.inner-card {
    width: 100%;
    height: 100%;
    transition: transform 0.6s;
    transform-style: preserve-3d;
    position: relative;
}

.card:hover .inner-card {
    transform: rotateY(180deg);
}

.card-face {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.5rem;
    color: white;
}

.front {
    background-color: #00b3ff;
}

.back {
    background-color: #28a752;
    transform: rotateY(180deg);
}
</style>