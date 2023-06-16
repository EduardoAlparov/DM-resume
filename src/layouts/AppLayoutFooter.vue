<template>
    <footer
        class="footer"
        :class="{footer_close: !hiddenFooterClass}"
    >
        <p class="footer__details">
            © 2021 . <span style="color: saddlebrown">&#10084;</span> WebDev

            <span class="footer__simple-text">
                Inspired by
            </span>

            <a href="#" class="footer__link">
                Dexter Morgan
            </a>

            <button
                class="footer__banner-close"
                @click="$emit('changeHiddenFooterClass', hiddenFooterClass)"
            >
                <svg class="footer__banner-close-svg" viewBox="0 0 24 24">
                    <use xlink:href="../assets/img/icons/close.svg#close-svg"/>
                </svg>
            </button>
        </p>
    </footer>
</template>

<script>
export default {
    name: "AppLayoutFooter",
    props: {
        hiddenFooterClass: {
            type: Boolean,
            default: false
        }
    },
    mounted() {
        setTimeout(() => {
            this.$emit('changeHiddenFooterClass', this.hiddenFooterClass);
        }, 0);
    }
}
</script>

<style scoped>
.footer {
    position: fixed;
    left: 0%;
    top: auto;
    right: 0%;
    bottom: 0;
    z-index: 9;

    display: flex;
    height: 30px;
    justify-content: center;
    align-items: center;

    background-color: #e6e7e8;
    opacity: 1;
    transition: bottom 0.3s ease-in;
}

.footer_close {
    bottom: -30px;
    opacity: 0;
}

.footer__details {
    margin-top: 0px;
    margin-bottom: 0px;
    font-family: Lato, sans-serif;
    color: #666;
    font-size: 12px;
    text-align: left;
}

.footer__simple-text {
    margin-left: 15px;
}

.footer__link {
    margin-right: 15px;

    color: #333;
    font-weight: 700;
    text-decoration: none;
}
.footer__banner-close {
    width: 20px;
    height: 20px;
    vertical-align: bottom;

    border: none;
    background-color: unset;
    outline: none;
    cursor: pointer;
}

.footer__banner-close object {
    pointer-events: none;
}

/* xs <= Small (sm) */
@media (max-width : 576px) {
    .footer__details {
        position: relative;
    }

    .footer__simple-text {
        margin-left: 10px;
    }

    .footer__link {
        margin-right: 10px;
    }

    .footer__banner-close {
        position: absolute;
        right: -10px;
    }
}

</style>
