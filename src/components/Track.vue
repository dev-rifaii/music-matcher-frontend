<template>
  <div class="card" style="width: 10rem">
    <img
      :src="track.imageUrl"
      @error="
        $event.target.src =
          'https://static.thenounproject.com/png/82455-200.png'
      "
      width="100"
      height="100"
    />
    <div class="card-body">
      <a :href="track.href" style="text-decoration: none">{{ track.name }}</a>
    </div>
  </div>
</template>


<script>
export default {
  name: "Track",
  props: {
    track: Object,
  },
};
</script>

<style>
.card {
  display: inline-block;
}
</style>