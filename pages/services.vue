<template>
  <div>
    <SiteHeader />
    <ServicesMain :data="data.service" :contactComponent="data.contactComponent" />
    <SiteFooter :data="data.footer" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Altalabs - Services'
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            ''
        }
      ]
    }
  },
  async asyncData({ $axios }) {
		const data = await Promise.all([
			$axios.$get(`${process.env.baseUrl}/service`),
			$axios.$get(`${process.env.baseUrl}/contact-component`),
			$axios.$get(`${process.env.baseUrl}/footer`)
		]);
		return {
			data: {
				service: data[0],
				contactComponent: data[1],
				footer: data[2]
			}
		};
	}
}
</script>

