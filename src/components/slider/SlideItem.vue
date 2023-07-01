<template>
    <div class="slide w-slider__slide">

        <div class="slide__flex slide__flex_works">

            <div class="slide__main-heading-wrapper">
                <h1 class="slide__main-heading slide__main-heading_small">
                    {{ work.name }}
                </h1>

            </div>

            <div class="slide__slice-wrapper">
                <div class="img-container-1 img-container-1_width img-container-1_work">
                    <div
                        class="abt-s1-img-slice-1_work s1-img-slice-1 abt-s1-img-slice-1"
                        :style="{ backgroundImage: 'url(' + require('@/assets/img/works-images/' + work.imageSmall) + ')' }"
                    >
                    </div>
                </div>

                <div class="img-container-2 img-container-1_width">
                    <div
                        class="s1-img-slice-2 abt-s1-img-slice-2 abt-s1-img-slice-2_work"
                        :style="{ backgroundImage: 'url(' + require('@/assets/img/works-images/' + work.imageSmall) + ')' }"
                    >
                    </div>
                </div>

                <div class="img-container-3 img-container-1_width">
                    <div
                        class="s1-img-slice-3 abt-s1-img-slice-3 abt-s1-img-slice-3_work"
                        :style="{ backgroundImage: 'url(' + require('@/assets/img/works-images/' + work.imageSmall) + ')' }"
                    >
                    </div>
                </div>
            </div>

            <div class="slide__text-wrapper slide__text-wrapper_works">
                <div class="slide__details-wrapper _name-parent">
                    <h2 class="slide__about-text-heading">
                        Сайт
                    </h2>
                    <h3 class="details-bold slide__details-bold">
                        {{ work.desc }}
                    </h3>
                    <a 
                        :href="work.href" 
                        target="_blank"
                        class="details slide__link"
                    >
                        Ссылка - {{ work.link }}
                    </a>

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
    left: 0;
    background-position: center 0;
}

.abt-s1-img-slice-2_work {
    left: 50%;
    background-position: center 0;
    transform: translateX(-50%);
}
.abt-s1-img-slice-3_work {
    left: unset;
    right: 0;
    background-position: center 0;
}

.img-container-1_work {
    filter: unset;
}

.img-container-1_width {
    flex-basis: calc(100% / 3);
}
.img-container-1_width > div {
    width: 300%;
}

@media (max-width : 768px) {
    .abt-s1-img-slice-1_work,
    .abt-s1-img-slice-2_work,
    .abt-s1-img-slice-3_work {
        filter: grayscale(50%)
            brightness(40%)
            hue-rotate(-20deg)
            contrast(0.9);
    }
}

</style>
