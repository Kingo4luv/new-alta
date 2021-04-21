<template>
    <main class="main" role="main">
			<section class="section hero hero--alt">
				<div class="container">
					<div class="hero__body hero__body--wide">
						<h1 class="hero__title d-none d-lg-flex">{{ data.AboutMainBanner.title }}</h1>
						<h1 class="hero__title d-lg-none">We are passionate about helping businesses grow</h1>
						<p class="section__caption section__caption--sm">{{ data.AboutMainBanner.description }}</p>
					</div>
				</div>
			</section>

			<section class="section section--greyed section--padded">
				<div class="container">
					<div class="section__flex">
						<template v-for="list in data.SecondBanner">
							<div
								class="stats__item"
								:key="list.id"
							>
								<h1>{{ list.header }}</h1>
								<span>{{ list.sub_text }}</span>
								<p>{{ list.description }}</p>
							</div>
						</template>
					</div>
				</div>
			</section>

			<section class="section section--padded about">
				<div class="container">
					<div class="section__body">
						<div class="section__heading section__heading--wide">
							<h1 class="section__title">{{ data.ThirdBanner.title }}</h1>
						</div>
						<p
							class="about__text"
							v-for="list in data.ThirdBanner.paragraphs"
							:key="list.id"
						>
							{{ list.description}}
						</p>
						<template
							v-for="list in data.fourthBanner"
						>
							<span :key="list.id">
								<h6><strong>{{ list.title}}</strong></h6>
								<p class="about__text">{{ list.description}}</p>
							</span>
						</template>
					</div>
					<div class="section__body section__body--pad-top d-none">
						<div class="section__heading section__heading--wide">
							<h1 class="section__title">Our Dedicated Team Members</h1>
							<p class="section__caption">Meet the Team.</p>
						</div>
						<p class="about__text">Product design dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quiaolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam dolor sit amet, dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quiaolor sit amet, consectetur, adipisci velit, sed qui aliqua. </p>
						<p class="about__text">Voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. perspiciatis unde omnis iste natus error sit Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore </p>
						<p class="about__text">magnam aliquam quaerat voluptatem. Aliquam bibendum lacus quis nulla dignissim faucibus. Sed mauris enim, bibendum at purus aliquet, maximus molestie tortor. Sed faucibus et tellus aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. perspiciatis unde omnis iste natus error sit Nemo e eu sollicitudin.</p>
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