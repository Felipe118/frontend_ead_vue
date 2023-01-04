<template>
   <header id="header">
        <nav>
            <span class="toggleMenu far fa-bars"></span>
            <router-link :to="{name: 'campus.home'}" >
                <span class="logo">
                    <img :src="require('@/assets/images/logo.svg')" alt="EspecializaTi">
                </span>
            </router-link>
           
        </nav>
    </header>
</template>

<script>

export default {
    name: 'header-component',
}
</script>