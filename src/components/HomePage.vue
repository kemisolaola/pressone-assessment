<template>
  <div class="main-container">
    <!-- Banner -->

    <div class="banner">
      <div class="banner-info">
        <h1 class="banner-title">
          You do the work,<br />
          We'll do the talk
        </h1>
        <h2 class="banner-subtitle">
          Move your customers'<span class="enquiry"> enquiry</span> to our team
          of experts
        </h2>
        <p class="banner-text">
          Let us manage your customer relatioship from their first call till
          they become your raving fans
        </p>
        <button class="get-started-btn">Get Started</button>
      </div>
      <div class="banner-img">
        <img src="../assets/banner.svg" alt="Image Description" />
      </div>
    </div>
    <!-- Review -->
    <section class="review-container">
      <div class="review-card" v-for="review in reviews" :key="review">
        <div class="avatar">
          <img src="../assets/user.svg" alt="" class="review-user-icon" />
        </div>
        <div class="review-inner-card">
          <p class="review-text">
            {{ review }}
          </p>
        </div>
      </div>
    </section>
    <!-- What you get -->
    <section class="product-container">
      <h1 class="product-header">What you get</h1>
      <div class="product">
        <div class="sales-card">
          <div class="product-inner-card">
            <div class="avatar">
              <img src="../assets/sales.svg" alt="" class="review-user-icon" />
            </div>
            <div class="support-info">
              <h2 style="text-align: center" class="support-title">
                Sales Support
              </h2>
              <ul>
                <li
                  v-for="(product, index) in salesProducts"
                  :key="index"
                  class="product-feature-list"
                >
                  <img src="../assets/sales-support-icon.svg" />
                  <p>{{ product }}</p>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="customer-card">
          <div class="product-inner-card">
            <div class="avatar">
              <img
                src="../assets/customer.svg"
                alt=""
                class="review-user-icon"
              />
            </div>
            <div class="support-info">
              <h2 style="text-align: center" class="support-title">
                Customer Support
              </h2>
              <ul>
                <li
                  v-for="(product, index) in salesProducts"
                  :key="index"
                  class="product-feature-list"
                >
                  <img src="../assets/customer-support-icon.svg" />
                  <p>{{ product }}</p>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Plan  -->
    <section>
      <h1 class="product-header">Choose a plan that works for you</h1>
      <!-- <div v-if="isLoading" class="loading message">
        Please Wait while we fetch plans.....
      </div>
      <div v-if="isError && !isLoading" class="error-message">
        {{ planError }} <span class="pointer" @click="getPlans">Retry</span>
      </div> -->
      <div>
        <div class="plan-container">
          <div>
            <div class="plan-img">
            <img src="../assets/plan-logo.svg" alt="" />
          </div>
          <table class="responsive-table" style="margin-top: 20px">
              <tbody>
                <tr>
                  <td>Call Reception</td>
                </tr>
                <tr>
                  <td>Call Reception</td>
                </tr>
                <tr>
                  <td class="last-data">Receive and make calls</td>
                </tr>
              </tbody>
            </table>
          </div>
         
          <div v-for="plan in plans" :key="plan.id">
            <div class="plan-card">
              <p class="starter-plan">{{ plan.name }}</p>
              <p class="plan-price">
                {{ plan.amount }}<span class="per-month">/month</span>
              </p>
              <p class="plan-info">{{ plan.description }}</p>
              <button class="subscribe">{{ plan.cta }}</button>
            </div>
            <table class="responsive-table" style="margin-top: 20px">
              <tbody>
                <tr>
                  <td>{{ plan.call_reception }}</td>
                </tr>
                <tr>
                  <td>{{ plan.calls_per_week }}</td>
                </tr>
                <tr>
                  <td>{{ plan.agent }}</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
        <!-- Plan Fearutes -->
        <!-- <div class="table-container">
          <table class="responsive-table">
            <tbody>
              <tr>
                <td>Call Reception</td>
                <td>Receive calls only</td>
                <td>Receive and make calls</td>
                <td class="last-data">Receive and make calls</td>
              </tr>
              <tr>
                <td>Calls per Week</td>
                <td>Less than 30 calls per week</td>
                <td>30 - 70 calls per week</td>
                <td class="last-data">You choose</td>
              </tr>
              <tr>
                <td>Agents</td>
                <td>Shared agents</td>
                <td>Semi-dedicated agents</td>
                <td class="last-data">Fully dedicated agents</td>
              </tr>
            </tbody>
          </table>
        </div> -->
      </div>

      <!-- support -->
      <section class="support-section">
        <div class="support-container">
          <p class="support-text">
            Join thousands of entrepreneurs using PressOne to improve their
            business communications.
          </p>
          <p class="support-subtext">
            Ready to make your customers love your business?
          </p>
          <div class="support-button">
            <button class="support-btn">Join now</button>
          </div>
        </div>
      </section>
    </section>
  </div>
  <!-- Footer -->
</template>
<script>
import { onMounted, ref } from "vue";
import axios from "axios";
export default {
  setup() {
    const reviews = ref([
      "75% of consumers prefer human interactions to automated interactions.",
      "81% of consumers say a positive customer service experience increases the chances of them making another purchase.",
      "76% of surveyed customers contact customer service over the phone.",
      "68% of buyers will pay more for products and services from a company with a strong record of good customer service.",
    ]);
    const salesProducts = ref([
      "We handle your enquiries, orders, reservations and help improve your customers' experience.",
      "We send a weekly report of custom sales through a personalized dashboard for your business.",
      "You can monitor the calls, hear the conversations and make instant decisions that would grow your business at a glance.",
    ]);
    const plans = ref([
      {
        id: 1,
        name: "Starter Plan",
        amount: "25000",
        description: "For businesses with few customers",
        cta: "Subscribe Here",
        call_reception: "Receive calls only",
        calls_per_week: "Less than 30 calls per week",
        agent: "Shared agents",
      },
      {
        id: 2,
        name: "Growth Plan",
        amount: "50000",
        description: "For growing businesses",
        cta: "Subscribe Here",
        call_reception: "Receive and make calls",
        calls_per_week: "30 - 70 calls per week",
        agent: "Semi-dedicated agents",
      },
      {
        id: 3,
        name: "All Access",
        amount: "Custom",
        description: "For e-commerce and retail businesses",
        cta: "Calculate Your Cost",
        call_reception: "Receive and make calls",
        calls_per_week: "You choose",
        agent: "Fully dedicated agents",
      },
    ]);
    const planError = ref("");
    const isLoading = ref(false);
    const isError = ref(false);
    const getPlans = async () => {
      try {
        isLoading.value = false;
        const res = await axios.get("https://api.jsonserve.com/swQ1ic");
        if (!res.ok) {
          isLoading.value = false;
          isError.value = true;
          planError.value = "Could not fetch plan.";
          return;
        }
        const responseData = res.json();
        plans.value = responseData.data;
        isLoading.value = false;
      } catch (error) {
        isError.value = true;
        isLoading.value = false;
        planError.value = "Could not fetch plan.";
      }
    };

    onMounted(() => {
      getPlans();
    });
    return {
      reviews,
      salesProducts,
      plans,
      getPlans,
      isLoading,
      isError,
      planError,
    };
  },
};
</script>
<style scoped lang="scss"></style>
