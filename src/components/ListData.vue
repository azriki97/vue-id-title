<<<<<<< HEAD
=======
<<<<<<< HEAD
<template>
  
    <v-app>
      <v-main>
        <v-card v color="transparent"  class="d-flex justify-center text-center"> 
          <v-btn class="mx-2"  color="#e040fb" @click="formMasuk">
            <v-icon>mdi-plus</v-icon>
          </v-btn>
  
          <v-table class="mt-5 text-center  " hover="true">
            <template v-slot:default>
              <thead>
                <tr class="bg-purple  text-center">
                  <th class="white--text text-center ">judul</th>
                  <th class="white--text text-center ">gambar</th>
                  <th class="white--text text-center w-50">deskripsi</th>
                  <th class="white--text text-center ">kendali</th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="artikel in artikels" :key="artikel.id">
                  <td class="bg-pink">{{ artikel.judul }}</td>
                  <td class="bg-pink"><v-img height="125" v-bind:src="artikel.image" alt="gambar" /></td>
                  <td class="bg-pink">{{ artikel.content }}</td>
                  <td class="bg-pink">
                    <v-btn>
                      <v-icon color="black">mdi-pencil</v-icon>
                    </v-btn>
                    <v-btn>
                      <v-icon color="black">mdi-delete</v-icon>
                    </v-btn>
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
            judul: 'halo del',
            image: 'https://static.wikia.nocookie.net/roshidere/images/b/bf/Alisa_Mikhailovna_Kujo_Bio.png',
            content: '"Pada Kamis (26/10/2023), ruang rapat lantai 3 Institut Teknologi Telkom Surabaya (ITTelkom Surabaya) menjadi panggung dari sebuah peristiwa bersejarah yang akan mengubah wajah pengembangan desa di Indonesia. Hari itu, ITTelkom Surabaya dan Asosiasi Dosen Integrator Desa (ADIDES) merayakan penandatanganan Memorandum of Understanding (MoU) yang memulai perjalanan menuju pengembangan desa yang lebih cerdas dan berkelanjutan di seluruh negeri."'
          },
          {
            id: '2',
            judul: 'halo mas',
            image: 'https://static.wikia.nocookie.net/roshidere/images/b/bf/Alisa_Mikhailovna_Kujo_Bio.png',
            content: '"Pada Kamis (26/10/2023), ruang rapat lantai 3 Institut Teknologi Telkom Surabaya (ITTelkom Surabaya) menjadi panggung dari sebuah peristiwa bersejarah yang akan mengubah wajah pengembangan desa di Indonesia. Hari itu, ITTelkom Surabaya dan Asosiasi Dosen Integrator Desa (ADIDES) merayakan penandatanganan Memorandum of Understanding (MoU) yang memulai perjalanan menuju pengembangan desa yang lebih cerdas dan berkelanjutan di seluruh negeri."'
          },
        ],
       
        }
      },
    }
    
  </script>
  
=======
>>>>>>> c575d9431bc371598cc054588d2906affff078f7
<template>
  <v-app>
    <v-main>
      <v-card color="transparent" class="d-flex justify-center text-center">
        <v-table class="mt-5 text-center">
          <template v-slot:default>
            <thead>
              <tr class="bg-pink-darken-1 text-center">
                <th class="white--text text-center">ID</th>
<<<<<<< HEAD
                <th class="white--text text-center" style="width: 50%;">Title</th>
=======
                <th class="white--text text-center w-50" >Title</th>
>>>>>>> c575d9431bc371598cc054588d2906affff078f7
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
<<<<<<< HEAD
                  <v-text-field v-model="artikel.title" label="Masukkan judul" outlined></v-text-field>
                </td>
                
                <td :style="{ backgroundColor: '#FCE4EC', width: '50%' }">
=======
                  <v-text-field v-model="artikel.Title" label="Masukkan Judul" outlined></v-text-field>
                </td>
                
                <td :style="{ backgroundColor: '#FCE4EC' }">
>>>>>>> c575d9431bc371598cc054588d2906affff078f7
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
<<<<<<< HEAD
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
=======
          Title: 'Halo Dunia ini adalah Program basis antarmuka',
        },
        {
          id: '2',
          NomorID: '1212121212',
          Title: 'Diam - diam aku membuat kelompok untuk skripsi',
        },
        {
          id: '3',
          NomorID: '3434343434',
          Title: 'Kerpibadian aku berubah setelah temanku mengucapkan "1 kata"',
>>>>>>> c575d9431bc371598cc054588d2906affff078f7
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
<<<<<<< HEAD
=======
>>>>>>> 1f735d3 (Tes repo)
>>>>>>> c575d9431bc371598cc054588d2906affff078f7
<<<<<<< HEAD
   
=======
  
>>>>>>> 2e0134acae2b990466a0e2726332fe3fde36de2a
