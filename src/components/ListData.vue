<template>
  <v-app>
    <v-main>
      <v-card color="transparent" class="d-flex justify-center text-center">
        <v-table class="mt-6 text-center">
          <template v-slot:default>
            <thead>
              <tr class="bg-pink-darken-1 text-center">
                <th class="white--text text-center">ID</th>
                <th class="white--text text-center" style="width: 20%;">Title</th>
                <th class="white--text text-center" style="width: 30%;">Deskripsi</th>
                <th class="white--text text-center">Option</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(artikel, index) in artikels" :key="index">

                <!-- Detail ID -->
                <td :style="{ backgroundColor: '#F8BBD0' }" v-if="index !== 5">
                  {{ artikel.NomorID }}
                </td>

                <!-- input ID -->
                <td v-else>
                  <v-text-field v-model="artikel.label" label="Nomor ID" outlined></v-text-field>
                </td>

                <!-- Detail title -->
                <td :style="{ backgroundColor: '#F8BBD0' }" v-if="index !== 5">{{ artikel.Title }}</td>

                <!-- input title -->
                <td v-else>
                  <v-text-field v-model="artikel.title" label="Masukkan judul" outlined></v-text-field>
                </td>

                <!-- Detail Deskripsi -->
                <td :style="{ backgroundColor: '#F8BBD0' }" v-if="index !== 5">{{ artikel.Desc }}</td>

                <!-- input Deskripsi -->
                <td v-else>
                  <v-text-field v-model="artikel.Desc" label="Isi Deskripsi" outlined></v-text-field>
                </td>
                
                <td :style="{ backgroundColor: '#FCE4EC', width: '50%' }">
                  <template v-if="index !== 5">
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
          Title: 'Perut manusia membesar sebesar telor naga setelah memakan harta anak yatim piatu semasa di dunia',
          Desc: 'Cerita ini tentang seorang manusia ketika semasa hidup di dunia diberi titipan rezeki untuk anak yatim piatu, namun ia mengabaikan untuk membeli rubicon dan pajero dan pada akhirnya anak tersebut mati kelaparan',
        },
        {
          id: '2',
          NomorID: '1111111111',
          Title: 'Kejar T-rex membuatku kakiku bertambah kecepatan berlari',
          Desc: 'Alur cerita ini ketika seseorang tersesat di hutan untuk menyelamatkan diri justru ia menemukan T-Rex jinak yang ia kejar untuk berburu, karena saking cepatnya ia harus berlatih lari cepat',
        },
        {
          id: '3',
          NomorID: '2222222222',
          Title: 'Minuman ini membuatku semakin terbuka pikirannya',
          Desc: 'Ketika seseorang membeli minuman yang salah, seharusnya untuk meracuni orang yang ia sayangi namun diminum kepada orang yang salah sehingga memicu keinginan untuk serba terbuka pikirannya',
        },
        {
          id: '4',
          NomorID: '3333333333',
          Title: 'Prestasiku bertambah setelah mendatangi negara yang aku datangi',
          Desc: 'Mengikuti dan lolos beasiswa itu merupakan hal yang menyenangkan lebih lagi dibiyayai full beasiswa',
        },
        {
          id: '5',
          NomorID: '4444444444',
          Title: 'Aku bereinkarnasi menjadi ahli sihir yang ganteng saat aku berpindah semesta',
          Desc: 'Cerita ini berisi tentans seseorang yang ingin menjadi penyihir anggun dan ganteng, namun ia mati dalam keadaan tragis sehingga berinkarnasi menjadi penyihir yang ia impikan selama ini',
        },
        {
          id: '6',
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
