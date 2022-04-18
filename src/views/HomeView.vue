<script>
  import JumbotronComps from "@/components/home/JumbotronComps.vue"
  import HeadingContent from "@/components/utils/HeadingContent.vue"
  import ContentImages from "@/components/utils/ContentImages.vue"
  import CarouselComps from "@/components/home/CarouselComps.vue"
  export default {
    name: 'HomeView',
    components: { JumbotronComps, HeadingContent, ContentImages, CarouselComps },
    data() {
      return {
        listServices: [
          'UGD (Unit Gawat Darurat)',
          'Pediatric Surgery',
          'Bedah Saraf',
          'Urologi Pediatric',
          'Bedah Plastic dan Rekonstruksi Estetik',
          'Urologi Perempuan',
          'Pediatric Neonatology',
          'Pediatric Neonatology',
          'Urogynecology',
          'Urogynecology'
        ]
      }
    }
  }
</script>

<template>
    <JumbotronComps :carouselItem="carouselItem" />
    <!-- List Services -->
    <div class="container-fluid background-cream">
      <div class="container py-5 row mx-auto">
        <div class="col-sm-6">
          <HeadingContent 
            subTitle="Stay strong and lets beat Cervical Cancer!" 
            title="Our Great Services for Your Family Care" 
          >
            <a href="#" data-bs-toggle="modal" data-bs-target="#auth" class="btn-pendaftaran btn btn-primary rounded-pill">
                View All Services <i class="bi bi-arrow-right"></i>
            </a>
          </HeadingContent>
        </div>
        <div class="col-sm-6 row">
          <div class="col-sm-6" v-for="listService in listServices" :key="listService">
            <p class="text-services fw-bold">
              {{listService}}
            </p>
          </div>
        </div>
      </div>
    </div>
    <!-- /List Services -->
    <ContentImages 
      title="Our First Facility Surgery & Kids Center" 
      paragraph="Dilengkapi dengan berbagai fasilitas kesehatan, di antaranya : Orthopaedics & Traumatologi Center, Bandung Urologi Center"
    >
      <img src="https://dummyimage.com/600x400/000/fff" class="d-block mx-auto img-fluid" alt="Bootstrap Themes" style="width: 100%;" height="500" loading="lazy">
        <template v-slot:extra>
          <a href="#" class="btn-pendaftaran btn btn-primary rounded-pill">
              View All Services <i class="bi bi-arrow-right"></i>
          </a>
      </template>
    </ContentImages>
    <section class="mx-0 container mx-auto row py-5" id="link-other">
        <div class="col-sm-4 link-icon">
            <div class="d-flex align-items-center gap-3">
                <img src="@/assets/images/first-aid-kit.png" alt="first-aid" />
                <h3 class="align-self-center">Zona P3K</h3>
            </div>
            <p>Dapatkan berbagai informasi dan pengetahuan seputar pertolongan pertama pada kecelakaan</p>
            <a href="#" class="link-to-readmore btn btn-primary rounded-pill">Read More <i class="bi bi-arrow-right"></i></a>
        </div>
        <div class="col-sm-4 link-icon">
            <div class="d-flex align-items-center gap-3">
                <img src="@/assets/images/baby.png" alt="first-aid" />
                <h3 class="align-self-center">Ide Nama Bayi</h3>
            </div>
            <p>Dapatkan berbagai informasi dan pengetahuan seputar pertolongan pertama pada kecelakaan</p>
            <a href="#" class="link-to-readmore btn btn-primary rounded-pill">Read More <i class="bi bi-arrow-right"></i></a>
        </div>
        <div class="col-sm-4 link-icon">
            <div class="d-flex align-items-center gap-3">
                <img src="@/assets/images/hospital.png" alt="hospital" />
                <h3 class="align-self-center">Foodtraveler</h3>
            </div>
            <p>Dapatkan berbagai informasi dan pengetahuan seputar pertolongan pertama pada kecelakaan</p>
            <a href="#" class="link-to-readmore btn btn-primary rounded-pill">Read More  <i class="bi bi-arrow-right"></i></a>
        </div>
    </section>
    <!-- carousel -->
    <CarouselComps />
    <!-- /carousel -->
</template>

<style scoped>
  .btn-pendaftaran, .link-to-readmore {
      background: #75C6EF;
      border: transparent;       
  }
  .btn-pendaftaran:hover {
      background: #75C6EF;
      border: transparent;
      opacity: 0.5;       
  }
  .text-services {
    color: #1B4674;
  }
</style>