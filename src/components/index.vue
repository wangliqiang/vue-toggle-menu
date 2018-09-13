<template>
    <div class="toggle_menu_container">
        <toggle-menu position="LT" menuBg="white" itemBg="white" :menuItems="menuItems" @clickMenu="clickMenu" baseDistance="150"></toggle-menu>
    </div>
</template>

<script>
import toggleMenu from './toggleMenu'
export default {
    name: 'index',
    data() {
        return {
            menuItems: [
                { name: 'emoji', src: require('../assets/emoji.png') },
                { name: 'cart', src: require('../assets/cart.png') },
                { name: 'folder', src: require('../assets/folder.png') },
                { name: 'home', src: require('../assets/home.png') },
                { name: 'my', src: require('../assets/my.png') },
            ]
        }
    },
    methods: {
        clickMenu(item, index) {
            console.log(item, index);
        }
    },
    components: {
        toggleMenu
    }
}
</script>

<style scoped>
</style>
