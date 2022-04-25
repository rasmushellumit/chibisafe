<template>
	<!-- eslint-disable max-len -->
	<div class="container has-text-left">
		<h2 class="subtitle">
			What is chibisafe?
		</h2>
		<article class="message">
			<div class="message-body">
				chibisafe is an easy to use, open source and completely free file upload service. It accepts your files, photos, documents, anything, and gives you back a shareable link for you to send to others.
			</div>
		</article>

		<h2 class="subtitle">
			Can I run my own chibisafe?
		</h2>
		<article class="message">
			<div class="message-body">
				Definitely. Head to <a target="_blank" href="https://github.com/rapphy243/chibisafe"></a> and follow the instructions to build and deploy it by yourself.
			</div>
		</article>
		
		<h2 class="subtitle">
			What are albums?
		</h2>
		<article class="message">
			<div class="message-body">
				Albums are a simple way of sorting uploads together. Right now you can create albums through the dashboard and use them only with <a target="_blank" href="https://chrome.google.com/webstore/detail/lolisafe-uploader/enkkmplljfjppcdaancckgilmgoiofnj">our chrome extension</a> which will enable you to <strong>right click -&gt; send to chibisafe</strong> or to a desired album if you have any.
			</div>
		</article>

		<h2 class="subtitle">
			Why should I use this?
		</h2>
		<article class="message">
			<div class="message-body">
				There are too many file upload services out there, and a lot of them rely on the foundations of pomf which is ancient. In a desperate and unsuccessful attempt of finding a good file uploader that's easily extendable, chibisafe was born. We give you control over your files, we give you a way to sort your uploads into albums for ease of access and we give you an api to use with ShareX or any other thing that let's you make POST requests.
			</div>
		</article>
		
			<h2 class="subtitle">
			Who is Rapphy243?
		</h2>
		<article class="message">
			<div class="message-body">
				I'm some random on the internet who decided to tried to edit and understand code with no prior coding knowledge. Headover to my website to learn more.  
			</div>
		</article>
	</div>
</template>

<script>
export default {
	name: 'Faq',
	data() {
		return {};
	},
	head() {
		return {
			title: 'FAQ'
		};
	}
};
</script>

<style lang="scss" scoped>
	@import '~/assets/styles/_colors.scss';
	article.message { background-color: #ffffff; }
</style>
