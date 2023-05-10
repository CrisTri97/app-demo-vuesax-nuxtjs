<template>
  <div class="center">
    <vs-table v-model="selected">
      <template #thead>
        <vs-tr>
          <vs-th>
            <vs-checkbox
              :indeterminate="selected.length == users.length"
              v-model="allCheck"
              @change="selected = $vs.checkAll(selected, users)"
            />
          </vs-th>
          <vs-th> Name </vs-th>
          <vs-th> Email </vs-th>
          <vs-th> Id </vs-th>
        </vs-tr>
      </template>
      <template #tbody>
        <vs-tr
          :key="i"
          v-for="(tr, i) in users"
          :data="tr"
          :is-selected="!!selected.includes(tr)"
        >
          <vs-td checkbox>
            <vs-checkbox :val="tr" v-model="selected" />
          </vs-td>
          <vs-td>
            {{ tr.name }}
          </vs-td>
          <vs-td>
            {{ tr.email }}
          </vs-td>
          <vs-td>
            {{ tr.id }}
          </vs-td>
        </vs-tr>
      </template>
    </vs-table>
    <span class="data">
      <pre>
  {{ selected.length > 0 ? selected : 'Select an item in the table' }}
        </pre
      >
    </span>
  </div>
</template>
<script>
import { users } from '~/mockData/user';
export default {
  data: () => ({
    allCheck: false,
    selected: [],
    users,
  }),
}
</script>
