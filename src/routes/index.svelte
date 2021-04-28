<script lang="ts">
  import Storm from '$lib/Storm.svelte';
  import InlineSVG from 'svelte-inline-svg';
  import Tile from '$lib/Tile.svelte';

  // https://ionicons.com/
  let socialMedia = [
    {
      name: 'Twitter',
      image: '/images/logo-twitter.svg',
      link: 'https://twitter.com/goodstarventure'
    },
    {
      name: 'Facebook',
      image: '/images/logo-facebook.svg',
      link: 'https://www.facebook.com/goodstardemolition'
    },
    {
      name: 'Instagram',
      image: '/images/logo-instagram.svg',
      link: 'https://www.instagram.com/goodstarventures'
    },
    {
      name: 'LinkedIn',
      image: '/images/logo-linkedin.svg',
      link: 'https://www.linkedin.com/company/goodstardemolition'
    },
    {
      name: 'Email',
      image: '/images/mail-outline.svg',
      link: 'mailto:ryan@goodstarventures.com'
    }
  ];

	let ventures = [
    {
      name: 'Disaster Recovery',
      image: '/images/tiles/snow@0.5x.jpg',
      link: 'https://goodstardemolition.com',
			description: "blah blahsdlfkja sdlfkjasdfalsd asdflkajsdflaskjdf aklsdjf asldkfj asdlkfjasdlkfjaslkdfj"
    },
    {
      name: 'Goodstar Demolition',
      image: '/images/tiles/demo@0.75x.jpg',
      link: 'https://goodstardemolition.com',
			description: "blah blahsdlfkja sdlfkjasdfalsd asdflkajsdflaskjdf aklsdjf asldkfj asdlkfjasdlkfjaslkdfj"
    },
    {
      name: 'Goodstar Tree Service',
      image: '/images/tiles/tree@0.75x.jpg',
      link: 'https://goodstardemolition.com',
			description: "blah blahsdlfkja sdlfkjasdfalsd asdflkajsdflaskjdf aklsdjf asldkfj asdlkfjasdlkfjaslkdfj"
    },
    {
      name: 'Signature Inspections',
      image: '/images/tiles/sig@0.75x.jpg',
      link: 'https://goodstardemolition.com',
			description: "blah blahsdlfkja sdlfkjasdfalsd asdflkajsdflaskjdf aklsdjf asldkfj asdlkfjasdlkfjaslkdfj"
    },
    {
      name: 'Goodstar Construction',
      image: '/images/tiles/construction@0.75x.jpg',
      link: 'https://goodstardemolition.com',
			description: "blah blahsdlfkja sdlfkjasdfalsd asdflkajsdflaskjdf aklsdjf asldkfj asdlkfjasdlkfjaslkdfj"
    },
	];
  // be more handy
  // Disaster times
</script>

<main>
  <div class="relative">
    <Storm />
    <div class="flex p-6">
      <div class="flex-grow">
        <div style="max-width: 170px;">
          <img class="my-4 max-w-full" src="/images/GOODSTARVENTURES.png" alt="Goodstar Ventures" />
        </div>
      </div>

      <div class="flex justify-center ">
        {#each socialMedia as social}
          <div class="my-4">
            <a href={social.link} class="stroke-current fill-current bg-gray-300 text-gray-300">
              <InlineSVG class="w-6 h-6 mx-2" src={social.image} />
            </a>
          </div>
        {/each}
      </div>
    </div>
    <div class="py-44">
      <div class="mb-2 text-gray-300 text-center text-4xl leading-relaxed">
        Starting local buisnesses to <br />fight global disasters
      </div>
    </div>
  </div>
	<div class="m-auto max-w-7xl text-2xl text-gray-400 p-6">
		Current ventures
	</div>
  <div class="grid xl:grid-cols-3 md:grid-cols-2 gap-4 max-w-7xl m-auto p-6">
    {#each ventures as venture}
      <Tile
        image={venture.image || "https://images.unsplash.com/photo-1619359037135-4d8b70426833?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2550&q=80"}
        name={venture.name}
      />
    {/each}
  </div>
</main>

<style>
</style>
