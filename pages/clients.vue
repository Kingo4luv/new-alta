<template>
  <div>
    <SiteHeader />
    <ClientsMain :data="data.client" :contactComponent="data.contactComponent" />
    <SiteFooter :data="data.footer" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Altalabs - Clients'
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
			$axios.$get(`${process.env.baseUrl}/client`),
			$axios.$get(`${process.env.baseUrl}/contact-component`),
			$axios.$get(`${process.env.baseUrl}/footer`)
		]);
		return {
			data: {
				client: data[0],
				contactComponent: data[1],
				footer: data[2]
			}
		};
	}
}
</script>

