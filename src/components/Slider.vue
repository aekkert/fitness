<template>
    <div id="slider">
        <carousel-3d>
            <template v-for="(item, index) in items">
                <slide :index="index" :key="index">
                    {{item.title}}
                </slide>
            </template>
        </carousel-3d>
   </div>
</template>

<script>
import {Carousel3d, Slide} from 'vue-carousel-3d';

export default {
    name: 'slider',
    components: {
        Carousel3d,
        Slide
    },
    data() {
        return {
            items: [
                { title: 'Услуги' },
                { title: 'Наши тренеры' },
                { title: 'Тренажеры' },
                { title: 'Расписание' },
                { title: 'Акции' },
                { title: 'О компании' },
                { title: 'Контакты' }
            ]
        }
    }
}
</script>
