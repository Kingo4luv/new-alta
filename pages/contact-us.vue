<template>
  <div>
    <SiteHeader />
    <ContactMain :data="data.contact" />
    <SiteFooter :data="data.footer" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Altalabs - Contact'
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
			$axios.$get(`${process.env.baseUrl}/contact`),
			$axios.$get(`${process.env.baseUrl}/footer`)
		]);
		return {
			data: {
				contact: data[0],
				footer: data[1]
			}
		};
	}
}
</script>

