<script setup lang="ts">
import UIkit from "uikit";

onMounted(() => {
  window.addEventListener("offline", function (e) {
    UIkit.notification({
      message: "Network: offline",
      status: "warning",
      pos: "top-right",
    });
  });

  window.addEventListener("online", function (e) {
    UIkit.notification({
      message: "Network: online",
      status: "primary",
      pos: "top-right",
    });
  });
});
</script>

<template></template>
