<template>
	<div class="links">
		<a
			href="https://hellum.it"
			target="_blank"
			class="link">
			<header class="bd-footer-star-header">
				<h4 class="bd-footer-title">hellum.it</h4>
				<p class="bd-footer-subtitle">hellums website😁</p>
			</header>
		</a>
		<a
			href="https://github.com/rasmushellumit/chibisafe"
			target="_blank"
			class="link">
			<header class="bd-footer-star-header">
			<h4 class="bd-footer-title">Github</h4>
			<p class="bd-footer-subtitle">Deploy your own Chibisafe</p>
		</a>
		<div
			v-if="loggedIn"
			class="link"
			@click="createShareXThing">
			<header class="bd-footer-star-header">
				<h4 class="bd-footer-title">
					ShareX
				</h4>
				<p class="bd-footer-subtitle">
					Upload from your Desktop
				</p>
			</header>
		</div>
		<router-link
			to="/faq"
			class="link">
			<header class="bd-footer-star-header">
				<h4 class="bd-footer-title">
					FAQ
				</h4>
				<p class="bd-footer-subtitle">
					We got you covered
				</p>
			</header>
		</router-link>
	</div>
</template>
<script>
import { mapGetters } from 'vuex';
import { saveAs } from 'file-saver';

export default {
	computed: {
		...mapGetters({
			loggedIn: 'auth/isLoggedIn',
			apiKey: 'auth/getApiKey'
		})
	},
	methods: {
		createShareXThing() {
			const sharexFile = `{
				"Name": "${this.$store.state.config.serviceName}",
				"DestinationType": "ImageUploader, FileUploader",
				"RequestType": "POST",
				"RequestURL": "${location.origin}/api/upload",
				"FileFormName": "files[]",
				"Headers": {
					"token": "${this.apiKey}",
					"accept": "application/vnd.chibisafe.json"
				},
				"ResponseType": "Text",
				"URL": "$json:url$",
				"ThumbnailURL": "$json:thumb$"
			}`;
			const sharexBlob = new Blob([sharexFile], { type: 'application/octet-binary' });
			saveAs(sharexBlob, `${location.hostname}.sxcu`);
		}
	}
};
</script>
<style lang="scss" scoped>
	@import '~/assets/styles/_colors.scss';
	.links {
		margin: 7rem 0 3rem 0;
		align-items: stretch;
		display: flex;
		justify-content: space-between;

		div.link { cursor: pointer; }
		.link {
			background: #0000002e;
			border: 1px solid #00000061;
			display: block;
			width: calc(25% - 2rem);
			border-radius: 6px;
			box-shadow: 0 1.5rem 1.5rem -1.25rem rgba(10,10,10,.05);
			transition-duration: 86ms;
			transition-property: box-shadow,-webkit-transform;
			transition-property: box-shadow,transform;
			transition-property: box-shadow,transform,-webkit-transform;
			will-change: box-shadow,transform;

			header.bd-footer-star-header {
				padding: 1.5rem;

				&:hover .bd-footer-subtitle { color: $textColorHighlight; }

				h4.bd-footer-title {
					color: $textColorHighlight;
					font-size: 1.5rem;
					line-height: 1.25;
					margin-bottom: .5rem;
					transition-duration: 86ms;
					transition-property: color;
					font-weight: 700;
				}

				p.bd-footer-subtitle {
					color: $textColor;
					margin-top: -.5rem;
					transition-duration: 86ms;
					transition-property: color;
					font-weight: 400;
				}
			}

			&:hover {
				box-shadow: 0 3rem 3rem -1.25rem rgba(10,10,10,.1);
				transform: translateY(-.5rem);
			}
		}
	}

	@media screen and (max-width: 768px) {
		.links {
			display: block;
			padding: 0px 2em;
			.link {
				width: 100%;
				margin-bottom: 1.5em;
			}
		}
	}
</style>
