<template>
  <div>
    <PostBox v-for="(item, index) in Posting" :key="index" :Posting="item" />
  </div>
</template>

<script>
import PostBox from './PostBox.vue';

export default {
    name : "ContainerBox",
    components : {
      PostBox,
    },
    props: {
      Posting : Array,
    },
}
</script>

<style>

</style>