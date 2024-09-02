<script setup>
import { ref, onMounted, watch } from 'vue'
import Tooltip from './Tooltip.vue';
import Accordion from './Accordion.vue'

const prices = [
  {
    contacts: '40%',
    plans: {
      essential: '500',
      premium: '450',
      enterprise: '475'
    }
  },
  {
    contacts: '50%',
    plans: {
      essential: '500',
      premium: '550',
      enterprise: '575'
    }
  },
  {
    contacts: '60%',
    plans: {
      essential: '500',
      premium: '550',
      enterprise: '590'
    }
  },
  {
    contacts: '70%',
    plans: {
      essential: '700',
      premium: '750',
      enterprise: '775'
    }
  },
  {
    contacts: '80%',
    plans: {
      essential: '800',
      premium: '850',
      enterprise: '875'
    }
  },
]

const tier = ref('2')
const segmentsWidth = ref('100%')
const progress = ref('0%')
const segments = prices.length - 1;

const calculateProgress = () => {
  segmentsWidth.value = `${100 / segments}%`;
  progress.value = `${100 / segments * tier.value}%`;
}

onMounted(() => {
  calculateProgress()
})

watch(
  () => tier.value,
  () => {
    calculateProgress()
  }
)

const faqs = [
  {
    "title": "Welche Dienstleistungen bietet TillTech an?",
    "text": "TillTech bietet ein umfassendes Spektrum an SEO-Dienstleistungen, sowohl in der Schweiz als auch international. Unsere Services umfassen Keyword-Recherche, technische SEO-Optimierung, On- und Off-Page-Optimierung, Content-Erstellung sowie maßgeschneiderte lokale SEO-Strategien.",
    "active": true
  },
  {
    "title": "Für welche Unternehmen ist die Zusammenarbeit mit einer SEO-Agentur sinnvoll?",
    "text": "Egal ob Start-up, KMU oder Großunternehmen – die Zusammenarbeit mit einer SEO-Agentur wie TillTech bringt für jedes Unternehmen Vorteile, unabhängig von Größe, Branche oder Marktstellung. In der digitalen Ära ist die Sichtbarkeit in Suchmaschinen wie Google entscheidend für den Erfolg. Wir helfen Ihnen dabei, Ihre Online-Präsenz zu stärken und in den Suchergebnissen ganz oben zu stehen.",
    "active": false
  },
  {
    "title": "Wie beeinflusst die kulturelle und sprachliche Vielfalt der Schweiz die Arbeit von TillTech?",
    "text": "Die Schweiz ist ein Land der Vielfalt, und das spiegelt sich in unserer Arbeit wider. Bei TillTech berücksichtigen wir die sprachlichen und kulturellen Unterschiede, um unsere SEO-Strategien optimal an verschiedene Zielgruppen und Regionen anzupassen. So maximieren wir die Reichweite und Wirksamkeit Ihrer Kampagnen.",
    "active": false
  },
  {
    "title": "Worauf sollte man bei der Auswahl einer SEO-Agentur achten?",
    "text": "Ein entscheidender Punkt, insbesondere in der Schweiz, ist die Mehrsprachigkeit. Bei TillTech sprechen wir neben Deutsch auch Italienisch, Französisch und Englisch, was es uns ermöglicht, Ihre Zielgruppen in den verschiedenen Landesteilen gezielt anzusprechen. Wichtig ist auch, dass die Agentur ein ganzheitliches Leistungsspektrum bietet – von der technischen SEO über Content-Erstellung bis hin zu Off-Page-Strategien. Wir bei TillTech kombinieren technisches Know-how mit innovativen SEO-Ansätzen, um sicherzustellen, dass Ihre Webseite nicht nur gut funktioniert, sondern auch in den Suchergebnissen heraussticht. Achten Sie darauf, dass Ihre Agentur auf dem neuesten Stand ist und aktuelle Trends wie AI-basierte Suche (KI-Suche) aktiv in ihre Strategien einbindet.",
    "active": false
  },
  {
    "title": "Wie sieht der Prozess aus?",
    "text": "Unser Prozess beginnt mit einer detaillierten Analyse Ihrer Webseite, gefolgt von einer maßgeschneiderten SEO-Strategie, die genau auf Ihre Ziele abgestimmt ist. Danach setzen wir die Strategie in klar definierten Schritten um und überwachen kontinuierlich die Ergebnisse, um sicherzustellen, dass Sie die bestmöglichen Ergebnisse erzielen.",
    "active": false
  }
]


