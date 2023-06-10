<template>
    <div class="slide w-slider__slide">

        <div class="slide__flex">

            <div class="slide__main-heading-wrapper">
                <h1 class="slide__main-heading slide__main-heading_small">
                    {{ work.name }}
                </h1>

            </div>

            <div class="slide__slice-wrapper">
                <div class="img-container-1 img-container-1_work">
                    <div
                        class="abt-s1-img-slice-1_work s1-img-slice-1 abt-s1-img-slice-1"
                        :style="{ backgroundImage: 'url(' + require('@/assets/img/works-images/' + work.imageSmall) + ')' }"
                    >
                    </div>
                </div>

                <div class="img-container-2">
                    <div
                        class="s1-img-slice-2 abt-s1-img-slice-2 abt-s1-img-slice-2_work"
                        :style="{ backgroundImage: 'url(' + require('@/assets/img/works-images/' + work.imageSmall) + ')' }"
                    >
                    </div>
                </div>

                <div class="img-container-3 ">
                    <div
                        class="s1-img-slice-3 abt-s1-img-slice-3 abt-s1-img-slice-3_work"
                        :style="{ backgroundImage: 'url(' + require('@/assets/img/works-images/' + work.imageSmall) + ')' }"
                    >
                    </div>
                </div>
            </div>

            <div class="slide__text-wrapper">
                <div class="slide__details-wrapper _name-parent">
                    <h2 class="slide__about-text-heading">
                        Сайт
                    </h2>
                    <h3 class="details-bold slide__details-bold">
                        {{ work.desc }}
                    </h3>
                    <p class="details slide__details">
                        Lorem ipsum dolor sit amet, consectetur
                        adipiscing elit. Suspendisse varius enim in
                        eros elementum tristique. Duis cursus, mi
                        quis viverra ornare, eros dolor interdum
                        nulla, ut commodo libero vitae erat. Aenean
                        faucibus nibh et justo cursus id rutrum
                        lorem imperdiet Aliquam facilisis elementum
                        dui.
                    </p>

                    <h2 class="slide__about-text-heading">
                        Стэк:
                    </h2>

                    <div class="_name-text">
                        .work
                    </div>
                </div>

                <div
                    class="slide__services-flex"
                >

                    <div
                        class="slide__servies-block"
                        v-for="(value,index) in work.skills"
                        :key="index"
                        :class="{'slide__servies-block-one': (index == 0),
                            'slide__servies-block-two': (index == 1),
                            'slide__servies-block-three': (index == 2),
                        }"
                    >
                        {{ value }}
                    </div>
                </div>
                <div
                    class="slide__services-flex"
                >
                    <SliderFancyboxLink
                        :link="work.imageBig"
                    />
                </div>
            </div>
        </div>

    </div>
</template>

<script>
import SliderFancyboxLink from "../../components/slider/SliderFancyboxLink.vue";

export default {
    name: 'SlideItem',

    components: {
		SliderFancyboxLink
	},

    props: {
        work: {
            type: Object,
            required: true
        }
    },

    data() {
        return {

        }
    }
}

</script>

<style scoped>
.abt-s1-img-slice-1_work,
.abt-s1-img-slice-2_work,
.abt-s1-img-slice-3_work {
    background-image: none;
}

.abt-s1-img-slice-1_work {
    left: -50%;
}

.abt-s1-img-slice-2_work {
    left: -150%;
}
.abt-s1-img-slice-3_work {
    left: -250%;
}

.img-container-1_work {
    filter: unset;
}

@media (max-width : 768px) {
    .abt-s1-img-slice-1_work,
    .abt-s1-img-slice-2_work,
    .abt-s1-img-slice-3_work {
        filter: grayscale(100%)
            brightness(20%)
            hue-rotate(-50deg)
            contrast(0.8);
    }
}

</style>
