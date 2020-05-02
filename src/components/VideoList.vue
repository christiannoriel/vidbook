<template>
  <ul class="list-group col-md-4">
    <VideoListItem
      :video="video"
      :key="video.etag"
      v-for="video in videos"
      @videoSelect="onVideoSelect"
    ></VideoListItem>
  </ul>
</template>

<script>
import VideoListItem from "./VideoListItem";
export default {
  name: "VideoList",
  props: ["videos"],
  components: {
    VideoListItem
  },
  methods: {
    onVideoSelect(video) {
      this.$emit("videoSelect", video);
    }
  }
};
</script>
<style>
</style> 