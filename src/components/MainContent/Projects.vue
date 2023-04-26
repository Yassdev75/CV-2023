<template>
  <div class="d-flex">
    <div class="about-description">
      <h2 class="numbered-heading mb-5">A propos de moi</h2>
    </div>
  </div>
</template>
<script>
export default {

}
</script>
<style>
.numbered-heading::after {
  content: "";
  display: inline-block;
  position: relative;
  top: -8px;
  width: 200px;
  height: 1px;
  margin-left: 20px;
  background-color: #000000;
}
</style>