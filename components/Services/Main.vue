<template>
    <main class="main" role="main">
			<section class="section hero hero--alt">
				<div class="container">
					<div class="hero__body hero__body--centered">
						<h1 class="hero__title d-none d-lg-flex">
							{{ data.ServiceMainHeader.title }}
						</h1>
						<h1 class="hero__title d-lg-none">Our Services</h1>
						<p class="section__caption section__caption--sm">
							{{ data.ServiceMainHeader.description }}
						</p>
					</div>
				</div>
			</section>

			<section class="section section--padded section--greyed">
				<div class="container">
					<div class="section__heading section__heading--centered">
						<h2 class="section__sub-title">{{ data.ServiceSecondHeader.title }}</h2>
						<p class="section__caption--sm">{{ data.ServiceSecondHeader.description }}</p>
					</div>
					<div class="section__flex three-words">
						<template 
							v-for="info in data.ServiceSecondHeader.ServiceList"
						>
							<div class="three-words__item" :key="info.id">
								<h4 class="label">{{ info.firstHeader}}</h4>
								<div>
									<h5>{{ info.secondHeader}}</h5>
									<p>{{ info.description}}</p>
								</div>
							</div>	
						</template>
					</div>
				</div>
			</section>

			<section class="section section--padded">
				<div class="container">
					<div class="section__heading section__heading--centered">
						<h2 class="section__sub-title">{{ data.ServiceThirdBanner.title}}</h2>
					</div>
					<div class="section__grid service__grid">
						<template
							v-for="info in data.ServiceThirdBanner.services"
						>
							<div class="service__item" :key="info.id">
								<div>
									<img :src="`${info.image[0].url}`" :alt="`${info.title }`">
								</div>
								<h5>{{ info.title }}</h5>
								<p>{{ info.description }}</p>
							</div>
						</template>
					</div>
				</div>
			</section>

			<section class="section d-none">
				<div class="section__flex">
<!--					<div class="container">-->
						<img src="~/assets/img/img-grid.png" alt="img-grid">
<!--					</div>-->
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