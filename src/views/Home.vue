<template>
    <div class="home">
        <slider></slider>
    </div>
</template>

<script>
// @ is an alias to /src

export default {
    name: 'home',
    components: {
        slider: () => import('@/components/Slider.vue')
    }
};
</script>
