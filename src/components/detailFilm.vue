<template>
    <div class="container">
        <div class="movie" v-for="(data, index) in movie" :value="data" :key="index">
            <div class="movie-item" v-if="filmId == data.id">
                <h1 class="page-title">Movie Details</h1>
                <img v-bind:src="data.image"  class="img-fluid img-movie" v-bind:alt="data">
                <div class="value">
                    <h1>{{data.title}}</h1>
                    <hr>
                    <p class="desc">{{data.desc}}</p>
                    <h2>IMDb : {{data.rating}}</h2>
                    <p>Genre : {{data.genre}}</p>
                    <p>Duration : {{data.duration}}</p>
                    <p>Director : {{data.director}}</p>
                    <p>Actor : {{data.actor}}</p>
                    <p>Release : {{data.release}}</p>
                    <p>Country : {{data.country}}</p>
                </div>
            </div>
        </div>
        <div class="back">
            <router-link to='/'><button class="btn-back">BACK TO HOME</button></router-link>
        </div>
        <div class="footer">
            <h5>Build &copy;2020. By Daarusynema</h5>
        </div>
    </div>
</template>

<script>
import Img1 from '../assets/images/11.jpg'
import Img2 from '../assets/images/12.jpg'
import Img3 from '../assets/images/13.jpg'
import Img4 from '../assets/images/4.jpg'
import Img5 from '../assets/images/14.jpg'
import Img6 from '../assets/images/6.jpg'
import Img7 from '../assets/images/7.jpg'
import Img8 from '../assets/images/8.jpeg'
export default {
  data () {
    return {
      filmId: this.$route.params.id,
      movie: [
        {
          id: 1,
          image: Img1,
          desc: 'Seorang anak bernama Aqilla (Aisha Nurra Datau) memiliki cita-cita untuk menjadi Astronot. Opanya (Cok Simbara) yang seorang astronom adalah orang yang sangat dia kagumi. Aqilla banyak belajar dan bertanya pada Opa, yang menjabat di Planetarium Jakarta. Hampir setiap hari Aqilla mendatangi Opa di Planetarium untuk berbincang. Hingga akhirnya Aqilla bertemu dengan Tsurayya (Maudy Koesnaedi), seorang astronot Indonesia yang sedang melakukan penelitian tanaman untuk dikirim ke ruang angkasa.',
          title: 'Iqro: My Universe (2019)',
          rating: '7.4',
          genre: 'Drama, Family',
          release: '2019',
          duration: '101 min',
          director: 'Iqbal Alfajri',
          actor: 'Aisha Nurra Datau, Cok Simbara, Maudy Koesnaedi, Raihan Khan, Harris J',
          country: 'Indonesia'
        },
        {
          id: 2,
          image: Img2,
          desc: 'Aqila (Aisha Nurra Datau) adalah anak yang sangat gandrung pada sains namun kurang punya minat belajar Al Qur’an. Aqila memiliki seorang kakek (Cok Simbara) yang berprofesi sebagai astronom dan tinggal di Observatorium Bosscha. Aqila bermaksud membuat tugas sekolahnya yang berhubungan dengan astronomi, Kakeknya memberi izin pada Aqila untuk menggunakan teropong bintang di Boscha untuk menyelesaikan tugasnya, namun dengan satu syarat: Aqila harus bisa membaca Al Qur’an. Aqila menyanggupinya. Saat di rumah kakeknya Aqila bertemu Ros (Adhitya Putri), anak dari seorang pembantu di sana. Ros mengajaknya bermain di sebuah masjid. Di masjid inilah Aqila belajar membaca Al Qur’an dengan metode Iqro, yang fun, berirama dan dibawakan secara ringan. Pengalaman Aqila belajar Al Qur’an dan teladan dari kakeknya inilah yang menggugah mata hatinya, tentang kebesaran Allah SWT yang menciptakan alam semesta.',
          title: 'Iqro: Petualangan Meraih Bintang',
          rating: '-',
          genre: 'Drama, Family',
          release: '2017',
          duration: '97 min',
          director: 'Iqbal Alfajri',
          actor: ' Aisha Nurra Datau, Raihan Khan, Adhitya Putri, Mike Lucock, Neno Warisman, Cok Simbara',
          country: 'Indonesia'
        },
        {
          id: 3,
          image: Img3,
          title: 'Koki-koki Cilik 2',
          desc: 'Film ini bercerita soal libur telah tiba dan Cooking Camp akan dibuka. Itu berarti waktu untuk Bima, Alfa, Kevin, Niki, Mely dan Key untuk datang kembali ke camp. Niat awal para koki cilik ini untuk berkumpul dan reuni anggota Cooking Camp sebelumnya. Sayangnya mereka dikejutkan bahwa camp sudah ditutup. Biang keroknya adalah Evan, mantan chef terkenal yang mengatakan bahwa Grant, pengajar di camp, tidak mumpuni. Grant terpuruk dan memutuskan untuk tidak lagi berkegiatan mengajar di camp. Bima dan kawan-kawan harus membantu membangkitkan semangat Grant dan menggalang dana untuk membuka kembali Cooking Camp.',
          rating: '6.8',
          genre: 'Drama, Family',
          release: '2019',
          duration: '91 min',
          director: 'Viva Westi',
          actor: ' Ringgo Agus Rahman, M. Adhiyat, Faras Fatik.',
          country: 'Indonesia'
        },
        {
          id: 4,
          image: Img4,
          title: 'Filosofi Kopi (2019)',
          desc: 'Cerita tentang pencarian jiwa dan perjalanan berdamai dengan masa lalu melalui kopi. Ben dan Jody adalah sahabat yang membangun kedai “Filosofi Kopi”, sebuah kedai kopi terkemuka di Jakarta yang hanya menyediakan kopi terbaik Indonesia. Sebuah tantangan untuk membuat kopi yang sempurna dari seorang pengusaha membawa Ben dan Jody pada petualangan menyusun serpihan masa lalu mereka yang penuh getir dengan orang tua mereka masing-masing.',
          rating: '7.1',
          release: '2019',
          duration: '117 min',
          genre: 'Adventure, Comedy, Drama',
          director: 'Angga Dwimas Sasongko',
          actor: ' Chicco Jerikho, Jajang C. Noer, Julie Estelle, Otig Pakis, Rio Dewanto, Ronny P. Tjandra, Slamet Rahardjo.',
          country: 'Indonesia'
        },
        {
          id: 5,
          image: Img5,
          title: 'Koki-koki Cilik',
          desc: 'Film ini berkisah tentang Bima (Farras Fatik), seorang anak dari keluarga tidak mampu, yang berhasil ikut dalam acara Cooking Camp, sebuah acara kemping memasak yang sangat bergengsi dan mahal. Dengan segala kekurangannya, Bima harus menghadapi tantangan memasak dari Chef Grant (Ringgo Agus Rahman) dan bersaing dengan Audrey (Chloe Xaviera), sang juara masak tiga kali berturut-turut di Cooking Camp.',
          rating: '7.4',
          release: '2018',
          duration: '91 min',
          genre: 'Drama, Family',
          director: 'Ifa Isfansyah',
          actor: ' Morgan Oey, Ringgo Agus Rahman, Faras Fatik.',
          country: 'Indonesia'
        },
        {
          id: 6,
          image: Img6,
          title: 'Rasuk 2 (2020)',
          desc: 'Isabella (Nikita Willy), mahasiswi kedokteran yang sedang menjalani koas, merasa tidak nyaman dengan kemampuan indera keenam yang dimilikinya. Dia berupaya kuat menganggap mereka tidak ada agar bisa hidup dengan normal. Namun, kejadian di ruang autopsi saat membedah satu jenazah wanita tanpa identitas mengubah semua pandangan hidupnya. Arwah jenazah itu terus mengikutinya, meneror, bahkan merasukinya untuk meminta tolong. Kondisi ini mengganggu hubungan Isabela dengan teman-temannya dan mengancam studinya. Satu-satunya orang yang bisa memahami Isabela dan memberinya dukungan adalah sang kakak, Fransisca Inggrid (Raquel Katie Larkin). Di tengah usahanya melepaskan diri dari gangguan gaib yang mengancam jiwanya, Isabela jatuh cinta dengan Radja (Achmad Megantara). Untuk pertama kali dalam hidupnya, Isabela bertemu dengan seseorang yang bisa memahami kelebihannya selain Fransisca Inggrid. Gangguan yang dialami Isabela membawanya menguak selembar demi selembar misteri tentang kematian sang arwah yang mengganggunya selama ini. Tidak ada pilihan bagi Isabela selain menerima kelebihannya, dan membantu sang arwah menyelesaikan urusannya. Meskipun ia harus mempertaruhkan keselamatan jiwanya..',
          rating: '7.0',
          release: '2020',
          duration: '100 min',
          genre: 'Horor, Mystery, Thriller',
          director: 'Rizal Mantovani',
          actor: 'Nikita Willy, Achmad Megantara, Asri Welas, Raquel Katie Larkin, Sonia Alyssa, Prilly Latuconsina, Tegar Satrya, Iang Darmawan.',
          country: 'Indonesia'
        },
        {
          id: 7,
          image: Img7,
          title: 'Sri Asih (2020)',
          desc: 'Nani Wijaya adalah seorang gadis lugu yang terlahir dari keluarga kaya raya. Ia merupakan reinkarnasi dari Dewi Sri. Apabila ia mengucapkan kata sakti "Dewi Asih", maka ia akan berubah menjadi Sri Asih, seorang pahlawan super wanita yang memiliki keahlian bela diri yang memiliki kekuatan setara dengan 250 pria dewasa.[1] Tak hanya itu, Sri Asih juga memiliki kemampuan untuk terbang, memiliki tubuh yang kebal, serta memiliki Triwikarma, sebuah kemampuan titisan Dewa Wisnu yang membuatnya dapat menggandakan diri dan dapat memperbesar tubuhnya.',
          rating: 'Coming Soon',
          release: 'Coming Soon 2020',
          duration: '-',
          genre: 'Action, Crime, Drama',
          director: 'Upi Avianto',
          actor: 'Pevita Pearce, Chelsea Islan, Chicco Jerikho, Joe Taslim, Nicholas Saputra .',
          country: 'Indonesia'
        },
        {
          id: 8,
          image: Img8,
          title: 'Gundala (2019)',
          desc: 'Sancaka telah hidup di jalanan sejak orang tuanya meninggalkannya. Menjalani hidup yang sulit, Sancaka bertahan dengan memikirkan keselamatannya sendiri. Ketika kondisi kota semakin memburuk dan ketidakadilan mengamuk di seluruh negeri, Sancaka harus memutuskan apakah ia terus hidup untuk menjaga dirinya sendiri atau bangkit untuk menjadi pahlawan bagi yang tertindas.',
          rating: '7.8',
          release: '2019',
          duration: '123 min',
          genre: 'Joko Anwar',
          director: 'Joachim Rønning, Espen Sandberg',
          actor: 'Abimana Aryasatya, Bront Palarae, Fariz Fajar, Marissa Anita, Muzakki Ramdhan, Rio Dewanto, Tara Basro.',
          country: 'Indonesia'
        }
      ]
    }
  }
}
</script>

