<script>
  import Saos from "saos";
  import Scroller from '@sveltejs/svelte-scroller';

  let top = 0.2
	let threshold = 0.5;
	let bottom = 0.9;
  let index, offset, progress, count;
</script>

<div class="h-full w-5/6 flex-col justify-center items-center space-y-56 m-10">
  <h1 class="h1 lg:h-28 sm:h-full text-center font-extrabold gradient-heading-2 lg:text-8xl md:text-4xl m-10">
    Projects
  </h1>
  <Scroller
		{top}
		{threshold}
		{bottom}
    bind:index
    bind:offset 
    bind:progress
    bind:count
	>
		<div slot="background">
			<p>current section: <strong>TEST</strong></p>

			<p>offset in current section</p>

			<p>total progress</p>
		</div>

		<div slot="foreground" class="space-y-56" style="padding: 0 0 0 50%;">
			<section>section 1</section>
			<section>section 2</section>
			<section>section 3</section>
			<section>section 4</section>
			<section>section 5</section>
		</div>
	</Scroller>
  <Saos 
      animation={'puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both'}
      animation_out={'slide-out-fwd-center 0.7s cubic-bezier(0.550, 0.085, 0.680, 0.530) both'}
  >
      <div><p>animation: from-left</p></div>
  </Saos>

  <Saos 
      animation={'puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both'}
      animation_out={'slide-out-fwd-center 0.7s cubic-bezier(0.550, 0.085, 0.680, 0.530) both'}
  >
      <div><p>animation: from-left</p></div>
  </Saos>

  <Saos 
      animation={'puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both'}
      animation_out={'slide-out-fwd-center 0.7s cubic-bezier(0.550, 0.085, 0.680, 0.530) both'}
  >
      <div><p>animation: from-left</p></div>
  </Saos>

  <Saos 
      animation={'puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both'}
      animation_out={'slide-out-fwd-center 0.7s cubic-bezier(0.550, 0.085, 0.680, 0.530) both'}
  >
      <div><p>animation: from-left</p></div>
  </Saos>

  <Saos 
      animation={'puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both'}
      animation_out={'slide-out-fwd-center 0.7s cubic-bezier(0.550, 0.085, 0.680, 0.530) both'}
  >
      <div><p>animation: from-left</p></div>
  </Saos>

  <Saos 
      animation={'puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both'}
      animation_out={'slide-out-fwd-center 0.7s cubic-bezier(0.550, 0.085, 0.680, 0.530) both'}
  >
      <div><p>animation: from-left</p></div>
  </Saos>

  <Saos 
      animation={'puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both'}
      animation_out={'slide-out-fwd-center 0.7s cubic-bezier(0.550, 0.085, 0.680, 0.530) both'}
  >
      <div><p>animation: from-left</p></div>
  </Saos>

  <Saos 
      animation={'puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both'}
      animation_out={'slide-out-fwd-center 0.7s cubic-bezier(0.550, 0.085, 0.680, 0.530) both'}
  >
      <div><p>animation: from-left</p></div>
  </Saos>
</div>
<style>
   @keyframes -global-puff-in-center {
    0% {
      transform: scale(2);
      filter: blur(4px);
      opacity: 0;
    }
    100% {
      transform: scale(1);
      filter: blur(0px);
      opacity: 1;
    }
  }
  @keyframes -global-slide-out-fwd-center {
    0% {
      transform: translateZ(1);
      opacity: 1;
    }
    100% {
      transform: translateZ(600px);
      opacity: 0;
    }
  }

	[slot="background"] {
		background-color: rgba(255,62,0,0.05);
		border-top: 2px solid #ff3e00;
		border-bottom: 2px solid #ff3e00;
		font-size: 1.4em;
		overflow: hidden;
		padding: 1em;
	}
	
	[slot="background"] p {
		margin: 0;
	}
	
	[slot="foreground"] {
		pointer-events: none;
	}
	
	[slot="foreground"] section {
		pointer-events: all;
	}
	
	section {
		height: 80vh;
		background-color: rgba(0,0,0,0.5);
		color: white;
		padding: 1em;
		margin: 0 0 2em 0;
	}
</style>