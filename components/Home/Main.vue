<template>
    <main class="main" role="main">
			<section class="section hero">
				<div class="container">
					<div class="hero__body">
						<h1 class="hero__title">{{ data.HomeMainBanner.title }}</h1>
						<p class="hero__caption">{{ data.HomeMainBanner.description }}</p>
					</div>
					<div class="hero__cta">
						<nuxt-link class="btn btn__primary" to="contact-us">
							{{ data.HomeMainBanner.call_to_action }}
							<svg width="18" height="13" fill="none" xmlns="http://www.w3.org/2000/svg">
								<path d="M2 6.5h14m0 0L11.6 2M16 6.5L11.6 11" stroke="#fff" stroke-width="2.977" stroke-linecap="round" stroke-linejoin="round"/>
							</svg>
						</nuxt-link>
					</div>
				</div>
			</section>

			<section class="section section--dark section--padded">
				<div class="container">
					<div class="section__heading">
						<h1 class="section__title">{{ data.HomeSecondBanner.title }}</h1>
						<p class="section__caption section__caption--sm">{{ data.HomeSecondBanner.description }}</p>
					</div>
					<div class="section__grid section__grid--left-pad">
						<div>
							<h4>{{ data.HomeSecondBanner.firstSubHeader }}</h4>
							<ul class="section__list">
								<li
									v-for="list in data.HomeSecondBanner.firstSubList"
									:key="list.id"
								>
									{{ list.title }}
								</li>
							</ul>
						</div>
						<div>
							<h4>{{ data.HomeSecondBanner.secondSubHeader }}</h4>
							<ul class="section__list">
								<li
									v-for="list in data.HomeSecondBanner.secondSubList"
									:key="list.id"
								>
									{{ list.title }}
								</li>
							</ul>
						</div>
						<div>
							<h4>{{ data.HomeSecondBanner.thirdSubHeader }}</h4>
							<ul class="section__list">
								<li
									v-for="list in data.HomeSecondBanner.thirdSubList"
									:key="list.id"
								>
									{{ list.title }}
								</li>
							</ul>
						</div>
					</div>
				</div>
			</section>

			<section class="section section--padded">
				<div class="container section__flex">
					<div class="section__body">
						<div class="section__heading section__heading--wide">
							<h1 class="section__title">
								{{ data.HomeThirdBanner.first_title }}
								<br>
								{{ data.HomeThirdBanner.second_title }}
							</h1>
							<p class="section__caption section__caption--sm pr-lg-5">
								{{ data.HomeThirdBanner.description }}
							</p>
						</div>
						<div class="section__cta">
							<nuxt-link class="btn btn__light" to="contact-us">
								{{ data.HomeThirdBanner.call_to_action }}
								<svg width="18" height="13" fill="none" xmlns="http://www.w3.org/2000/svg">
									<path d="M2 6.5h14m0 0L11.6 2M16 6.5L11.6 11" stroke="#fff" stroke-width="2.977" stroke-linecap="round" stroke-linejoin="round"/>
								</svg>
							</nuxt-link>
						</div>
					</div>
					<div class="section__media">
						<img src="~/assets/img/nexus.svg" alt="nexus">
					</div>
				</div>
			</section>

			<section class="section">
				<div class="section__grid section__grid--features">
					<div class="section__body">
						<div class="section__heading section__heading--wide">
							<h1 class="section__title section__title--light">
								{{ data.HomeFourthBanner.title }}
							</h1>
							<p class="section__caption section__caption--sm">
								{{ data.HomeFourthBanner.description }}
							</p>
						</div>
						<div class="section__cta">
							<nuxt-link class="btn btn__light--outline" to="clients">
								{{ data.HomeFourthBanner.call_to_action }}
								<svg width="18" height="13" fill="none" xmlns="http://www.w3.org/2000/svg">
									<path d="M2 6.5h14m0 0L11.6 2M16 6.5L11.6 11" stroke="#fff" stroke-width="2.977" stroke-linecap="round" stroke-linejoin="round"/>
								</svg>
							</nuxt-link>
						</div>
					</div>
					<div class="section__media">
						<img src="~/assets/img/laptop-background.png" alt="laptop-background">
					</div>

					<div class="section__body">
						<div class="section__heading section__heading--wide">
							<h1 class="section__title section__title--light">
								{{ data.HomeFifthBanner.title }}
							</h1>
							<p class="section__caption section__caption--sm">
								{{ data.HomeFifthBanner.description }}
							</p>
						</div>
					</div>
					<div class="section__media">
						<img src="~/assets/img/tech.png" alt="tech">
					</div>
				</div>
			</section>

			<section class="section section--padded section--greyed">
				<div class="container">
					<div class="section__body">
						<div class="section__heading section__heading--wide">
							<h1 class="section__title">{{ data.HomeSixthBanner.title }}</h1>
							<p class="section__caption section__caption--sm">
								{{ data.HomeSixthBanner.description }}
							</p>
						</div>
					</div>
					<div class="logo__scroller">
						<div class="logo__container">
							<img src="~/assets/img/logo/dryva.png" alt="dryva logo">
							<img src="~/assets/img/logo/ladda.png" alt="ladda logo">
							<img src="~/assets/img/logo/vfd-group.png" alt="vfd group logo">
							<img src="~/assets/img/logo/kudi.png" alt="kudi logo">
							<img src="~/assets/img/logo/shuttlers.png" alt="shuttlers logo">
							<img src="~/assets/img/logo/unical-lg.png" alt="unical logo">
							<img src="~/assets/img/logo/rovedana.svg" alt="rovedana logo">
							<img src="~/assets/img/logo/patricia-gifts-logo.svg" alt="patricia logo">
							<img src="~/assets/img/logo/FCMB.png" alt="FCMB logo">
							<img src="~/assets/img/logo/yellow-jasper.svg" alt="yellow-jasper logo">
							<img src="~/assets/img/logo/chaka-lg.png" alt="chaka">

							<img src="~/assets/img/logo/eplat.png" alt="eplat logo">
							<img src="~/assets/img/logo/Group 688.png" alt="yellow jasper logo">
							<img src="~/assets/img/logo/techspec.png" alt="techspec logo">
							<img src="~/assets/img/logo/kudi.png" alt="kudi logo">
							<img src="~/assets/img/logo/shuttlers.png" alt="shuttlers logo">
							<img src="~/assets/img/logo/unical-lg.png" alt="unical logo">
							<img src="~/assets/img/logo/rovedana.svg" alt="rovedana logo">
							<img src="~/assets/img/logo/patricia-gifts-logo.svg" alt="patricia logo">
							<img src="~/assets/img/logo/kudi.png" alt="kudi logo">
							<img src="~/assets/img/logo/shuttlers.png" alt="shuttlers logo">
							<img src="~/assets/img/logo/unical-lg.png" alt="unical logo">
							<img src="~/assets/img/logo/rovena.png" alt="rovedana logo">
							<img src="~/assets/img/logo/patricia-gifts-logo.svg" alt="patricia logo">

						</div>
						<div class="logo__container logo__container--left">
							<img src="~/assets/img/logo/FCMB.png" alt="FCMB logo">
							<img src="~/assets/img/logo/yellow-jasper.svg" alt="yellow-jasper logo">
							<img src="~/assets/img/logo/chaka-lg.png" alt="chaka logo">
							<img src="~/assets/img/logo/kudi.png" alt="kudi logo">
							<img src="~/assets/img/logo/shuttlers.png" alt="shuttlers logo">
							<img src="~/assets/img/logo/unical-lg.png" alt="unical logo">
							<img src="~/assets/img/logo/rovedana.svg" alt="rovedana logo">
							<img src="~/assets/img/logo/patricia-gifts-logo.svg" alt="patricia logo">
							<img src="~/assets/img/logo/eplat.png" alt="eplat logo">
							<img src="~/assets/img/logo/Group 688.png" alt="emerging logo">
							<img src="~/assets/img/logo/dryva.png" alt="dryva logo">
							<img src="~/assets/img/logo/ladda.png" alt="ladda logo">
							<img src="~/assets/img/logo/techspec.png" alt="techspec logo">
							<img src="~/assets/img/logo/rovedana.svg" alt="rovedana logo">
							<img src="~/assets/img/logo/patricia-gifts-logo.svg" alt="patricia logo">
							<img src="~/assets/img/logo/eplat.png" alt="eplat logo">
							<img src="~/assets/img/logo/Group 688.png" alt="emerging logo">
							<img src="~/assets/img/logo/techspec.png" alt="techspec logo">
							<img src="~/assets/img/logo/rovena.png" alt="rovena logo">
							<img src="~/assets/img/logo/vfd-group.png" alt="vfd group logo">
							<img src="~/assets/img/logo/patricia-gifts-logo.svg" alt="">
							<img src="~/assets/img/logo/eplat.png" alt="eplat logo">
							<img src="~/assets/img/logo/Group 688.png" alt="emerging logo">
							<img src="~/assets/img/logo/techspec.png" alt="techspec logo">
							<img src="~/assets/img/logo/dryva.png" alt="dryva logo">
							<img src="~/assets/img/logo/ladda.png" alt="ladda logo">
						</div>
					</div>
				</div>
			</section>

			<section class="section">
				<div class="features">
					<div class="section__body">
						<div class="section__heading section__heading--wide">
							<h1 class="section__title">{{ data.HomeSeventhBanner.title }}</h1>
							<p class="section__caption section__caption--sm">
								{{ data.HomeSeventhBanner.description }}
							</p>
						</div>
						<div class="section__cta">
							<nuxt-link class="btn btn__light" to="services">
								{{ data.HomeSeventhBanner.call_to_action }}
								<svg width="18" height="13" fill="none" xmlns="http://www.w3.org/2000/svg">
									<path d="M2 6.5h14m0 0L11.6 2M16 6.5L11.6 11" stroke="#fff" stroke-width="2.977" stroke-linecap="round" stroke-linejoin="round"/>
								</svg>
							</nuxt-link>
						</div>
					</div>
					<div class="features__item">
						<div class="features__media">
							<img src="~/assets/img/chess.png" alt="what we do">
						</div>
					</div>
