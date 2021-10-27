<template>
    <dialogue open>
        <slot></slot>
    </dialogue>
</template>

<style scoped>
dialogue {
    position: fixed;
    top: 20vh;
    left: 30%;
    width: 40%;
    background-color: bisque;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
    padding:1rem;
}
</style>