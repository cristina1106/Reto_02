<template>
  <div id="app">
     <fu-podcast :image="podcast.image_url" :name="podcast.name"/>
    <fu-player
      :name="podcast.name"
      :album="podcast.album"
      :url="podcast.url"
      :image="podcast.image_url"
    />
  </div>
</template>

<script>
import FuPlayer from "./components/FuPlayer";
import FuHeader from "./components/FuHeader";
import FuPodcast from "./components/FuPodcast";

export default {
  name: "App",
  components: {
    FuPlayer,
    FuHeader,
    FuPodcast,
  },

  data() {
    return {
      podcast: {
        name: "US Open Day 14 Preview",
        album: "Courtside: The Official Podcast of the US Open",
        url: "https://audioboom.com/posts/7000554-us-open-day-14-preview.mp3",
        image_url: "https://images.theabcdn.com/i/33251592",
        duration: 1651.04,
      },
    };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
