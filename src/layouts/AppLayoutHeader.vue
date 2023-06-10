<template>
    <header class="header">
        <a href="/" class="header__logo logo _name-parent">
            <span>
                Эдуард Алпаров.
            </span>

            <span class="logo__text-span">
                front-end разработка
            </span>

            <div class="_name-text">
                .logo
            </div>
        </a>

        <div class="header__nav">
            <ul class="nav _name-parent">
                <li class="nav__item">
                    <router-link
                        to="/"
                        tag="a"
                        href="#"
                        class="nav__link"
                    >
                        <span class="nav__link-text">
                            обо мне.
                            <br>
                            обо мне.
                        </span>
                    </router-link>
                </li>

                <li class="nav__item">
                    <router-link
                        to="/works"
                        tag="a"
                        href="#"
                        class="nav__link"
                    >

                        <span class="nav__link-text">
                            работы.
                            <br>
                            работы.
                        </span>

                    </router-link>
                </li>

                <li class="nav__item">
                    <router-link
                        to="/contacts"
                        tag="a"
                        href="#"
                        class="nav__link"
                    >

                        <span class="nav__link-text">
                            контакты.
                            <br>
                            контакты.
                        </span>

                    </router-link>
                </li>

                <div class="_name-text">
                    .nav
                </div>
            </ul>
        </div>

        <div class="header__mobile-nav _name-parent">
            <button
                class="mobile-nav__menu-heading-wrapper"
                @click="$emit('toggleModal', isModalMenuVisible)"
            >
                <div class="mobile-nav__menu-text">
                    Меню
                    <br>
                    закрыть
                </div>

                <div class="mobile-nav__icon-bar-wrapper">
                    <div class="mobile-nav__icon-bar _1"></div>
                    <div class="mobile-nav__icon-bar _2"></div>
                    <div class="mobile-nav__icon-bar _3"></div>
                </div>
            </button>

            <div class="_name-text _name-text_right">
                .mobile-nav
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: "AppLayoutHeader",
    props: {
        isModalMenuVisible: {
            type: Boolean,
            default: false
        }
    }
}
</script>

<style scoped>
.header {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    z-index: 13;

    width: 90%;
    height: auto;
    display: flex;
    margin-right: auto;
    margin-left: auto;
    padding-top: 30px;
    padding-bottom: 30px;

}

.header__logo,
.header__nav {
    flex-shrink: 0;
    flex-basis: 50%;
}

.header__mobile-nav {
    display: none;
    flex-shrink: 0;
    flex-basis: 50%;
}

/* md <= Large (lg) */
@media (max-width : 991px) {
    .header__nav {
        display: none;
    }

    .header__mobile-nav {
        display: block;
    }
}

.nav {
    display: flex;
}

.nav_mobile-menu {
    flex-direction: column;
}

.nav__item {
    position: relative;

    flex-shrink: 0;
    flex-basis: calc(100% / 3);
}

.nav__link {
    position: relative;
    z-index: 1;
    overflow-x: visible;
    overflow-y: clip;

    display: inline-block;
    height: 20px;

    font-size: 12px;
    font-weight: 400;
    text-decoration: none;
    text-transform: uppercase;
    color: inherit;
    cursor: pointer;
}

.nav_mobile-menu .nav__link {
    padding-top: 30px;
    padding-bottom: 30px;

    color: #fdfdff;
    font-size: 3.5rem;
    line-height: 30px;
    font-weight: 400;
    text-transform: none;
}

.nav__link-text {
    display: block;
    width: auto;
    height: 40px;

    transform: translate3d(0px, 0%, 0px) scale3d(1, 1, 1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) skew(0deg, 0deg);
    transform-style: preserve-3d;

    pointer-events: none;
    transition: 0.2s;
    line-height: 20px;
}

@media (any-hover: hover) {
    .nav__link:hover .nav__link-text {
        transform: translate3d(0px, -50%, 0px) scale3d(1, 1, 1) rotateX(0deg) rotateY(0deg) rotateZ(0deg) skew(0deg, 0deg);
    }
}

/* md <= Large (lg) */
@media (max-width : 991px) {

}

/* sm <= Medium (md) */
@media (max-width : 768px) {
    .nav_mobile-menu .nav__link {
        font-size: 2rem;
    }
}

.mobile-nav__menu-heading-wrapper {
    position: relative;

    display: flex;
    overflow: hidden;
    width: 73px;
    height: 17px;
    float: right;
    align-items: center;

    border: none;
    background-color: unset;
    outline: none;
    cursor: pointer;
}

.mobile-nav__menu-text {
    position: relative;
    z-index: 1;

    display: inline-block;
    width: 50px;
    margin-top: 19px;

    color: #fff;
    line-height: 20px;
    font-weight: 500;

    background-color: transparent;
}

.mobile-nav__icon-bar {
    width: 100%;
    height: 1px;
    margin-top: 5px;

    background-color: #fff;
}

.mobile-nav__icon-bar._1 {
    width: 20px;
    margin-top: 0px;
}

.mobile-nav__icon-bar._2 {
    width: 23px;
}

.mobile-nav__icon-bar._3 {
    width: 20px;
}

.mobile-nav__icon-bar-wrapper {
    position: absolute;
    top: 0px;
    right: 0px;
    bottom: 0px;

    display: flex;
    overflow: hidden;
    width: 23px;
    height: 17px;
    flex-direction: column;
    justify-content: center;

    align-items: flex-end;
}


.router-link-exact-active::after {
    position: absolute;
    top: 50%;
    right: auto;
    left: calc(100% + 2rem);
    z-index: 14;

    font-family: 'Russo One', sans-serif;
    color: saddlebrown;
    font-size: 10px;
    text-transform: lowercase;

    transform: translateY(-50%);
    content: '.active';
}

</style>
