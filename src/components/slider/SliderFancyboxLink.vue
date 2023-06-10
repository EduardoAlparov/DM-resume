<template>
    <div ref="container">
        <a
            class="expand-button"
            data-fancybox="gallery"
            :href="require('@/assets/img/works-images/' + link)"
        >
            <svg x="0px" y="0px" viewBox="0 0 54 54" style="enable-background:new 0 0 54 54;" xml:space="preserve">
                <g>
                    <path d="M0,0v54h54V0H0z M52,52H2V2h50V52z"/>
                    <path d="M20.143,49v-2H8.414l15.293-15.293c0.391-0.391,0.391-1.023,0-1.414s-1.023-0.391-1.414,0L7,45.586V33.857H5V49H20.143z"/>
                    <path d="M31,24c0.256,0,0.512-0.098,0.707-0.293L47,8.414v11.729h2V5H33.857v2h11.729L30.293,22.293
                        c-0.391,0.391-0.391,1.023,0,1.414C30.488,23.902,30.744,24,31,24z"/>
                </g>
            </svg>

            Посмотреть макет полностью
        </a>
    </div>
</template>

<script>
import { Fancybox } from '@fancyapps/ui';
import '@fancyapps/ui/dist/fancybox/fancybox.css';


export default {
    name: 'SliderFancyboxLink',

    props: {
        link: {
            type: String,
            default: ""
        }
    },

    data() {
        return {
            options: {
                type: Object,

            }
        }
    },

   mounted() {
        Fancybox.bind(this.$refs.container, '[data-fancybox]', {
            ...(this.options || {}),
        });
    },

    updated() {
        Fancybox.unbind(this.$refs.container);
        Fancybox.close();

        Fancybox.bind(this.$refs.container, '[data-fancybox]', {
        ...(this.options || {}),
        });
    },

    unmounted() {
        Fancybox.destroy();
    },
}

</script>

<style scoped>

.expand-button {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 30px 0;

    background-color: transparent;
    border: none;
    outline: none;
    cursor: pointer;

    font-family: 'Ubuntu Condensed', sans-serif;
    font-size: 14px;
    line-height: 22px;
    color: var(--accent);

    transition: 200ms;
}

.expand-button svg {
    height: 30px;
    width: 30px;

    fill: var(--accent);
    transition: transform 200ms;
}

@media (any-hover: hover) {
    .expand-button:hover {
        color: #FEFEFE;
    }

    .expand-button:hover svg {
        transform: scale(1.2);
        fill: #FEFEFE;
    }
}

@media (hover: none) {
  /* behaviour for touch browsers */
      .expand-button {
        color: #FEFEFE;
    }

    .expand-button svg {
        transform: scale(1.2);
        fill: #FEFEFE;
    }
}

@media (max-width : 768px) {
    .expand-button {
        color: #FEFEFE;
    }

    .expand-button svg {
        transform: scale(1.2);
        fill: #FEFEFE;
    }
}

</style>
