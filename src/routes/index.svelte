<script lang="ts">
	import Slideshow from '$lib/Slideshow.svelte';
	import InlineSVG from 'svelte-inline-svg'

  // https://ionicons.com/
	let socialMedia = [
		{
			name: 'Twitter',
			image: '/images/logo-twitter.svg',
			link: 'https://twitter.com/goodstardemo'
		},
		{
			name: 'Facebook',
			image: '/images/logo-facebook.svg',
			link: 'https://www.facebook.com/goodstardemolition'
		},
		{
			name: 'Instagram',
			image: '/images/logo-instagram.svg',
			link: 'https://www.instagram.com/goodstardemolition'
		},
		{
			name: 'LinkedIn',
			image: '/images/logo-linkedin.svg',
			link: 'https://www.linkedin.com/company/goodstardemolition'
		},
		{
			name: 'Email',
			image: '/images/mail-outline.svg',
			link: 'mailto:ryan@goodstardemolition.com'
		},
	];
</script>

<main>
	<Slideshow />

	<div class="bg-gray-600 py-24">
		<img src="/images/goodstar-logo.png" class="m-auto mb-3" alt="Goodstar"/>
		<div class="mb-2 text-gray-300 text-center">
			<span class="font-bold">
				OKC
			</span> | 
			Demolition & Disaster Recovery
		</div>
		<div class="flex justify-center ">
			{#each socialMedia as social}
				<div>
					<a href={social.link} class="stroke-current fill-current bg-gray-300 text-gray-300">
						<InlineSVG class="w-8 h-8 mx-2" src={social.image} />
					</a>
				</div>
			{/each}
		</div>
	</div>
</main>

<style>
</style>
