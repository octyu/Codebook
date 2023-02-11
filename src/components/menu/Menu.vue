<script setup lang="ts">

import { ref } from "vue";

const prop = defineProps(['id', 'title', 'icon'])


function onClick() {

}

</script>

<template>
    <div class="menu">
        <i><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="16" height="16"><path fill="none" d="M0 0h24v24H0z"/><path :d="icon" fill="rgba(221,221,221,1)"/></svg></i>
        <span>{{ title }}</span>
    </div>
</template>

<style scoped>

i {
    display: inline-block;
    vertical-align: middle;
    height: 16px;
    margin-left: 16px;
    margin-right: 8px;
}

span {
    vertical-align: middle;
    display: inline-block;
}

.menu {
    cursor: default;
    margin: 8px 0;
    padding: 8px 0;
    border-radius: 8px;
    -webkit-user-select: none; /*禁止选择*/
    color: rgb(169, 169, 169);
}

</style>