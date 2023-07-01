<template>
    <div class="mobile-menu">
        <ul class="nav nav_mobile-menu _name-parent">
            <li class="nav__item">
                <a 
                    class="nav__link"
                    @click="clickHandler('')"
                >
                    <span class="nav__link-text">
                        Обо мне
                    </span>
                </a>
            </li>

            <li class="nav__item">
                <a
                    class="nav__link"
                    @click="clickHandler('works')"
                >
                    <span class="nav__link-text">
                        Работы
                    </span>
                </a>
            </li>

            <li class="nav__item">
                <a 
                    class="nav__link"
                    @click="clickHandler('contacts')"
                >
                    <span class="nav__link-text">
                        Контакты
                    </span>
                </a>
            </li>

            <div class="_name-text">
                .mobile-menu
            </div>
        </ul>

        <div class="mobile-social">
            <ul class="socials socials_mobile _name-parent">
                <li class="socials__item">
                    <a href="https://github.com/EduardoAlparov" class="socials__link" aria-label="to github" target="_blank">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64">
                            <path d="M32,10c12.15,0,22,9.85,22,22c0,9.768-6.369,18.045-15.179,20.916c0.002-0.008,0.006-0.021,0.006-0.021	s-1.485-0.696-1.453-1.938c0.035-1.367,0-4.556,0-5.727c0-2.01-1.272-3.434-1.272-3.434s9.977,0.112,9.977-10.533	c0-4.107-2.147-6.245-2.147-6.245s1.128-4.385-0.39-6.245c-1.701-0.184-4.749,1.626-6.05,2.472c0,0-2.062-0.846-5.492-0.846	c-3.43,0-5.492,0.846-5.492,0.846c-1.301-0.846-4.348-2.656-6.05-2.472c-1.518,1.86-0.39,6.245-0.39,6.245s-2.147,2.137-2.147,6.245	c0,10.645,9.977,10.533,9.977,10.533s-1.005,1.136-1.225,2.806c-0.696,0.236-1.721,0.528-2.549,0.528	c-2.165,0-3.812-2.105-4.416-3.078c-0.595-0.96-1.815-1.766-2.953-1.766c-0.749,0-1.115,0.375-1.115,0.803s1.05,0.727,1.743,1.521	c1.461,1.674,1.435,5.438,6.641,5.438c0.565,0,1.719-0.139,2.588-0.256c-0.005,1.185-0.007,2.436,0.012,3.167	c0.031,1.242-1.453,1.938-1.453,1.938s0.004,0.012,0.006,0.021C16.369,50.045,10,41.768,10,32C10,19.85,19.85,10,32,10z"></path>
                        </svg>
                    </a>
                </li>

                <li class="socials__item">
                    <a href="https://t.me/EdFrontDev" class="socials__link" aria-label="to telegram" target="_blank">
                        <svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 72 72">
                            <path d="M36,12c13.255,0,24,10.745,24,24S49.255,60,36,60S12,49.255,12,36S22.745,12,36,12z M44.279,45.783	c0.441-1.354,2.51-14.853,2.765-17.513c0.077-0.806-0.177-1.341-0.676-1.58c-0.603-0.29-1.496-0.145-2.533,0.229	c-1.421,0.512-19.59,8.227-20.64,8.673c-0.995,0.423-1.937,0.884-1.937,1.552c0,0.47,0.279,0.734,1.047,1.008	c0.799,0.285,2.812,0.895,4.001,1.223c1.145,0.316,2.448,0.042,3.178-0.412c0.774-0.481,9.71-6.46,10.351-6.984	c0.641-0.524,1.152,0.147,0.628,0.672c-0.524,0.524-6.657,6.477-7.466,7.301c-0.982,1.001-0.285,2.038,0.374,2.453	c0.752,0.474,6.163,4.103,6.978,4.685c0.815,0.582,1.641,0.846,2.398,0.846S43.902,46.94,44.279,45.783z"/>
                        </svg>
                    </a>
                </li>

                <li class="socials__item">
                    <a href="https://vk.com/id316661997" class="socials__link" aria-label="to vk" target="_blank">
                        <svg xmlns="http://www.w3.org/2000/svg"	viewBox="0 0 64 64">
                            <path d="M40.227,12C51.146,12,52,12.854,52,23.773v16.453C52,51.145,51.146,52,40.227,52H23.773C12.854,52,12,51.145,12,40.227	V23.773C12,12.854,12.854,12,23.773,12H40.227z M43.851,39.792c0.723,0,1.914-0.119,1.008-1.628	c-0.076-0.125-0.528-1.115-2.72-3.152c-1.867-1.74-1.771-1.931,0.691-5.543c1.973-2.895,2.269-3.423,2.12-3.906	c-0.138-0.445-0.307-0.618-1.33-0.618c-0.888,0-3.105-0.057-3.822-0.057c-1.083,0-1.238,0.795-2.761,3.891	c-1.232,2.504-1.868,3.251-2.405,3.251c-0.613,0-0.937-0.639-0.937-3.021c0-3.384,0.161-4.802-2.814-4.802	c-4.16,0-4.351,0.976-3.856,1.214c0.614,0.294,1.453,0.651,1.453,2.391c0,2.549,0.015,4.057-0.72,4.057	c-0.735,0-1.121-0.344-2.695-3.212c-1.854-3.378-1.844-3.768-3.152-3.768c-1.056,0-2.488,0-3.419,0c-0.68,0-0.875,0.554-0.705,0.963	c0.216,0.518,3.29,7.474,6.531,10.758s6.552,3.184,7.036,3.184c0.153,0,0.705,0,0.904,0c1.015,0,1.378-0.579,1.465-1.049	c0.294-1.587,0.389-2.524,1.012-2.524c0.595,0,0.961,0.368,3.639,3.066c0.33,0.332,0.619,0.507,1.49,0.507	C40.738,39.792,43.128,39.792,43.851,39.792z"></path>
                        </svg>
                    </a>
                </li>

                <div class="_name-text _name-text_center">
                    .soc
                </div>
            </ul>
        </div>
    </div>
</template>

<script>

export default {
    name: "AppLayoutModalMenu",

    methods: {
        clickHandler: function(link) {
            this.$emit('closeMenu', 'false');
            
            if(link === 'contacts') {
                this.$router.push('/contacts');
            } else if(link === 'works') {
                this.$router.push('/works');
            } else {
                this.$router.push('/');
            }
        }
    },
}
</script>

<style scoped>
.mobile-menu {
    position: absolute;
    left: 0;
    top: 0px;
    bottom: 0px;
    z-index: 12;

    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    overflow: hidden;
    padding: 0 30px;

    background-color: #1c1d1d;
}

.mobile-menu_close {
    opacity: 0;
    visibility: hidden;
    pointer-events: none;
}

.mobile-social {
    position: absolute;
    left: 0px;
    right: 0px;
    bottom: 0px;

    display: flex;
    width: 100%;
    padding-top: 30px;
    padding-bottom: 30px;
    justify-content: center;
    align-items: center;
}

.socials {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 14px;
    width: 45px;
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
    overflow: hidden;

    max-width: 100%;
    width: 100%;
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
.socials_mobile {
    flex-direction: row;
    width: 100%;
    justify-content: space-evenly;
    gap: unset;
}

.socials__link {
    display: block;
    width: 100%;
    height: 45px;

    text-decoration: none;
    color: inherit;
    cursor: pointer;
}

.socials__link > svg {
    width: 100%;
    height: 100%;

    fill: var(--text);
    transition: 0.3s;
}

@media (any-hover: hover) {
    .socials__link:hover svg {
        fill: var(--accent);
    }
}
</style>
