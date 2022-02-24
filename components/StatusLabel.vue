<script setup lang="ts">
const props = defineProps({
  status: String,
});

const labelStates = {
  running: "success",
  stopped: "warning",
};

const labelStatus = labelStates[props.status];
</script>

<template>
  <span class="uk-label" :class="'uk-label-' + labelStatus">{{
    props.status
  }}</span>
</template>
