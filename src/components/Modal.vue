<template>
    <div class="backdrop">
        <div class="modal">
            <h1>Modal Title</h1>
            <p>modal content</p>
        </div>
    </div>
</template>
<style scoped>
.modal {
    width: 400px;
    padding: 20px;
    margin: 200px auto;
    background: #fff;
    border-radius: 10px;
}

.backdrop {
    inset: 0 auto auto auto;
    position: fixed;
    background: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
}
h1 {
    color: #03cfb4;
    border: none;
    padding: 0;
}
</style>