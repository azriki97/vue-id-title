<template>
  <v-app>
    <v-main>
      <v-card color="transparent" class="d-flex justify-center text-center">
        <v-table class="mt-5 text-center">
          <template v-slot:default>
            <thead>
              <tr class="bg-pink-darken-1 text-center">
                <th class="white--text text-center">ID</th>
                <th class="white--text text-center" style="width: 50%;">Title</th>
                <th class="white--text text-center">Option</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(artikel, index) in artikels" :key="index">
                <td :style="{ backgroundColor: '#F8BBD0' }" v-if="index !== 3">
                  {{ artikel.NomorID }}
                </td>

                <td v-else>
                  <v-text-field v-model="artikel.label" label="Nomor ID" outlined></v-text-field>
                </td>

                <td :style="{ backgroundColor: '#F8BBD0' }" v-if="index !== 3">{{ artikel.Title }}</td>

                <td v-else>
                  <v-text-field v-model="artikel.title" label="Masukkan judul" outlined></v-text-field>
                </td>
                
                <td :style="{ backgroundColor: '#FCE4EC', width: '50%' }">
                  <template v-if="index !== 3">
                    <v-btn>
                      <v-icon>mdi-pencil</v-icon>
                    </v-btn>
                    <v-btn>
                      <v-icon>mdi-delete</v-icon>
                    </v-btn>
                  </template>
                  <template v-else>
                    <v-btn @click="addRow">
                      <v-icon>mdi-plus</v-icon>
                    </v-btn>
                  </template>
                </td>
              </tr>
            </tbody>
          </template>
        </v-table>
      </v-card>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'ListData',
  data() {
    return {
      artikels: [
        {
          id: '1',
          NomorID: '1234567890',
          Title: 'Pedagang jual sayur yang berwarna hijau',
        },
        {
          id: '2',
          NomorID: '1111111111',
          Title: 'Kejar T-rex membuatku kaki semakin buff speed',
        },
        {
          id: '3',
          NomorID: '2222222222',
          Title: 'Minuman ini membuatku semakin terbuka pikirannya',
        },
        {
          id: '4',
          NomorID: '',
          Title: '',
        },
      ],
    };
  },
  methods: {
    addRow() {
      // Logic to add a new row
    },
  },
};
</script>
