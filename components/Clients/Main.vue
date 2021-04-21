<template>
    <main class="main" role="main">
			<section class="section section--greyed hero hero--alt">
				<div class="container">
					<div class="hero__body hero__body--wide">
						<h1 class="hero__title">{{ data.title }}</h1>
						<p class="section__caption">{{ data.description }}</p>
					</div>
				</div>
			</section>

			<section class="section section--padded">
				<div class="container">
					<div class="section__grid card__wrapper">
						<template
							v-for="info in data.box"
						>
							<div class="card__item" :key="info.id">
								<a :href="`${info.link}`" target="_blank" class="card__heading">
									<img class="card__media" :src="`${ info.image[0].url}`" :alt="`${info.title} logo`">
									<div>
										<h5 class="card__title">{{ info.title }}</h5>
										<p>{{ info.industry }} </p>
									</div>
								</a>
								<p class="d-none">{{ info.description }}</p>
							</div>
						</template>
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