</script>

<template>
  <section id="pricing">
    <div class="py-12 md:py-20">
      <div class="max-w-6xl mx-auto px-4 sm:px-6">
        <div class="relative max-w-3xl mx-auto text-center pb-12">
          <h2 class="font-inter-tight text-3xl md:text-4xl font-bold text-gray-900 mb-4">Wie weit möchten Sie wachsen?
          </h2>
          <p class="text-lg text-gray-500">Wählen Sie aus, wie groß Ihr Wachstum sein soll und wie weit Sie Ihr
            Unternehmen skalieren möchten. Unser Durschnittlicher Wachstum pro Kunde liegt je nach Monat bei 40-80%!</p>
        </div>


        <!-- Pricing tabs component -->
        <div class="pb-12 md:pb-20">



          <div class="max-w-sm mx-auto grid gap-6 lg:grid-cols-3 items-start lg:max-w-none">

            <!-- Pricing tab 1 -->
            <div class="h-full">
              <div
                class="relative flex flex-col h-full p-6 rounded-lg border border-transparent [background:linear-gradient(theme(colors.zinc.50),theme(colors.zinc.50))_padding-box,linear-gradient(120deg,theme(colors.zinc.300),theme(colors.zinc.100),theme(colors.zinc.300))_border-box]">
                <div class="mb-4">
                  <div class="text-lg text-zinc-900 font-semibold mb-1">Essential</div>
                  <div class="font-inter-tight inline-flex items-baseline mb-2">
                    <span class="text-zinc-900 font-bold text-2xl">CHF</span>
                    <span class="text-zinc-900 font-bold text-3xl">{{ prices[tier].plans.essential }}</span>
                    <span class="text-zinc-500 font-medium">/mo</span>
                  </div>
                  <div class="text-zinc-500">Ideal für Unternehmen, die einen einfachen Einstieg in die Welt de SEO's
                    suchen.</div>
                </div>
                <div class="grow">
                  <div class="text-sm text-zinc-900 font-medium mb-4">Inhalt:</div>
                  <ul class="text-zinc-600 dark:text-zinc-400 text-sm space-y-3 grow">
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="01" content="500 Wörter pro Artikel">
                        2 Blog Artikel pro Monat
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="02" content="20 Keywords">
                        Keyword Recherche und Optimierung
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="03" content="Egal welche Seiten">
                        On-Page SEO für 5 Seiten
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="04" content="Direkt per E-Mail oder Zoom Call">
                        Wöchentliches Reporting & Analysen
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="05" content="Webseiten Optimierung">
                        Grundlegende Technische SEO Überprüfungen
                      </Tooltip>
                    </li>

                  </ul>
                </div>
                <div class="mt-8">
                  <a class="btn text-zinc-100 bg-gradient-to-r from-zinc-700 to-zinc-900 hover:from-zinc-900 hover:to-zinc-900 w-full shadow"
                    href="https://buy.stripe.com/8wM29zbA64WX8r69AN">
                    Jetzt Starten
                  </a>
                </div>
              </div>
            </div>

            <!-- Pricing tab 2 -->
            <div class="h-full">
              <div class="relative flex flex-col h-full p-6 rounded-lg bg-zinc-800">
                <img class="absolute right-6 -top-5 mix-blend-exclusion" src="/images/pricing-decoration.png"
                  alt="Pricing decoration" width="76" height="74" aria-hidden="true">
                <div class="mb-4">
                  <div class="text-lg text-zinc-200 font-semibold mb-1">Premium</div>
                  <div class="font-inter-tight inline-flex items-baseline mb-2">
                    <span class="text-zinc-200 font-bold text-2xl">CHF</span>
                    <span class="text-zinc-200 font-bold text-3xl">{{ prices[tier].plans.premium }}</span>
                    <span class="text-zinc-500 font-medium">/mo</span>
                  </div>
                  <div class="text-zinc-500">Für Unternehmen, die umfassendes Wachstum und Unterstützung in der
                    SEO-Strategie wünschen.</div>
                </div>
                <div class="grow">
                  <div class="text-sm text-zinc-200 font-medium mb-4">Inhalt:</div>
                  <ul class="text-zinc-600 dark:text-zinc-400 text-sm space-y-3 grow">
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="07" content="750 Wörter pro Artikel" dark>
                        4 Blog-Artikel pro Monat
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="08" content="20 Keywords" dark>
                        Erweiterte Keyword-Recherche und -Optimierung
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="09" content="Egal welche Seiten" dark>
                        On-Page SEO für 10 Seiten
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="10" content="Direkt per E-Mail oder Zoom" dark>
                        Wöchentliches Reporting & detaillierte Analysen
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="11" content="Immer auf dem neusten Stand!" dark>
                        Technische SEO-Überprüfung und Fehlerbehebung
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="12" content="Für die Optimale Performance" dark>
                        Linkbuilding-Strategie
                      </Tooltip>
                    </li>

                  </ul>
                </div>
                <div class="mt-8">
                  <a class="btn text-zinc-600 bg-white hover:text-zinc-900 w-full shadow"
                    href="https://buy.stripe.com/4gw5lLaw2611ePu4gu">
                    Jetzt Starten
                  </a>
                </div>
              </div>
            </div>

            <!-- Pricing tab 3 -->
            <div class="h-full">
              <div
                class="relative flex flex-col h-full p-6 rounded-lg border border-transparent [background:linear-gradient(theme(colors.zinc.50),theme(colors.zinc.50))_padding-box,linear-gradient(120deg,theme(colors.zinc.300),theme(colors.zinc.100),theme(colors.zinc.300))_border-box]">
                <div class="mb-4">
                  <div class="text-lg text-zinc-900 font-semibold mb-1">Enterprise</div>
                  <div class="font-inter-tight inline-flex items-baseline mb-2">
                    <span class="text-zinc-900 font-bold text-2xl">CHF</span>
                    <span class="text-zinc-900 font-bold text-3xl">{{ prices[tier].plans.enterprise }}</span>
                    <span class="text-zinc-500 font-medium">/mo</span>
                  </div>
                  <div class="text-zinc-500">Für Unternehmen, die maximalen Wachstum und Unterstützung in der
                    SEO-Strategie wünschen.</div>
                </div>
                <div class="grow">
                  <div class="text-sm text-zinc-900 font-medium mb-4">Inhalt:</div>
                  <ul class="text-zinc-600 dark:text-zinc-400 text-sm space-y-3 grow">
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="13" content="1000 Wörter pro Artikel">
                        6 Blog-Artikel pro Monat
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="14" content="40 Keywords">
                        Umfassende Keyword-Recherche und -Optimierung
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="15" content="Jede Seite auf Ihrer Webseite">
                        On-Page SEO für unbegrenzte Seiten
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="16" content="Direkt per Zoom oder E-Mail">
                        Wöchentliches Reporting & umfassende Analysen
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="17" content="Immer einen Schritt voraus">
                        Vollständige technische SEO-Überprüfung und fortlaufende Optimierung
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="18" content="Immer Top 1 Performance">
                        Umfassende Linkbuilding-Strategie
                      </Tooltip>
                    </li>
                    <li class="flex items-center">
                      <svg class="w-3 h-3 fill-emerald-500 mr-3 shrink-0" viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M10.28 2.28L3.989 8.575 1.695 6.28A1 1 0 00.28 7.695l3 3a1 1 0 001.414 0l7-7A1 1 0 0010.28 2.28z" />
                      </svg>
                      <Tooltip id="12" content="Ein Experte mit langjähriger SEO Erfahrung" dark>
                        Persönlicher SEO-Manager
                      </Tooltip>
                    </li>
                  </ul>
                </div>
                <div class="mt-8">
                  <a class="btn text-zinc-100 bg-gradient-to-r from-zinc-700 to-zinc-900 hover:from-zinc-900 hover:to-zinc-900 w-full shadow"
                    href="https://buy.stripe.com/14k4hHaw21KL7n200f">
                    Jetzt Starten
                  </a>
                </div>
              </div>
            </div>

          </div>

        </div>

        <!-- FAQs -->
        <div class="max-w-2xl mx-auto">
          <div class="space-y-2">
            <template v-for="(faq, index) in faqs">
              <Accordion :title="faq.title" :id="`faqs-${index}`" :active="faq.active">
                {{ faq.text }}
              </Accordion>
            </template>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>
