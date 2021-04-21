<template>
  <div>
    <SiteHeader />
    <HomeMain :data="data.home" :contactComponent="data.contactComponent" />
    <SiteFooter :data="data.footer" />
  </div>
</template>

<script>
export default {
	async asyncData({ $axios }) {
		const data = await Promise.all([
			$axios.$get(`${process.env.baseUrl}/home`),
			$axios.$get(`${process.env.baseUrl}/contact-component`),
			$axios.$get(`${process.env.baseUrl}/footer`)
		]);
		return {
			data: {
				home: data[0],
				contactComponent: data[1],
				footer: data[2]
			}
		};
	}
};
</script>
