<template>
  <div :style="styleObject">
    {{ user.first_name }} {{ user.last_name }} <img width="128" height="128" :src="user.avatar" />
    <!--<div style="width:128px; height:128px" v-bind:style="{ 'background-image': `url(${user.avatar})`}" ></div>-->
  </div>
</template>

<script>
export default {
  name: 'User',
  props: {
    user: Object,
  },
};
</script>

<style></style>
