<template>
    <main class="main" role="main">
			<section class="section section--greyed hero hero--mapped">
				<div class="container">
					<div class="hero__body">
						<h1 class="hero__title">{{ data.ContactMainBanner.title }}</h1>
						<p class="section__caption">
							{{ data.ContactMainBanner.description }}
						</p>
					</div>
				</div>
			</section>

			<section class="section">
				<div class="form__card">
					<form  @submit.prevent="addFormData">
						<div
							class="alert alert-success text-center"
							v-if="isSuccess"
						>
							<button
								type="button" class="close" aria-label="Close"  data-dismiss="alert"
								@click="isSuccess = !isSuccess"
							>
								<span aria-hidden="true">&times;</span>
							</button>
							{{ data.ContactFormResponse.success }}
						</div>
						<div
							class="alert alert-danger text-center"
							v-if="isError"
						>
							<button
								type="button" class="close" aria-label="Close"  data-dismiss="alert"
								@click="isError = !isError"
							>
								<span aria-hidden="true">&times;</span>
							</button>
							{{ data.ContactFormResponse.error}}
						</div>
						<div class="form-group">
							<div class="form-row">
								<div class="col-md-6">
									<label for="name">{{ data.ContactForm.first }}</label>
									<input type="text" class="form-control" id="name"
										v-model="formData.first"
									>
								</div>
								<div class="col-md-6">
									<label for="name">{{ data.ContactForm.second }}</label>
									<input type="text" class="form-control" id="name"
										v-model="formData.second"
									>
								</div>
							</div>
						</div>
						<div class="form-group">
							<div class="form-row">
								<div class="col-md-6">
									<label for="name">{{ data.ContactForm.third }}</label>
									<input type="text" class="form-control" id="name"
									 v-model="formData.third"
									>
								</div>
								<div class="col-md-6">
									<label for="name">{{ data.ContactForm.fourth }}</label>
									<input type="text" class="form-control" id="name"
									 v-model="formData.fourth"
									>
								</div>
							</div>
						</div>
						<div class="form-group">
							<label for="name">{{ data.ContactForm.fifth }}</label>
							<input type="text" class="form-control" id="name"
							 v-model="formData.fifth"
							>
						</div>
						<div class="form-group">
							<label for="name"> {{ data.ContactForm.sixth }}</label>
							<input type="text" class="form-control" id="name"
							 v-model="formData.sixth"
							>
						</div>
						<div class="form-group">
							<label for="name">{{ data.ContactForm.seventh }}</label>
							<input type="text" class="form-control" id="name" v-model="formData.seventh">
						</div>
						<div class="form-group">
							<label for="name">{{ data.ContactForm.eighth }}</label>
							<input type="text" class="form-control" id="name" v-model="formData.eighth">
						</div>
						<div class="form-group">
							<label for="name">{{ data.ContactForm.ninth }}</label>
							<input type="text" class="form-control" id="name" v-model="formData.ninth">
						</div>
						<div class="form-group">
							<label for="name">{{ data.ContactForm.tenth }}</label>
							<input type="text" class="form-control" id="name" v-model="formData.tenth">
						</div>
						<div class="form-group">
							<label for="name">{{ data.ContactForm.eleventh }}</label>
							<input type="text" class="form-control" id="name" v-model="formData.eleventh">
						</div>
						<div class="form-group">
							<label for="name">{{ data.ContactForm.twelveth }}</label>
							<input type="text" class="form-control" id="name" v-model="formData.twelveth">
						</div>
						<div class="form-group">
							<label for="name">{{ data.ContactForm.thirteenth }}</label>
							<input type="text" class="form-control" id="name" v-model="formData.thirteenth">
						</div>
						<div class="form-group">
							<label for="name">{{ data.ContactForm.fourteenth }}</label>
							<input type="text" class="form-control" id="name" v-model="formData.fourteenth">
						</div>
						<div class="form-group">
							<label for="name">{{ data.ContactForm.fifteenth }}</label>
							<input type="text" class="form-control" id="name" v-model="formData.fifteenth">
						</div>
						<div class="form-group">
							<button
								class="btn btn__primary" type="submit"
								:style="{
									'cursor': !isSubmit ? 'not-allowed' : 'pointer'
								}"
							>
								{{ data.ContactForm.call_to_action }} 
								<svg width="18" height="13" fill="none" xmlns="http://www.w3.org/2000/svg">
									<path d="M2 6.5h14m0 0L11.6 2M16 6.5L11.6 11" stroke="#fff" stroke-width="2.977" stroke-linecap="round" stroke-linejoin="round"/>
								</svg>
							</button>
						</div>
					</form>
				</div>
			</section>
		</main>
</template>


<script>
export default {
	props: {
		data: {
			type: Object
		}
	},
	data() {
		return {
			formData: {},
			isSuccess: false,
			isError: false
		}
	},
	computed: {
		isSubmit() {
			return  Object.values(this.formData).length > 14;
		}
	},
	methods: {
		addFormData() {
			return this.$axios.post(`${process.env.NUXT_APP_API_URL}/contact-forms`, this.formData)
				.then((res) => {
					this.formData = {};
					this.isSuccess = true;
					return true;
				})
				.catch((err) => {
					this.isError = true;
					return err;
				});
		}
	}
}
</script>