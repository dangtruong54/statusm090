<template>
  <div class="item-post">
    <h4>Title item post</h4>
    <p>It’s sometimes useful to emit a specific value with an event. For example, we may want the
      component to be in charge of how much to enlarge the text by. In those cases, we can use $emit‘s 2nd parameter to provide this value:</p>
    <a href="#" @click="statusElement(checkShow)">Detail post</a>
    <div v-if="checkShow" class="More-detail">
      <p>It’s sometimes useful to emit a specific value with an event. For example, we may want the
        component to be in charge of how much to enlarge the text by</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: "ItemPost",
    props: {
      checkShow: {
        type: Boolean
      },
      title: {
        type: String
      }
    },
    methods: {
      statusElement(checkShow) {
        checkShow = !checkShow
        this.$emit('currentClick', checkShow)
        this.$emit('update:title', "Tieu de post")
      }
    }
  }
</script>

<style scoped>
  .item-post p {
    max-width: 1100px;
    margin: 0 auto;
  }
</style>