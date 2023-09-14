<template>
  <div class="footer">
    <div class="copyright">
      Copyright © 2023 RESTJob, Inc All rights reserved.
    </div>
    <div class="developer">Developed by {{ developerName }}</div>
  </div>
</template>

<script>
export default {
  props: {
    developerName: String,
  },
};
</script>

<style scoped>
.footer {
  text-align: center;
  background-color: #f0f0f0;
  padding: 16px;
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
}

.copyright {
  font-size: 12px;
  color: #333;
}

.developer {
  font-size: 12px;
  color: #555;
}
</style>