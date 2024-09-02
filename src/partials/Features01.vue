<script setup>
import { ref } from 'vue'

const tab = ref('1')
</script>

<template>
  <section class="relative bg-gray-50">
    <div class="py-12 md:py-20">
      <div class="max-w-6xl mx-auto px-4 sm:px-6">
        <div class="max-w-3xl mx-auto text-center pb-12">
          <h2 class="font-inter-tight text-3xl md:text-4xl font-bold text-gray-900 mb-4">Unsere Expertise</h2>
          <p class="text-lg text-gray-500">Entdecken Sie unsere Kernkompetenzen, die Ihnen helfen, online erfolgreich zu sein.</p>
        </div>
        <div>
          <!-- Tabs buttons -->
          <div class="grid grid-cols-2 md:grid-cols-4 gap-4 md:gap-6">
            <button
              :class="tab !== '1' ? 'bg-gray-100 opacity-60 hover:opacity-100 transition' : '[background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] shadow-sm rotate-1'"
              class="text-left px-4 py-5 border border-transparent rounded" @click.prevent="tab = '1'">
              <div class="flex items-center justify-between mb-1">
                <div class="font-inter-tight font-semibold text-gray-900">Technische Optimierung</div>
                <svg :class="tab !== '1' ? 'hidden' : ''" class="fill-gray-400 shrink-0 ml-2" xmlns="http://www.w3.org/2000/svg" width="10" height="10">
                  <path
                    d="M8.667.186H2.675a.999.999 0 0 0 0 1.998h3.581L.971 7.469a.999.999 0 1 0 1.412 1.412l5.285-5.285v3.58a.999.999 0 1 0 1.998 0V1.186a.999.999 0 0 0-.999-.999Z" />
                </svg>
              </div>
              <div class="text-sm text-gray-500">Optimieren Sie die technische Grundlage Ihrer Website für maximale Performance und Sichtbarkeit.</div>
            </button>
            <button
              :class="tab !== '2' ? 'bg-gray-100 opacity-60 hover:opacity-100 transition' : '[background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] shadow-sm rotate-1'"
              class="text-left px-4 py-5 border border-transparent rounded" @click.prevent="tab = '2'">
              <div class="flex items-center justify-between mb-1">
                <div class="font-inter-tight font-semibold text-gray-900">On-Page SEO</div>
                <svg :class="tab !== '2' ? 'hidden' : ''" class="fill-gray-400 shrink-0 ml-2" xmlns="http://www.w3.org/2000/svg" width="10" height="10">
                  <path
                    d="M8.667.186H2.675a.999.999 0 0 0 0 1.998h3.581L.971 7.469a.999.999 0 1 0 1.412 1.412l5.285-5.285v3.58a.999.999 0 1 0 1.998 0V1.186a.999.999 0 0 0-.999-.999Z" />
                </svg>
              </div>
              <div class="text-sm text-gray-500">Optimieren Sie Ihre Inhalte und Meta-Daten, um Ihre Sichtbarkeit in den Suchergebnissen zu steigern.</div>
            </button>
            <button
              :class="tab !== '3' ? 'bg-gray-100 opacity-60 hover:opacity-100 transition' : '[background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] shadow-sm rotate-1'"
              class="text-left px-4 py-5 border border-transparent rounded" @click.prevent="tab = '3'">
              <div class="flex items-center justify-between mb-1">
                <div class="font-inter-tight font-semibold text-gray-900">Content-Erstellung</div>
                <svg :class="tab !== '3' ? 'hidden' : ''" class="fill-gray-400 shrink-0 ml-2" xmlns="http://www.w3.org/2000/svg" width="10" height="10">
                  <path
                    d="M8.667.186H2.675a.999.999 0 0 0 0 1.998h3.581L.971 7.469a.999.999 0 1 0 1.412 1.412l5.285-5.285v3.58a.999.999 0 1 0 1.998 0V1.186a.999.999 0 0 0-.999-.999Z" />
                </svg>
              </div>
              <div class="text-sm text-gray-500">Erstellen Sie hochwertigen, SEO-optimierten Content, der Ihre Zielgruppe begeistert und Ihre Rankings verbessert.</div>
            </button>
            <button
              :class="tab !== '4' ? 'bg-gray-100 opacity-60 hover:opacity-100 transition' : '[background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] shadow-sm rotate-1'"
              class="text-left px-4 py-5 border border-transparent rounded" @click.prevent="tab = '4'">
              <div class="flex items-center justify-between mb-1">
                <div class="font-inter-tight font-semibold text-gray-900">Keyword-Analyse</div>
                <svg :class="tab !== '4' ? 'hidden' : ''" class="fill-gray-400 shrink-0 ml-2" xmlns="http://www.w3.org/2000/svg" width="10" height="10">
                  <path
                    d="M8.667.186H2.675a.999.999 0 0 0 0 1.998h3.581L.971 7.469a.999.999 0 1 0 1.412 1.412l5.285-5.285v3.58a.999.999 0 1 0 1.998 0V1.186a.999.999 0 0 0-.999-.999Z" />
                </svg>
              </div>
              <div class="text-sm text-gray-500">Identifizieren Sie die Schlüsselwörter, die Ihnen den meisten Traffic und die besten Leads bringen.</div>
            </button>
            <button
              :class="tab !== '5' ? 'bg-gray-100 opacity-60 hover:opacity-100 transition' : '[background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] shadow-sm rotate-1'"
              class="text-left px-4 py-5 border border-transparent rounded" @click.prevent="tab = '5'">
              <div class="flex items-center justify-between mb-1">
                <div class="font-inter-tight font-semibold text-gray-900">Systemintegration</div>
                <svg :class="tab !== '5' ? 'hidden' : ''" class="fill-gray-400 shrink-0 ml-2" xmlns="http://www.w3.org/2000/svg" width="10" height="10">
                  <path
                    d="M8.667.186H2.675a.999.999 0 0 0 0 1.998h3.581L.971 7.469a.999.999 0 1 0 1.412 1.412l5.285-5.285v3.58a.999.999 0 1 0 1.998 0V1.186a.999.999 0 0 0-.999-.999Z" />
                </svg>
              </div>
              <div class="text-sm text-gray-500">Verknüpfen Sie Ihre Systeme nahtlos für eine effizientere Verwaltung Ihrer SEO-Aktivitäten.</div>
            </button>
            <button
              :class="tab !== '6' ? 'bg-gray-100 opacity-60 hover:opacity-100 transition' : '[background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] shadow-sm rotate-1'"
              class="text-left px-4 py-5 border border-transparent rounded" @click.prevent="tab = '6'">
              <div class="flex items-center justify-between mb-1">
                <div class="font-inter-tight font-semibold text-gray-900">Off-Page SEO</div>
                <svg :class="tab !== '6' ? 'hidden' : ''" class="fill-gray-400 shrink-0 ml-2" xmlns="http://www.w3.org/2000/svg" width="10" height="10">
                  <path
                    d="M8.667.186H2.675a.999.999 0 0 0 0 1.998h3.581L.971 7.469a.999.999 0 1 0 1.412 1.412l5.285-5.285v3.58a.999.999 0 1 0 1.998 0V1.186a.999.999 0 0 0-.999-.999Z" />
                </svg>
              </div>
              <div class="text-sm text-gray-500">Erhöhen Sie Ihre Reichweite und Autorität durch gezielte Off-Page-Strategien und Backlinks.</div>
            </button>
          </div>
          <!-- Tabs items -->
          <div class="relative lg:max-w-none [mask-image:linear-gradient(white_0%,white_calc(100%-40px),_transparent_calc(100%-1px))] -mx-6">
            <div class="relative flex flex-col pt-12 md:pt-20 mx-6">
              <!-- Item 1 -->
              <transition enter-active-class="transition ease-in-out duration-700 transform order-first"
                enter-from-class="opacity-0 -translate-y-4" enter-to-class="opacity-100 translate-y-0"
                leave-active-class="transition ease-in-out duration-300 transform absolute"
                leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-4">
                <div class="w-full text-center" v-show="tab === '1'">
                  <p class="text-lg text-gray-500 pb-4 text-left sm:text-center">Technische Optimierung ist das Fundament Ihrer Webseite. Wir kümmern uns um alles, von der sitemap.xml und robots.txt bis hin zu HTTPS-Implementierungen und der Optimierung von Indizierungsseiten. So wird Ihre Webseite von Google als technisch einwandfrei bewertet und erhält die Sichtbarkeit, die sie verdient. Komplex? Wir haben die Erfahrung und das Know-how, um Ihre Webseite nach vorn zu bringen.</p>
                  <div class="inline-flex relative align-top">
                    <img
                      class="rounded-t-lg border border-transparent [background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] box-content shadow-2xl"
                      src="/images/Wireframe.webp" width="600" height="360" alt="Feature 01" />
                  </div>
                </div>
              </transition>
              <!-- Item 2 -->
              <transition enter-active-class="transition ease-in-out duration-700 transform order-first"
                enter-from-class="opacity-0 -translate-y-4" enter-to-class="opacity-100 translate-y-0"
                leave-active-class="transition ease-in-out duration-300 transform absolute"
                leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-4">
                <div class="w-full text-center" v-show="tab === '2'">
                  <p class="text-lg text-gray-500 pb-4 text-left sm:text-center">Ihre Webseite sieht großartig aus, aber haben Sie auch die unsichtbaren Elemente optimiert? Meta-Tags, Titel und Beschreibungen sind entscheidend für Ihre Platzierung in den Suchergebnissen. Wir sorgen dafür, dass Ihre On-Page-SEO perfekt aufeinander abgestimmt ist, damit Ihre Webseite die Aufmerksamkeit bekommt, die sie verdient.</p>
                  <div class="inline-flex relative align-top">
                    <img
                      class="rounded-t-lg border border-transparent [background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] box-content shadow-2xl"
                      src="/images/Keywords.webp" width="600" height="360" alt="Feature 02" />
                  </div>
                </div>
              </transition>
              <!-- Item 3 -->
              <transition enter-active-class="transition ease-in-out duration-700 transform order-first"
                enter-from-class="opacity-0 -translate-y-4" enter-to-class="opacity-100 translate-y-0"
                leave-active-class="transition ease-in-out duration-300 transform absolute"
                leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-4">
                <div class="w-full text-center" v-show="tab === '3'">
                  <p class="text-lg text-gray-500 pb-4 text-left sm:text-center">„Content is King!“ Hochwertige Inhalte sind das Herzstück Ihrer SEO-Strategie. Unsere Experten erstellen maßgeschneiderten Content, der nicht nur Ihre Zielgruppe anspricht, sondern auch Ihre Position in den Suchergebnissen stärkt. Ihre Inhalte werden zur wertvollen Ressource für Ihre Nutzer und zu einem starken Wettbewerbsfaktor.</p>
                  <div class="inline-flex relative align-top">
                    <img
                      class="rounded-t-lg border border-transparent [background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] box-content shadow-2xl"
                      src="/images/Blog.webp" width="600" height="360" alt="Feature 03" />
                  </div>
                </div>
              </transition>
              <!-- Item 4 -->
              <transition enter-active-class="transition ease-in-out duration-700 transform order-first"
                enter-from-class="opacity-0 -translate-y-4" enter-to-class="opacity-100 translate-y-0"
                leave-active-class="transition ease-in-out duration-300 transform absolute"
                leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-4">
                <div class="w-full text-center" v-show="tab === '4'">
                  <p class="text-lg text-gray-500 pb-4 text-left sm:text-center">Die richtige Keyword-Analyse ist der Schlüssel zu erfolgreichen SEO-Kampagnen. Unsere Experten identifizieren die Keywords, die Ihren Traffic und Ihre Konversionen steigern. Mit einer gezielten Keyword-Strategie sorgen wir dafür, dass Ihre Inhalte genau das richtige Publikum erreichen.</p>
                  <div class="inline-flex relative align-top">
                    <img
                      class="rounded-t-lg border border-transparent [background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] box-content shadow-2xl"
                      src="/images/SEO-Analysis.webp" width="600" height="360" alt="Feature 04" />
                  </div>
                </div>
              </transition>
              <!-- Item 5 -->
              <transition enter-active-class="transition ease-in-out duration-700 transform order-first"
                enter-from-class="opacity-0 -translate-y-4" enter-to-class="opacity-100 translate-y-0"
                leave-active-class="transition ease-in-out duration-300 transform absolute"
                leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-4">
                <div class="w-full text-center" v-show="tab === '5'">
                  <p class="text-lg text-gray-500 pb-4 text-left sm:text-center">Um den Erfolg Ihrer SEO-Maßnahmen zu maximieren, ist die nahtlose Integration von Analyse-Tools und Systemen entscheidend. Ob Google Analytics, Search Console oder andere Plattformen – wir sorgen dafür, dass Sie alle notwendigen Daten zur Hand haben, um Ihre Performance ständig zu überwachen und zu verbessern.</p>
                  <div class="inline-flex relative align-top">
                    <img
                      class="rounded-t-lg border border-transparent [background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] box-content shadow-2xl"
                      src="/images/SeoTools.webp" width="600" height="360" alt="Feature 05" />
                  </div>
                </div>
              </transition>
              <!-- Item 6 -->
              <transition enter-active-class="transition ease-in-out duration-700 transform order-first"
                enter-from-class="opacity-0 -translate-y-4" enter-to-class="opacity-100 translate-y-0"
                leave-active-class="transition ease-in-out duration-300 transform absolute"
                leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-4">
                <div class="w-full text-center" v-show="tab === '6'">
                  <p class="text-lg text-gray-500 pb-4 text-left sm:text-center">Backlinks sind ein entscheidender Faktor für das Google-Ranking. Mit einer fundierten Backlink-Strategie von hochwertigen Quellen steigern wir Ihre Autorität und Sichtbarkeit in den Suchergebnissen. Qualitativ hochwertige Backlinks bringen Ihre Webseite ganz nach vorne.</p>
                  <div class="inline-flex relative align-top">
                    <img
                      class="rounded-t-lg border border-transparent [background:linear-gradient(theme(colors.white),theme(colors.white))_padding-box,linear-gradient(120deg,theme(colors.gray.300),theme(colors.gray.100),theme(colors.gray.300))_border-box] box-content shadow-2xl"
                      src="/images/Backlinks.webp" width="600" height="360" alt="Feature 06" />
                  </div>
                </div>
              </transition>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
