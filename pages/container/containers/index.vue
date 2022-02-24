<script setup lang="ts">
const containerItems = [
  {
    id: "asdfasdf1",
    name: "Container1",
    status: "running",
    stack: "Stack1",
    image: "sample/sample-image1",
    created: "2022-02-21 18:03",
    ip_address: "xxx.yyy.zzz.www",
    host: "manager1",
    published_ports: "xxxx:yyyy",
    owenership: "administrator",
  },
  {
    id: "asdfasdf2",
    name: "Container2",
    status: "stopped",
    stack: "Stack2",
    image: "sample/sample-image2",
    created: "2022-02-22 12:00",
    ip_address: "xxx.yyy.zzz.www",
    host: "manager2",
    published_ports: "xxxx:yyyy",
    ownership: "administrator",
  },
];
</script>

<template>
  <div class="uk-overflow-auto">
    {{ $route.path }}
    <table class="uk-table uk-table-hover uk-table-middle uk-table-divider">
      <thead>
        <tr>
          <th class="uk-table-shrink"></th>
          <th class="uk-table-expand">Name</th>
          <th class="uk-table-shrink">State</th>
          <th class="uk-table-shrink">Stack</th>
          <th class="uk-table-shrink">Image</th>
          <th class="uk-table-shrink">Created</th>
          <th class="uk-table-shrink">IP Address</th>
          <th class="uk-table-shrink">Host</th>
          <th class="uk-table-shrink">Published Ports</th>
          <th class="uk-table-shrink">Ownership</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item, index) in containerItems" :key="index">
          <td><input class="uk-checkbox" type="checkbox" /></td>
          <td class="uk-table-link uk-text-truncate">
            <NuxtLink :to="`/container/containers/${item.id}`" class="">{{
              item.name
            }}</NuxtLink>
          </td>
          <td>
            <!-- <span class="uk-label uk-label-success">{{ item.status }}</span> -->
            <status-label :status="item.status"></status-label>
          </td>
          <!-- <td>
            <a uk-icon="desktop" class="uk-margin-small-right" uk-tooltip="Exec console"></a>
            <a uk-icon="file-text" class="uk-margin-small-right" uk-tooltip="Logs"></a>
            <a uk-icon="info" class="uk-margin-small-right" uk-tooltip="Stats"></a>
            <a uk-icon="search" class="uk-margin-small-right" uk-tooltip="Inspect"></a>
          </td> -->
          <td class="uk-text-nowrap">{{ item.stack }}</td>
          <td class="uk-text-nowrap">
            <NuxtLink to="#" class="">{{ item.image }}</NuxtLink>
          </td>
          <td class="uk-text-nowrap">{{ item.created }}</td>
          <td class="uk-text-nowrap">{{ item.ip_address }}</td>
          <td class="uk-text-nowrap">{{ item.host }}</td>
          <td class="uk-text-nowrap">{{ item.published_ports }}</td>
          <td class="uk-text-nowrap">{{ item.ownership }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
