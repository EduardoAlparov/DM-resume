<template>
  <div id="app">
    <div class="wrapper">
        <AppLayoutHeader
            :is-modal-menu-visible="isModalMenuVisible"
            @toggleModal="toggleModal"
        />

        <router-view />

        <div class="buttons__banner-open-wrapper">
          <button
            class="buttons__banner-open"
            @click="hiddenFooterClass = !hiddenFooterClass"
            :disabled="hiddenFooterClass == true"
          >
            <span class="buttons__banner-open-icon">
              <svg viewBox="0 0 52 52" xmlns="http://www.w3.org/2000/svg">
                <g data-name="Group 132" id="Group_132">
                  <path d="M14,52a2,2,0,0,1-1.41-3.41L35.17,26,12.59,3.41a2,2,0,0,1,0-2.82,2,2,0,0,1,2.82,0l24,24a2,2,0,0,1,0,2.82l-24,24A2,2,0,0,1,14,52Z"/>
                </g>
              </svg>
            </span>
          </button>
        </div>

        <AppLayoutFooter
            :hidden-footer-class="hiddenFooterClass"
            @changeHiddenFooterClass="changeHiddenFooterClass"
        />

        <AppLayoutModalMenu v-show="isModalMenuVisible"/>

    </div>
  </div>
</template>

<script>
import AppLayoutHeader from "./layouts/AppLayoutHeader.vue";
import AppLayoutModalMenu from "./layouts/AppLayoutModalMenu.vue";
import AppLayoutFooter from "./layouts/AppLayoutFooter.vue";


export default {
    name: 'AppLayoutDefault',

    components: {
        AppLayoutHeader,
        AppLayoutModalMenu,
        AppLayoutFooter,
    },

    data() {
        return {
            isModalMenuVisible: false,
            hiddenFooterClass: true
        }
    },

    methods: {
        toggleModal() {
            this.isModalMenuVisible = !this.isModalMenuVisible;
        },
        changeHiddenFooterClass() {
            this.hiddenFooterClass = !this.hiddenFooterClass;
        }
    }
}
</script>

<style lang="scss">
@import url('./assets/css/main.css');

html,
body {
  height: 100%;
}

#app {
  height: 100%;
}

.wrapper {
  width: 100%;
  height: 100%;

  position: relative;
  overflow: hidden;
}

@keyframes coloring {
    0% {
        transform: translate3d(-100%, 0, 0);
        opacity: 0;
    }

    100% {
        transform: translate3d(0px, 0, 0);
        opacity: 1;
    }
}

</style>
