<template>
  <!-- banner area -->
  <section class="banner">
    <div class="banner-box">
      <h5>what we do</h5>
      <p>
        We are driven by one goal: to create spaces that inspire people to do
        amazing things.
      </p>
    </div>
    <div class="banner-inner">
      <img src="../assets/images/banner.png" alt="" />
      <p>
        <b>iFlowspace</b> is not just a platform that outsources everything to
        partners; we work closely with each professional as an in-house team to
        provide comprehensive business and residential solutions. From finding a
        cozy house or stylish office, to space planning, design, build, and even
        post-completion aftercare, you will only need to deal with
        <b>one dedicated team.</b>
      </p>
    </div>
  </section>
  <!-- company details area -->
   <section class="com-details">
    <div class="container">
      <h3 class="details-title">What we do</h3>
      <div class="details-inner">
  <div class="card card-1">
    <h2>Design & Build</h2>
    <p>Comprehensive management of your project from initial concept to final construction.</p>
  </div>
  <div class="card card-2">
    <h2>Office Space</h2>
    <p>Creating functional and aesthetically pleasing work environments tailored to your business needs.</p>
  </div>
  <div class="card card-3">
    <h2>Refurbishment</h2>
    <p>Modernizing and revitalizing existing spaces or your commercial lot to enhance their appeal and functionality.</p>
  </div>
  <div class="card card-4">
    <h2>Construction</h2>
    <p>Delivering high-quality building services for various types of projects, ensuring durability and excellence.</p>
  </div>
  <div class="card card-5">
    <h2>Home Renovation</h2>
    <p>Transforming your home to reflect your style and improve your living experience.</p>
  </div>
  <div class="card card-6">
    <h2>Space Planning</h2>
    <p>Efficiently organizing and optimizing your space for maximum usability and comfort including landscape planning.</p>
  </div>
  <div class="card card-7">
    <h2>Interior & Styling</h2>
    <p>We’ll consult and collaborate before providing you with detailed sketches, plans and 3D renders to help you visualise your space.</p>
  </div>
  <div class="card card-8">
    <h2>Property Search</h2>
    <p>Assisting in finding the perfect property that meets your personal, business or investment needs.</p>
  </div>
  <div class="card card-9">
    <h2>Carpentry</h2>
    <p>Providing custom carpentry solutions with exceptional craftsmanship and attention to detail.</p>
  </div>
  <div class="card card-10">
    <h2>Coworking/Serviced</h2>
    <p>Designing and building dynamic coworking environments that foster collaboration and maximize space profit potential.</p>
  </div>
  <div class="card card-11">
    <h2>Furniture</h2>
    <p>Sourcing and installing quality furniture, curtains and home appliance to complete your space with style and functionality.</p>
  </div>
</div>
    </div>
   </section>
  <!-- isotop area -->
  <section class="isotop-section">
    <IsotopeGrid />
  </section>
  <!-- consult area -->
  <section class="consult">
    <div class="consult-content">
      <div class="consult-images">
        <img src="../assets/images/image 18.png" alt="" />
        <img src="../assets/images/image 21.png" alt="" />
        <img src="../assets/images/image 19.png" alt="" />
        <img src="../assets/images/image 20.png" alt="" />
      </div>
      <div class="consult-text">
        <p>
          We handle projects of all sizes, from small tasks to large
          architectural endeavors. <br /><br />
          Speak with our consultant, and we will assign a professional to cater
          to your specific property needs.
        </p>
      </div>
      <div class="consult-button">
        <button class="btn btn-consult">Talk to our consultant</button>
      </div>
    </div>
  </section>
</template>

<script>
import IsotopeGrid from "./Isotop.vue";

export default {
  components: {
    IsotopeGrid,
  },
  data() {
    return {
      message: "Hello Vue 3!",
    };
  },
};
</script>

<style>
</style>
