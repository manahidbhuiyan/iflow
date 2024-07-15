<template>
    <div class="footer">
        <div class="footer-child-1">
            <p>
                iFlowspace Sdn Bhd <br>
                28-3 Jalan PJU 5/4 <br>
                Dataran Sunway, Kota Damansara,<br>
                Petaling Jaya, 47810 Selangor.<br>
                Whatsapp : +6 010 888 5055
            </p>
        </div>
        <div class="footer-child-2">
            <h5 class="footer-title">Company</h5>
            <div class="addition-page">
                <div class="left">
                    <p><a href="#">Abot</a></p>
                    <p><a href="#">Career</a></p>
                    <p><a href="#">Calculator</a></p>
                </div>
                <div class="right">
                    <p><a href="#">FAQs</a></p>
                    <p><a href="#">Contact Us</a></p>
                    <p><a href="#">Partnership</a></p>
                </div>
            </div>
        </div>
        <div class="footer-child-3">
            <h5 class="footer-title">GET LATEST NEWS ON <br> PROPERTY & DESIGN</h5>
            <input type="text" class="mail-input" placeholder="Enter your email address">
            <div class="footer-child-3-btn"><a href="#" class="signUp-button">Sign Up</a></div>
        </div>
        <div class="footer-child-4">
            <h5 class="footer-title">Keep in touch</h5>
            <p>hello@iflowspace.com</p>
            <div class="social-icon">
                <img src="../assets/images/Instagram.png" alt="">
                <img src="../assets/images/LinkedIn.png" alt="">
            </div>
        </div>
    </div>
</template>
<script>

</script>
<style lang="css" scoped>
.footer{
    background-color: #0E2442;
    padding: 50px 40px;
    display: grid;
    grid-template-columns: 1fr; /* Default to 1 column */
    gap: 30px; /* Adjust spacing between items as needed */
}

.footer-title{
    font-size: 20px !important;
    font-weight: 600;
    color: #fff;
}
.footer-child-1 p{
    margin-top: 10px;
    color: #fff;
}
.footer-child-2 h5{
    font-size: 24px !important;
    font-weight: 600;
    color: #fff;
}
.addition-page{
    display: flex;
    justify-content: flex-start;
    gap: 50px;
}
.addition-page a{
    color: #fff;
    font-size: 16px;
    text-decoration: none;
}
.mail-input{
    width: 330px;
    padding: 5px;
    margin-top: 10px;
    margin-bottom: 20px;
}
.mail-input:focus-visible{
    border: none;
    outline: 0;
    box-shadow: none;
}
.footer-child-3-btn{
    width: 115px;
}
.signUp-button{
    display: inline-block;
    width: 110px;
    text-decoration: none;
    text-align: center;
    color: #fff;
    padding: 5px;
    border: 2px solid #fff;
    cursor: pointer;
}
.footer-child-4{
    color: #fff;
}
.social-icon{
    display: flex;
    justify-content: start;
    gap: 10px;
}
.social-icon img{
    width: 40px;
}

/* Medium devices (Tablets) */
@media (min-width: 768px) {
  .footer {
    grid-template-columns: 1fr 1fr; /* 2 columns */
  }
}

/* Large devices (Desktops) */
@media (min-width: 992px) {
  .footer {
    grid-template-columns: 1fr 1fr 1fr 1fr; /* 4 columns */
    gap: 20px; /* Adjust spacing between items as needed */
  }
}

/* small device */
@media (max-width: 576px) {
  .footer {
    padding: 40px 10px;
  }
}
@media (max-width: 400px) {
  .mail-input {
    width: 100% !important;
  }
}
</style>