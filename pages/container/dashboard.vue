<script setup>
const items = [
  {
    logo: "thumbnails",
    title: "Stacks",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna lliqua.",
    to: "/container/containers",
  },
  {
    logo: "list",
    title: "Service",
    description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
    to: "#",
  },
  {
    logo: "nut",
    title: "Container",
    description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
    to: "/container/containers",
  },
  {
    logo: "image",
    title: "Images",
    description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
    to: "#",
  },
  {
    logo: "database",
    title: "Volumes",
    description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
    to: "#",
  },
  {
    logo: "server",
    title: "Networks",
    description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
    to: "#",
  },
];
</script>

<template>
  <div
    uk-grid
    class="
      uk-child-width-1-1@s
      uk-child-width-1-1@m
      uk-child-width-1-2@l
      uk-child-width-1-3@xl
      uk-grid-small
      uk-grid-match
    "
  >
    <div v-for="(item, index) in items" :key="index">
      <div class="uk-card uk-card-default uk-card-body uk-card-hover">
        <NuxtLink :to="item.to" class="uk-link-reset">
          <div uk-grid class="uk-grid-small uk-flex-middle">
            <div class="uk-width-auto">
              <span :uk-icon="'icon: ' + item.logo + ';' + 'ratio: 2;'"></span>
            </div>
            <div class="uk-width-expand">
              <h3 class="uk-card-title">{{ item.title }}</h3>
            </div>
          </div>
        </NuxtLink>
        <p>{{ item.description }}</p>
      </div>
    </div>
  </div>
</template>
