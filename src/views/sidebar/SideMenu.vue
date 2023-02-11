<script setup lang="ts">
import Menu from "../../components/menu/Menu.vue";
import MenuList from "../../components/menu/MenuList.vue";
import { ref } from "vue";

const activeMenuId = ref("")
const menus = {
    problem: {id: "Problem", title: "Problem", icon: "M3 18.5V5a3 3 0 0 1 3-3h14a1 1 0 0 1 1 1v18a1 1 0 0 1-1 1H6.5A3.5 3.5 0 0 1 3 18.5zM19 20v-3H6.5a1.5 1.5 0 0 0 0 3H19zM5 15.337A3.486 3.486 0 0 1 6.5 15H19V4H6a1 1 0 0 0-1 1v10.337z"},
    test: {id: "Test", title: "Test", icon: "M3 18.5V5a3 3 0 0 1 3-3h14a1 1 0 0 1 1 1v18a1 1 0 0 1-1 1H6.5A3.5 3.5 0 0 1 3 18.5zM19 20v-3H6.5a1.5 1.5 0 0 0 0 3H19zM5 15.337A3.486 3.486 0 0 1 6.5 15H19V4H6a1 1 0 0 0-1 1v10.337z"}
}

function onSelectMenu(menuId: string) {
    activeMenuId.value = menuId
}
</script>

<template>

    <div>
        <h5>Dashboard</h5>
        <Menu v-for="menu in menus" :class="{'active': activeMenuId === menu.id}"
              @click="onSelectMenu(menu.id)" :title="menu.title" :icon="menu.icon"/>
    </div>

</template>

<style scoped>

.active {
    background-color: rgb(53, 53, 53);
}

</style>