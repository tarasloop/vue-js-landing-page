<script lang="ts" setup>
import { onMounted } from 'vue';
import '@n8n/chat/style.css';

import { createChat } from '@n8n/chat';

onMounted(() => {
  createChat({
    webhookUrl: 'https://tobeaccelerator.app.n8n.cloud/webhook/9877aa83-4a0f-43d6-9eea-795c2a0f172d/chat',
    webhookConfig: {
		method: 'POST',
		headers: {}
	},
	target: '#n8n-chat',
	mode: 'window',
	chatInputKey: 'chatInput',
	chatSessionKey: 'sessionId',
	metadata: {},
	showWelcomeScreen: false,
	defaultLanguage: 'en',
	initialMessages: [
		'Ciao sono TOBy 👋',
		'Come posso aiutarti oggi?'
	],
	i18n: {
		en: {
			title: 'TOBy',
			subtitle: "Powered By To Be Accelerator",
			footer: '',
			getStarted: 'New Conversation',
			inputPlaceholder: 'Chiedimi qualcosa!',
		},
	},
});
});
import mainPhoto from "../assets/images/hero.svg";
import { themeColor } from "../data/items";

const heroHeading = "To Be Accelerator AI";
// const buttonSeeFeature = "See Features";
// const buttonPricing = "Pricing";
</script>

<template>
  <div class="untree_co-hero" id="home-section">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-12">
          <div class="dots"></div>
          <div class="row align-items-center">
            <div
              class="col-lg-7 ml-auto order-lg-2"
              data-aos="fade-right"
              data-aos-delay="400"
            >
              <img :src="mainPhoto" alt="Image" class="img-fluid" />
            </div>
            <div class="col-lg-5">
              <h1 class="heading" data-aos="fade-up" data-aos-delay="0">
                {{ heroHeading }}
              </h1>
              <!-- <div class="excerpt" data-aos="fade-up" data-aos-delay="100">
                <p>
                  Another cool free html css template by
                  <span
                    style="
                      background-color: rgba(64, 123, 255, 0.07);
                      color: #407bff;
                    "
                    >Colorlib</span
                  >
                  To Be Accelerator AI Model Transformer
                </p>
              </div> -->
              <!-- <p data-aos="fade-up" data-aos-delay="200">
                <a
                  href="#features-section"
                  class="btn btn-primary smoothscroll"
                  style="margin-right: 5px"
                  :style="[
                    { background: themeColor },
                    { borderColor: themeColor },
                  ]"
                  >{{ buttonSeeFeature }}</a
                >
                <a
                  href="#pricing-section"
                  class="btn btn-outline-primary smoothscroll pricing"
                  :style="[{ color: themeColor }, { borderColor: themeColor }]"
                  >{{ buttonPricing }}</a
                >
              </p> -->
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.pricing:hover {
  color: #fff !important;
}
</style>
