<script>
    import Saos from "saos";
</script>

<div class="h-full w-5/6 flex-col justify-center items-center space-y-56 m-10">
  <h1 class="h1 lg:h-28 sm:h-full text-center font-extrabold gradient-heading-2 lg:text-8xl md:text-4xl m-10">
    Projects
  </h1>
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
</style>