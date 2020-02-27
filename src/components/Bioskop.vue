<template>
  <div id="ListBioskop">
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand" href="#">Navbar</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
            <li class="nav-item active">
                <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="#">Link</a>
            </li>
            <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                Dropdown
                </a>
                <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                <a class="dropdown-item" href="#">Action</a>
                <a class="dropdown-item" href="#">Another action</a>
                <div class="dropdown-divider"></div>
                <a class="dropdown-item" href="#">Something else here</a>
                </div>
            </li>
            <li class="nav-item">
                <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
            </li>
            </ul>
            <form class="form-inline my-2 my-lg-0">
            <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
            <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
            </form>
        </div>
      </nav>

      <div class="judulTabel">
          <!-- <h2>Daftar List Tugas</h2> -->
          <div class="jumbotron">
            <h1 class="display-4">Assignment List</h1>
            <p class="lead"><i>"Kemenangan itu manja, harus direbut dengan perjuangan yang keras"</i></p>
            <p class="lead">dr Gamal Albinsaid, M.Biomed.</p>
            <hr class="my-4">
            <a class="btn btn-primary btn-lg" href="#mulai" role="button">Get Started</a>
        </div>
      </div>
      <br>
      <div class="btnTambah" id="mulai">
          <br>
          <div class="container">
          <button class="btn btn-success" mt-5 mb-5 @click="tambahkan">Tambahkan Tugas</button>
          <!-- <button @click="showAlert">Hello world</button> -->
          <!-- <button @click="destroy(statuses.id)" class="btn btn-danger btn-flat btn-sm"> <i class="fa fa-remove"></i> </button> -->
          </div>
      </div>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import LembarTengah from './components/HelloWorld.vue'
export default {
  name: 'tampilkanList',
  components: {

  },
  data () {
    return {
      allData: [
        {
          namaTugas: '',
          mataKuliah: '',
          deadline: '',
          deskripsi: ''
        }
      ]
    }
  },
  methods: {
    tambahkan () {
      this.allData.push({
        namaTugas: '',
        mataKuliah: '',
        deadline: '',
        deskripsi: ''
      })
      this.$swal('Tugas Berhasil Ditambahkan!')
    },
    hapus (index) {
      this.allData.splice(index, 1)
      this.$swal('Tugas Berhasil Dihapus!')
    },
    showAlert () {
      this.$swal('Hello Vue world!!!')
    },
    hapusi (index) {
      this.$swal.fire({
        title: 'Are you sure?',
        text: "You won't be able to revert this!",
        icon: 'warning',
        showCancelButton: true,
        confirmButtonColor: '#3085d6',
        cancelButtonColor: '#d33',
        confirmButtonText: 'Yes, delete it!'
      }).then((result) => {
        if (result.value) {
          this.allData.splice(index, 1)
          this.$swal.fire(
            'Deleted!',
            'Your file has been deleted.',
            'success'
          )
        }
      })
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center ;
  color: #2c3e50;
}
.inputan{
    text-align: center;
    margin-left: 100px;
    margin-right: 100px;
    margin-top: 20px;
    background-color: rgb(2, 2, 2);
}
.judulTabel{
    color: black;
    align-content: center;
}
div.btnTambah{
    position: -webkit-sticky;
  position: sticky;
  top: 0;
  padding: 5px;
  background-color: #2c3e50;
  border: 2px solid #4CAF50;
}
.detail{
    text-align: left;
    background: rgb(0, 191, 255);
    padding: 10px;
}
.cd-popup {
  opacity: 0;
  visibility: hidden;
  transition: opacity 0.3s 0s, visibility 0s 0.3s;
}

.cd-popup.is-visible {
  opacity: 1;
  visibility: visible;
  transition: opacity 0.3s 0s, visibility 0s 0s;
}

.cd-popup-container {
  transform: translateY(-40px);
  transition-property: transform;
  transition-duration: 0.3s;
}

.is-visible .cd-popup-container {
  transform: translateY(0);
}
</style>
