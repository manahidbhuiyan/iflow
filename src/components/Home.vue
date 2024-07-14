<template>
  <!-- banner area -->
   <section class="banner">
    <div class="banner-box">
      <h5>what we do</h5>
      <p>We are driven by one goal: to create spaces that inspire people to do amazing things.
      </p>
    </div>
    <div class="banner-inner">
      <img src="../assets/images/banner.png" alt="">
      <p>
        <b>iFlowspace</b> is not just a platform that outsources everything to partners; we work closely with each professional
         as an in-house team to provide comprehensive business and residential solutions. From finding a cozy house or stylish office,
          to space planning, design, build, and even post-completion aftercare, you will only need to deal with <b>one dedicated team.</b>
      </p>
    </div>
   </section>
   <!-- isotop area -->
    <section class="isotop-section">
      <IsotopeGrid />
    </section>
</template>

<script>
import IsotopeGrid from './Isotop.vue';

export default {
  components: {
    IsotopeGrid,
  },
  data() {
    return {
      message: 'Hello Vue 3!'
    }
  }
}
</script>

<style>

</style>
