<template>
  <div class="my-list" id="my-list">
    <div class="title">{{ title }}</div>
    <div style="background-color:#F99634; padding-left: 2em;">
      <slot  name="subtitle"></slot>
    </div>
    <div class="list">
      <div class="list-item" v-for="item in items">
        <slot v-bind="item"></slot>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: 'my-list',
        props:[ 'title', 'items' ]
    }
</script>

<style lang="scss" scoped>
  .my-list {
    flex: 1 1 50%;
    font-family: Arial;
    color: white;
    $padding: 20px;
    $radius: 4px;
    margin: 20px;
    .title {
      background: #F99634;
      padding: $padding;
      font-weight: bold;
      font-size: 22px;
      border-top-left-radius: $radius;
      border-top-right-radius: $radius;
    }
    .list {
      background: #321800;
      padding: $padding;
      font-size: 16px;
      border-bottom-left-radius: $radius;
      border-bottom-right-radius: $radius;
    }
    .list-item:not(:last-child) {
      padding-bottom: $padding;
    }
  }
</style>
