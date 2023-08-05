<template>
  <footer class="footer">
    <div class="footer-section">
      <div class="section">
      <img src="../assets/logo.svg" alt="Logo" class="footer-logo" />
      <p>
        <a href="mailto:hello@pressone.africa" class="email"
          >hello@pressone.africa</a
        >
      </p>
      <p class="phone-number">+234 1 343 8962</p>
      <ul class="social-media-icons">
        <li>
          <a href="#">
            <img src="../assets/facebook.svg" alt="" class="social-icons"
          /></a>
        </li>
        <li>
          <a href="#">
            <img src="../assets/twitter.svg" alt="" class="social-icons"
          /></a>
        </li>
        <li>
          <a href="#">
            <img src="../assets/instagram.svg" alt="" class="social-icons"
          /></a>
        </li>
        <li>
          <a href="#">
            <img src="../assets/linkedin.svg" alt="" class="social-icons"
          /></a>
        </li>
      </ul>
    </div>
    <div class="section company-section">
      <h4 class="section-title">Company</h4>
      <ul class="navigation-list">
        <li><a href="#">Help & Support</a></li>
        <li><a href="#">About Us</a></li>
        <li><a href="#">Product</a></li>
        <li><a href="#">Media</a></li>
        <li><a href="#">FAQs</a></li>
      </ul>
    </div>
    <div class="section address-section">
      <h4 style="margin-bottom: 20px" class="footer-title">Address</h4>
      <p class="address">
        The Lennox Mall, 3 Admiralty Way,<br />
        Lekki Phase 1, Lagos
      </p>
    </div>
    </div>
  
    <div class="caption">
      <div class="caption-section">
        <p>&copy; 2022 PressOne Africa <span>&nbsp; All rights reserved</span></p>
      </div>
      <div  class="caption-section pointer">
        <p >Terms & Agreement<span>&nbsp; Privacy Policy</span></p>
      </div>
    </div>
  </footer>
  
</template>

<script>
export default {
  name: "FooterView",
  
};
</script>

<style scoped lang="scss">
@media (min-width: 1000px) {
  .footer {
    padding: 50px 120px;
    background-color: #fef8e7;

  }
  .footer-logo {
  margin-bottom: 30px;
}
.caption {
  display: flex;
    justify-content: space-between;
    color: #474B50;
} 
}
@media (min-width: 769px) and (max-width: 999px) {
  .footer {
    padding: 50px 40px;
    background-color: #fef8e7;

  }
  .footer-logo {
  margin-bottom: 30px;
}
.caption {
  display: flex;
    justify-content: space-between;
    color: #474B50;
}  
}
@media (max-width: 768px) {
  .footer {
    padding: 50px 20px 20px;
  }
  .footer-logo {
  margin-bottom: 10px;
}
.section-title {
  margin-bottom: 20px;
  text-align: right;
}
.navigation-list {
  text-align: right;
}
.address-section {
  text-align: left;
}
}
.footer-section {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.footer {
  font-family: "Urbanist";
}
.section {
  flex: 1 1 calc(33.33% - 20px);
  margin-right: 20px;
  margin-bottom: 20px;

  h4 {
    margin-bottom: 10px;
  }

  .social-media-icons {
    display: flex;
    gap: 20px;

    img {
      width: 22px;
      height: 22px;
    }
  }
  .address-section {
  text-align: right !important;
}
}


.email {
  text-decoration: none;
  color: #474b50;
  font-size: 15px;
  line-height: 17px;
}
.phone-number {
  color: #474b50;
  font-size: 15px;
  line-height: 17px;
  margin-top: 12px;
}
li {
  list-style: none;
}
.navigation-list {
  list-style: none;
  padding: 0;

  li {
    margin-bottom: 15px;
  }

  a {
    color: #616c74;
    text-decoration: none;
  }
  
}

.address {
  color: #474b50;
  font-size: 16px;  
}
.section-title {
  margin-bottom: 20px;
  /* text-align: right; */
}

.caption {
    color: #474B50;
} 
.caption-section {
  margin-right: 0;

}
</style>
