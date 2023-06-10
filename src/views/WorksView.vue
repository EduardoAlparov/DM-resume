<template>
	<div class="">
		<div class="slider w-slider">
			<div class="mask w-slider__mask">
				<Flickity
					ref="flickity"
					:options="flickityOptions"
				>
					<SlideItem
						class="carousel-cell"
						v-for="work in works"
						:key="work.id"
						:work="work"
					/>
				</Flickity>
			</div>

			<div class="w-slider__button w-slider__button-left-arrow">
				<button
					@click="previous()"
					:disabled="disablePrevButton"
					class="_reset-button buttons__left-arrow-wrapper"
				>
					<span class="buttons__left-icon">
						<svg viewBox="0 0 52 52" xmlns="http://www.w3.org/2000/svg">
							<g data-name="Group 132" id="Group_132">
								<path d="M14,52a2,2,0,0,1-1.41-3.41L35.17,26,12.59,3.41a2,2,0,0,1,0-2.82,2,2,0,0,1,2.82,0l24,24a2,2,0,0,1,0,2.82l-24,24A2,2,0,0,1,14,52Z"/>
							</g>
						</svg>
					</span>
				</button>
			</div>

			<div class="w-slider__button w-slider__button-right-arrow">
				<button
					@click="next()"
					:disabled="disableNextButton"
					class="_reset-button buttons__right-arrow-wrapper"
				>
					<span class="buttons__right-icon">
						<svg viewBox="0 0 52 52" xmlns="http://www.w3.org/2000/svg">
							<g data-name="Group 132" id="Group_132">
								<path d="M14,52a2,2,0,0,1-1.41-3.41L35.17,26,12.59,3.41a2,2,0,0,1,0-2.82,2,2,0,0,1,2.82,0l24,24a2,2,0,0,1,0,2.82l-24,24A2,2,0,0,1,14,52Z"/>
							</g>
						</svg>
					</span>
				</button>
			</div>
		</div>

		<div class="back-container">
            <div class="back-container__column back-container__column_first"></div>
            <div class="back-container__column"></div>
            <div class="back-container__column"></div>
            <div class="back-container__column"></div>
            <div class="back-container__column"></div>
            <div class="back-container__column"></div>
            <div class="back-container__column"></div>
            <div class="back-container__column back-container__column_last"></div>
        </div>

        <div class="back-container-2">
          <div class="back-container-2__column back-container-2__column_first">
            <div class="back-container-2__socials">
                <SocialsComponent />
            </div>
          </div>
          <div class="back-container-2__column"></div>
          <div class="back-container-2__column"></div>
        </div>

        <div class="back-dark"></div>
	</div>
</template>

<script>
import works from '../static/works.json'

import Flickity from 'vue-flickity';
import "flickity-fade";

import SlideItem from "../components/slider/SlideItem.vue";
import SocialsComponent from "../components/commons/SocialsComponent.vue";
export default {
    name: "WorksView",

	components: {
		SlideItem,
		Flickity,
		SocialsComponent
	},

	data() {
		return {
			decorClass: '.work',

			flickityOptions: {
				prevNextButtons: false,
				pageDots: false,
				wrapAround: false,
				fade: true,
				draggable: false
			},

			works: works,

			counter: 1,

			disableNextButton: false,
			disablePrevButton: true
		}
	},

	methods: {
		next() {
			this.$refs.flickity.next();

			this.counter += 1;

			if (this.$refs.flickity.getCellElements().length == this.counter) {
				this.disableNextButton = true;
			}
			if (this.counter > 1) {
				this.disablePrevButton = false;
			}
		},

		previous() {
			this.$refs.flickity.previous();

			this.counter -= 1;

			if (this.counter > 1) {
				this.disablePrevButton = false;
			} else {
				this.disablePrevButton = true;
			}

			if (this.$refs.flickity.getCellElements().length > this.counter) {
				this.disableNextButton = false;
			}
		}
	}
}
</script>
<style scoped>
@import url('../assets/css/layout/back-container.css');
@import url('../assets/css/layout/back-container-2.css');
@import url('../assets/css/layout/back-dark.css');

.carousel-cell {
	width: 100%;
	height: 100vh;
}

</style>
