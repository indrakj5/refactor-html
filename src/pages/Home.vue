<template>
  <div>
    <div class="hero-image">
      <div class="hero-text">
        <h1>Ayo Kita Travel</h1>
        <p>Temukan Destinasi Impianmu</p>
        <button><a href="#destinasi">Pesan Sekarang</a></button>
      </div>
    </div>
    <div id="home">
      <div class="text-home">
        <h1>Home</h1>
        <h2>Butuh Liburan?</h2>
        <p>Ayo liburan, pilih destinasi wisata tujuan kalian di TravelKuy</p>
        <p>
          Kami menyediakan banyak pilihan destinasi wisata untuk kalian semua,
          mulai dari dalam negeri sampai ke luar negeri dengan harga bersahabat
        </p>
      </div>
      <div class="iframe-container">
        <iframe
          width="720"
          height="480"
          src="https://www.youtube.com/embed/3SsK-cxlj_w"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>

    <div id="about">
      <div class="text-aboutus">
        <h1>About Us</h1>
        <h3>
          TravelKuy adalah sebuah perusahaan travel yang bertujuan melayani
          kebutuhan orang-orang dalam hal rekreasi
        </h3>
        <p>
          Kami memiliki tim profesional yang berkomitmen dan bersemangat untuk
          memastikan dari saat Anda mendarat hingga keberangkatan Anda, Anda
          akan menerima pelayanan terbaik dan pengalaman yang mengubah hidup
          yang tak terlupakan. Kami menyediakan semua tour hemat dan berkualitas
          untuk semua orang, dari paket tour standar ke paket tour mewah, paket
          wisata umum dan wisata yang dibuat khusus. Dengan pengalaman kami
          sebagai operator tour, kami membantu Anda membuat perjalanan Anda
          menjadi luar biasa. Kami berdiri sejak tahun 2000, telah mendapatkan
          berbagai pengalaman wisata baik domestik atau luar negeri. Berbagai
          pelayanan tour terbaik telah kami berikan kepada klien-klien kami.
        </p>
        <h3>
          Kami menyediakan berbagai macam paket liburan dengan destinasi menarik
          mulai dari dalam negeri hingga luar negeri
        </h3>
        <p>
          TravelKuy memberikan kualitas, kepuasan, kenyamanan, kepercayaan diri,
          dan keamanan bagi perjalanan klien kami. Menjadi salah satu perusahaan
          terbesar di Indonesia adalah impian kami. Yang bisa memberikan
          pelayanan maksimal kepada klien-klien kami baik sekarang ataupun masa
          yang akan datang. NOL komplain merupakan tujuan utama kami melayani
          klien-klien kami.
        </p>
      </div>
    </div>
    <div id="destinasi">
      <div class="text-destinasi">
        <h1>Destinasi</h1>
        <h3>Silahkan pilih destinasi wisata Anda</h3>
        <div class="image-flex-container">
          <div class="image-flex"><img src="../assets/asia.png" /></div>
          <div class="image-flex"><img src="../assets/australia.png" /></div>
          <div class="image-flex"><img src="../assets/africa.png" /></div>
          <div class="image-flex"><img src="../assets/america.png" /></div>
          <div class="image-flex"><img src="../assets/europe.png" /></div>
        </div>
        <div class="text-flex-container">
          <div class="text-flex">Asia</div>
          <div class="text-flex">Australia</div>
          <div class="text-flex">Afrika</div>
          <div class="text-flex">Amerika</div>
          <div class="text-flex">Eropa</div>
        </div>
      </div>
    </div>
    <div id="contact">
      <div class="text-contact">
        <h1>Contact</h1>
        <p><i class="fa fa-phone"> Telephone : 0213456789</i></p>
        <p><i class="fa fa-envelope"> Email : info@travelkuy.com</i></p>
        <p><i class="fa fa-facebook"> Facebook : TravelKuy</i></p>
        <p><i class="fa fa-instagram"> Instagram : @TravelKuy</i></p>
      </div>
    </div>
  </div>
</template>

<script>
import CustomButton from "../components/Button.vue";
import axios from "axios";
export default {
  data() {
    return {
      label: "About",
      dataUSA: []
    };
  },
  components: {
    CustomButton
  },
  async created() {
    try {
      const urlAPI =
        "https://datausa.io/api/data?drilldowns=Nation&measures=Population";
      const response = await axios.get(urlAPI);
      const {
        data: { data: arrData }
      } = response;
      this.dataUSA = arrData;
    } catch (err) {
      console.log(err);
    }
  }
};
</script>

<style></style>
