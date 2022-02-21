<template>
  <div class="uk-overflow-auto">
    <table class="uk-table uk-table-hover uk-table-middle uk-table-divider">
      <thead>
        <tr>
          <th class="uk-table-shrink"></th>
          <th class="uk-table-expand">Name</th>
          <th class="uk-table-shrink">State</th>
          <th class="uk-table-shrink">Quick actions</th>
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
        <tr>
          <td><input class="uk-checkbox" type="checkbox" /></td>
          <td class="uk-text-truncate">Container1</td>
          <td>
            <span class="uk-label uk-label-success">running</span>
          </td>
          <td>
            <a uk-icon="desktop" class="uk-margin-small-right" uk-tooltip="Exec console"></a>
            <a uk-icon="file-text" class="uk-margin-small-right" uk-tooltip="Logs"></a>
            <a uk-icon="info" class="uk-margin-small-right" uk-tooltip="Stats"></a>
            <a uk-icon="search" class="uk-margin-small-right" uk-tooltip="Inspect"></a>
          </td>
          <td class="uk-text-nowrap">Stack2</td>
          <td class="uk-text-nowrap">sample/sample-image1</td>
          <td class="uk-text-nowrap">2022-02-21 18:03</td>
          <td class="uk-text-nowrap">xxx.yyy.zzz.www</td>
          <td class="uk-text-nowrap">manager1</td>
          <td class="uk-text-nowrap">xxxx:yyyy</td>
          <td class="uk-text-nowrap">administrator</td>
        </tr>

        <tr>
          <td><input class="uk-checkbox" type="checkbox" /></td>
          <td class="uk-text-rtuncate">Container2</td>
          <td><span class="uk-label uk-label-warning">STOPPED</span></td>
          <td>
            <span uk-icon="desktop" class="uk-margin-small-right"></span>
            <span uk-icon="file-text" class="uk-margin-small-right"></span>
            <span uk-icon="info" class="uk-margin-small-right"></span>
            <span uk-icon="search"></span>
          </td>
          <td class="uk-text-nowrap">Stack1</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
