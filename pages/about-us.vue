<template>
  <div>
    <SiteHeader />
    <AboutMain :data="data.about" :contactComponent="data.contactComponent" />
    <SiteFooter :data="data.footer" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Altalabs - About'
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
			$axios.$get(`${process.env.baseUrl}/about`),
			$axios.$get(`${process.env.baseUrl}/contact-component`),
			$axios.$get(`${process.env.baseUrl}/footer`)
		]);
		return {
			data: {
				about: data[0],
				contactComponent: data[1],
				footer: data[2]
			}
		};
	}
}
</script>
