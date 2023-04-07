<template>
    <nav class="nav__container">
        <ul class="ul__nav flex flex-col">
            <li v-for="route in avelableRoutes" :key="route.to" :class="{'active-route': currentRoute === route.to}">
                <NuxtLink :to="route.to" class="">
                    {{ route.name }}
                </NuxtLink>
            </li>
        </ul>
    </nav>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';

export default defineComponent({
  name: 'navigationBarSimple',
  props: {
    currentRoute: {
      type: String as PropType<string>,
      required: true,
    },
    avelableRoutes: {
        type: Array as PropType<{name: string, to: string}[]>,
      required: true,
    },
  },
});
</script>

<style lang="scss" scoped>
    .ul__nav {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 50px;
        text-transform: uppercase;
        letter-spacing: 2px;
        font-weight: 700;
        list-style: none;
    }

    .ul__nav * {
        -webkit-box-sizing: border-box;
        box-sizing: border-box;
        -webkit-transition: all 0.35s ease;
        transition: all 0.35s ease;
    }

    .ul__nav a {
        position: relative;
        color: rgba(205, 207, 205, 0.5);
        padding: 0.5rem 0.8rem;
        text-decoration: none;
    }

    .ul__nav a:before,
    .ul__nav a:after {
        position: absolute;
        height: 15px;
        width: 15px;
        content: '';
        -webkit-transition: all 0.35s ease;
        transition: all 0.35s ease;
        opacity: 0;
    }

    .ul__nav a:before {
        right: 0;
        top: 0;
        border-right: 3px solid #b80000;
        border-top: 3px solid #b80000;
        -webkit-transform: translate(-60%, 30%);
        transform: translate(-60%, 30%);
    }

    .ul__nav a:after {
        left: 0;
        bottom: 0;
        border-left: 3px solid #b80000;
        border-bottom: 3px solid #b80000;
        -webkit-transform: translate(60%, -30%);
        transform: translate(60%, -30%);
    }

    .ul__nav a:hover,
    .ul__nav .active-route a {
        color: #ffffff;
    }

    .ul__nav a:hover:before,
    .ul__nav .active-route a:before,
    .ul__nav a:hover:after,
    .ul__nav .active-route a:after {
        -webkit-transform: translate(0%, 0%);
        transform: translate(0%, 0%);
        opacity: 1;
    }
</style>