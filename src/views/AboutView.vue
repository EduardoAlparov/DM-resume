<template>
	<div class="">

		<div class="slider w-slider">
			<div class="mask w-slider__mask">
				<div class="slide w-slider__slide">

					<div class="slide__flex">

						<div class="slide__main-heading-wrapper">
							<h1 class="slide__main-heading">
								эдуард&nbsp;<br>aлпаров
							</h1>
						</div>

						<div class="slide__slice-wrapper">
							<div class="img-container-1">
								<div class="s1-img-slice-1 abt-s1-img-slice-1"></div>
							</div>

							<div class="img-container-2">
								<div class="s1-img-slice-2 abt-s1-img-slice-2"></div>
							</div>

							<div class="img-container-3 ">
								<div class="s1-img-slice-3 abt-s1-img-slice-3"></div>
							</div>
						</div>

						<div class="slide__text-wrapper">
							<div class="slide__details-wrapper _name-parent">
								<h2 class="slide__about-text-heading">
									Обо мне
								</h2>
								<h3 class="details-bold slide__details-bold">
									Morbi lacinia, ligula quis maximus mollis,
									orci lectus ornare enim, vel rhoncus
									tellus libero ut arcu.
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
									Скиллы и технологии:
								</h2>

								<div class="_name-text">
									.about
								</div>
							</div>

							<div class="slide__services-flex">
								<div class="slide__servies-block-one">
									<span class="_accent-color">#</span>
									CLEARE CSS <span class="_accent-color">and</span> scss
									<br>
									<span class="_accent-color">#</span>
									semantic HTML
									<br>
								</div>

								<div class="slide__servies-block-two">
									<span class="_accent-color">#</span>
									vanilla JS
									<br>
									<span class="_accent-color">#</span>
									Vue
									<br>
								</div>

								<div class="slide__servies-block-three">
									<span class="_accent-color">#</span>
									figma
									<br>
								</div>
							</div>
						</div>
					</div>

				</div>
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
import SocialsComponent from "../components/commons/SocialsComponent.vue";

export default {
    name: "AboutView",
	components: {
		SocialsComponent
	},
}
</script>

<style scoped>
@import url('../assets/css/layout/back-container.css');
@import url('../assets/css/layout/back-container-2.css');
@import url('../assets/css/layout/back-dark.css');
</style>
