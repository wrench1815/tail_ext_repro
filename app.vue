<script lang="ts" setup>
function setVH() {
  // true viewport height
  let vh = window.innerHeight * 0.01;
  document.documentElement.style.setProperty('--vh', `${vh}px`);
}

onMounted(() => {
  setVH();
  window.addEventListener('resize', () => {
    setVH();
  });
});
</script>
<template>
  <div>
    <HelloDaisy />
  </div>
</template>
