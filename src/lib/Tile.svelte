<script>
export let image;
export let name;

</script>
<div>
  <img src={image} alt={name} loading="lazy" />
  <div class="my-2 text-gray-700">
    {name}
  </div>
</div>