<style scoped>
    .container {
        width: auto;
    }
    .header-title {
      font-family: monospace;
      font-size: 70px;
      color: #fff;
    }
    .header-subtitle {
      font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
      font-size: 20px;
    }
    .movie-item {
        padding: 50px;
        width: auto;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-auto-rows: minmax(50px, auto);
        text-align: left;
        background-color: #F0F8FF;
    }
    .page-title {
        grid-column: 1/3;
        text-align: center;
        padding-bottom: 30px;
        background-color: #87CEEB;
        font-family: 'Times New Roman', Times, serif;
        border: 0px;
        border-radius: 20px;
    }
    .back {
      text-align: center;
      padding-bottom: 50px;
      background-color: #87CEEB;
    }
    .btn-back {
        background-color: red;
        color: #fff;
        border: 0px;
        border-radius: 60px;
        text-align: center;
        margin: 5px 2px;
        padding: 20px 15px;
        cursor: pointer;
        transition: 0.3s;
        margin: 20px;
        width: 300px;
    }
    .btn-back:hover {
        background-color: transparent;
        border: 2px solid red;
        color: red;
    }
    .img-movie {
        width: 500px;
        box-shadow: 0 20px 25px 0 rgba(0,0,0,0.2);
        transition: 0.3s ease;
        border: 0px;
        border-radius: 20px;
    }
    .desc {
        text-align: justify;
    }
    .footer {
        padding: 10px;
        grid-column: 1/5;
        background-color: #fff;
        color: #000;
        text-align: center;
    }
    .value{
      color: #000;
      font-family: 'Times New Roman', Times, serif;
    }
    h1{
      font-size: 50px;
      padding-top: 50px;
    }
    .page-title{
      color:#fff;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
      transition: 0.3s;
      background-color: #181818;
      width: 100%;
      height: 100px;
    }
</style>
