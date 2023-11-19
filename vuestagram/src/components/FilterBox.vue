<template>
    <div :class="`${filter} filter-item`" :style="`background-image:url(${URL})`">
        <slot></slot>
    </div> 
</template>

<script>
export default {
    name : "FilterBox",
    props : {
        URL : String,
        filter : String,
    },
}
</script>

<style>
.filter-item {
  width: 100px;
  height: 100px;
  margin: 10px 10px 10px auto;
  padding: 8px;
  display: inline-block;
  color : black;
  background-size: cover;
  background-position : center;
}
</style>