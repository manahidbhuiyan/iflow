<template>
  <!-- banner area -->
  <section class="banner pt-5 px-0 pb-10 overflow-hidden relative bg-white">
    <div class="banner-box hidden sm:block sm:w-full md:w-[740px] p-6 pt-0 md:p-6 bg-white relative md:top-[65px] left-0 md:left-[30px] 991:left-[160px] 1200:left-[245px]">
      <h5 class="text-3xl pb-2 capitalize font-semibold text-[#0e2442] ">what we do</h5>
      <p class="text-3xl capitalize font-normal leading-10 text-[#0e2442] mb-0">
        We are driven by one goal: to create spaces that inspire people to do
        amazing things.
      </p>
    </div>
    <div class="banner-inner">
      <img class="w-full" src="../assets/images/banner.png" alt="" />
      <p class="pt-3 sm:pt-5 md:pt-10 px-[10px] pb-0 my-0 mx-auto w-full md:w-4/5 text-base md:text-[28px] leading-7 md:leading-10 text-[#0e2442] text-center">
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
   <section class="com-details px-2 py-[30px] sm:px-20 sm:py-[50px] md:py-[70px] lg:px-32 bg-[#EDF5FE] ">
    <div class="container">
      <h3 class="details-title text-4xl font-semibold uppercase text-center mb-[30px] md:mb-[50px]">What we do</h3>
      <div class="details-inner grid gap-4 grid-cols-1 576:grid-cols-2 991:grid-cols-3 1300:grid-cols-4 ">
  <div class="card card-1 bg-[#e57661] text-white row-span-2 auto-rows-auto hover:bg-[#e57661]">
    <h2 class="text-white text-3xl mb-5">Design & Build</h2>
    <p class="text-2xl text-white">Comprehensive management of your project from initial concept to final construction.</p>
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
  <section class="isotop-section py-[50px] px-5 md:py-20 bg-[#f6f7f9] text-center h-auto ">
    <IsotopeGrid />
  </section>
  <!-- consult area -->
  <section class="consult py-[30px] px-[10px] 991:p-[50px] 1300:p-[70px] relative ">
    <div class="consult-content relative z-20">
      <div class="consult-images w-full hidden 991:flex justify-between gap-5 ">
        <img class=" w-[20%]" src="../assets/images/image 18.png" alt="" />
        <img class=" w-[20%]" src="../assets/images/image 21.png" alt="" />
        <img class=" w-[20%]" src="../assets/images/image 19.png" alt="" />
        <img class=" w-[20%]" src="../assets/images/image 20.png" alt="" />
      </div>
      <div class="consult-text">
        <p class=" max-w-[720px] my-0 mx-auto py-[50px] px-0 text-2xl font-medium text-center text-white">
          We handle projects of all sizes, from small tasks to large
          architectural endeavors. <br /><br />
          Speak with our consultant, and we will assign a professional to cater
          to your specific property needs.
        </p>
      </div>
      <div class="consult-button text-center">
        <button class="btn btn-consult w-[300px] text-[18px] font-medium sm:w-[380px] 
        sm:p-2 bg-[#e57661] border-[3px] border-[#f3f3f3] sm:text-white uppercase
         sm:text-2xl sm:font-semibold ">Talk to our consultant</button>
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
