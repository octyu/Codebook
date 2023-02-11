<script setup lang="ts">

import { ref } from "vue";

const avatar = ref("https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png")
const nickname = ref("Octyu")

</script>

<template>
    <div>
        <span>
            <img :src="avatar" alt="avatar">{{ nickname }}
        </span>
    </div>
</template>

<style scoped>

img {
    vertical-align:middle;
    border-radius: 50%;
    width: 24px;
    height: 24px;
    margin-right: 8px;
    -webkit-user-select: none;
}
</style>