<script setup lang="ts">

import { ref } from "vue";

const prop = defineProps(['title'])
console.log(prop)

</script>

<template>
    <div class="menu">
        <i><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="16" height="16"><path fill="none" d="M0 0h24v24H0z"/><path d="M13.172 12l-4.95-4.95 1.414-1.414L16 12l-6.364 6.364-1.414-1.414z" fill="rgba(49,49,49,1)"/></svg></i>
        <i style="margin-right: 8px"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="16" height="16"><path fill="none" d="M0 0h24v24H0z"/><path d="M3 18.5V5a3 3 0 0 1 3-3h14a1 1 0 0 1 1 1v18a1 1 0 0 1-1 1H6.5A3.5 3.5 0 0 1 3 18.5zM19 20v-3H6.5a1.5 1.5 0 0 0 0 3H19zM5 15.337A3.486 3.486 0 0 1 6.5 15H19V4H6a1 1 0 0 0-1 1v10.337z" fill="rgba(225,225,225,1)"/></svg></i>
        <span>{{ title }}</span>
    </div>
</template>

<style scoped>

i {
    display: inline-block;
    vertical-align: middle;
    height: 16px;
}

span {
    vertical-align: middle;
    display: inline-block;
}

.menu {
    cursor: default;
    margin: 8px 0;
    -webkit-user-select: none; /*禁止选择*/
    color: rgb(196, 196, 196);
}


.arrow {

}
</style>