<template>
  <div class="podcast">
    <img class="podcast__image" :src="image" :alt="name" />
    <p class="podcast__name">{{ name }}</p>
  </div>
</template>

<script>
export default {
  name: "FuPodcast",

  props: {
    image: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
  },
};
</script>

<style  scoped>
.podcast__image {
  width: 144px;
  height: 164px;
  object-fit: cover;

}

.podcast__name {
  margin: 0;
  margin-top: 4px;
  font-weight: bold;
  font-size: 14px;
}
</style>