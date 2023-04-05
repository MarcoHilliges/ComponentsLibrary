<template>
    <nav class="nav__container">
        <ul class="ul__nav">
            <li class="home">
                <NuxtLink to="/" class="">
                    Home
                </NuxtLink>
            </li>
            <li>
                <NuxtLink to="/components" class="">
                    Components
                </NuxtLink>
            </li>
            <li>
                <NuxtLink to="/nuxtOriginal" class="">
                    Nuxt Original
                </NuxtLink>
            </li>
            <li>
                <NuxtLink to="/nuxtOriginal" class="">
                    Nuxt Original
                </NuxtLink>
            </li>
        </ul>
    </nav>
</template>

<script>

</script>

<style lang="scss" scoped>
    .ul__nav {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 50px;
        text-transform: uppercase;
        letter-spacing: 2px;
    }
</style>