<!--					<div class="features__item">-->
<!--						<div class="features__media">-->
<!--							<img src="img/table.png" alt="">-->
<!--						</div>-->
<!--					</div>-->
<!--					<div class="features__item">-->
<!--						<div class="features__media">-->
<!--							<img src="img/desktop.png" alt="">-->
<!--						</div>-->
<!--					</div>-->
<!--					<div class="features__item">-->
<!--						<div class="features__media">-->
<!--							<img src="img/strategy.png" alt="">-->
<!--						</div>-->
<!--					</div>-->
<!--					<div class="features__item">-->
<!--						<div class="features__media">-->
<!--							<img src="img/paper.png" alt="">-->
<!--						</div>-->
<!--					</div>-->
				</div>
			</section>

			<section class="section section--padded testimonials d-none">
				<div class="section__heading section__heading--centered">
					<h2>Our Clients Are Saying</h2>
					<p>Below we have shared some feedback we received from our clients.</p>
				</div>
				<div class="container">
					<div class="slider">
						<div class="slider__wrapper">
							<div class="slider-item">
								<div class="slider__body">
									<p>“You simply can't know how deep the rabbit hole goes, and stack helps provide that essential initial direction so Even propositions and user personas make attempting an a comparison a dangerous game.”</p>
								</div>
								<div class="slider__meta">
									<div class="slider__media">
										<img src="~/assets/img/Ellipse.png" alt="ellipse">
									</div>
									<div>
										<p><strong>Cletus Adewale</strong></p>
										<p>CTO Techpoint</p>
									</div>
								</div>
							</div>
							<div class="slider-item">
								<div class="slider__body">
									<p>“You simply can't know how deep the rabbit hole goes, and stack helps provide that essential initial direction so Even propositions and user personas make attempting an a comparison a dangerous game.”</p>
								</div>
								<div class="slider__meta">
									<div class="slider__media">
										<img src="~/assets/img/Ellipse.png" alt="">
									</div>
									<div>
										<p><strong>Cletus Adewale</strong></p>
										<p>CTO Techpoint</p>
									</div>
								</div>
							</div>
							<div class="slider-item">
								<div class="slider__body">
									<p>“You simply can't know how deep the rabbit hole goes, and stack helps provide that essential initial direction so Even propositions and user personas make attempting an a comparison a dangerous game.”</p>
								</div>
								<div class="slider__meta">
									<div class="slider__media">
										<img src="~/assets/img/Ellipse.png" alt="">
									</div>
									<div>
										<p><strong>Cletus Adewale</strong></p>
										<p>CTO Techpoint</p>
									</div>
								</div>
							</div>
							<div class="slider-item">
								<div class="slider__body">
									<p>“The services provided by Alta have ranged from fashioning out new features, wrangling with overnight algorithm adjustments to ongoing technical support...It goes without saying that if you're in the market for a local professional development team, Alta Labs is highly recommended.” </p>
								</div>
								<div class="slider__meta">
									<div class="slider__media">
										<img src="~/assets/img/Ellipse.png" alt="">
									</div>
									<div>
										<p><strong>Cletus Adewale</strong></p>
										<p>CTO Kudy Financials</p>
									</div>
								</div>
							</div>
							<div class="slider-item">
								<div class="slider__body">
									<p>“You simply can't know how deep the rabbit hole goes, and stack helps provide that essential initial direction so Even propositions and user personas make attempting an a comparison a dangerous game.”</p>
								</div>
								<div class="slider__meta">
									<div class="slider__media">
										<img src="~/assets/img/Ellipse.png" alt="">
									</div>
									<div>
										<p><strong>Cletus Adewale</strong></p>
										<p>CTO Techpoint</p>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>
			</section>

			<ContactSection :data="contactComponent" />
		</main>
</template>

<script>
export default {
	props: {
		data: {
			type: Object
		},
		contactComponent: {
			type: Object
		}
	}
}
</script>