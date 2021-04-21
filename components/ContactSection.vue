<template>
    <section class="section section--padded section--dark">
        <div class="section__heading section__heading--centered">
            <h2>{{ data.title }}</h2>
            <div class="section__cta">
                <!-- <a class="btn btn__light border-0" href="/contact.html"></a> -->
                <nuxt-link class="btn btn__light border-0" to="/contact-us">{{ data.call_to_action }}</nuxt-link>
            </div>
        </div>
    </section>
</template>

<script>
export default {
	props: {
		data: {
			type: Object
		}
	}
}
</script>