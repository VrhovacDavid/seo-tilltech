<script setup>
import Testimonial from '../partials/Testimonial.vue'
import TestimonialImg01 from '/images/MarkusKathriner.webp'
import TestimonialImg02 from '/images/JessicaZeder.webp'
import TestimonialImg03 from '/images/MaximilianMurtinger.webp'
import TestimonialImg04 from '/images/J.png'
import TestimonialImg05 from '/images/S.png'
import TestimonialImg06 from '/images/M.png'
import TestimonialImg07 from '/images/testimonial-07.jpg'
import TestimonialImg08 from '/images/testimonial-08.jpg'

const testimonials01 = [
  {
    image: TestimonialImg01,
    name: 'Markus Kathriner',
    user: '@mk',
    link: '#0',
    content: 'TillTech namentlich David hat uns als User mit Geduld, Struktur, Klarheit und Verständlichkeit binnen kürzester Zeit auf den aktuellsten Stand eines modernen Marketing gebracht.',
  },
  {
    image: TestimonialImg02,
    name: 'Jessica Zeder',
    user: '@JZ',
    link: '#0',
    content: 'Homepage, Graphisches Design, Social Media und KI. Alles komplett verständlich für uns als Kunden. Das hat echtes Vertrauen geschaffen.',
  },
  {
    image: TestimonialImg03,
    name: 'Dr. Maximilian Murtinger',
    user: '@MM',
    link: '#0',
    content: 'David von Tilltech hat uns Schritt für Schritt in die Welt des SEOs für unseren Onlineshop eingeführt. ',
  },
  {
    image: TestimonialImg04,
    name: 'Jonathan Cheek',
    user: '@JC',
    link: '#0',
    content: 'Habe eine sehr gute Zusammenarbeit mit der Firma Till Tech konnten die Zielgruppe analysieren, und dadurch gezielt Werbung schalten. Ihr macht das super gut, weiter so....',
  },  
]

const testimonials02 = [
  {
    image: TestimonialImg05,
    name: 'Stephan Hauser',
    user: '@SH',
    link: '#0',
    content: 'Dank der SEO-Strategien hat sich unser Website-Traffic innerhalb von drei Monaten verdreifacht ❤️. Die Zusammenarbeit war professionell und die Ergebnisse sprechen für sich. Sehr empfehlenswert!',
  },
  {
    image: TestimonialImg06,
    name: 'Karl Ahmed',
    user: '@karl87',
    link: '#0',
    content: 'Die SEO-Optimierungen haben uns geholfen, auf die erste Seite von Google zu kommen. Der Service ist zuverlässig, transparent und liefert genau das, was versprochen wird.',
  },
  {
    image: TestimonialImg07,
    name: 'Carlotta Grech',
    user: '@carlagrech',
    link: '#0',
    content: ' Seit wir den SEO-Service nutzen, haben sich unsere Suchmaschinenrankings erheblich verbessert',
  },
  {
    image: TestimonialImg08,
    name: 'Alejandra Gok',
    user: '@alejandraIT',
    link: '#0',
    content: ' Die Betreuung war von Anfang an großartig, und die Ergebnisse haben unsere Erwartungen übertroffen. Der organische Traffic und die Conversion-Raten haben sich extrem erhöht.',
  },
]
</script>

<template>
  <section class="bg-zinc-800">
    <div class="py-12 md:py-20">
      <div class="max-w-6xl mx-auto px-4 sm:px-6">
        <div class="max-w-3xl mx-auto text-center pb-12 md:pb-20">
          <h2 class="font-inter-tight text-3xl md:text-4xl font-bold text-zinc-200">5 Sterne auf Google und zahlreiche zufriedene Kunden</h2>
        </div>
      </div>
      <div class="max-w-[94rem] mx-auto space-y-6">
        <!-- Row #1 -->
        <div class="w-full inline-flex flex-nowrap overflow-hidden [mask-image:_linear-gradient(to_right,transparent_0,_black_28%,_black_calc(100%-28%),transparent_100%)] group">
          <div class="flex items-start justify-center md:justify-start [&>div]:mx-3 animate-infinite-scroll group-hover:[animation-play-state:paused]">
            <!-- Items -->
            <Testimonial v-for="(testimonial, index) in testimonials01" :key="testimonial.id" :testimonial="testimonial" >
              {{ testimonial.content }}
            </Testimonial>
          </div>
          <!-- Duplicated element for infinite scroll -->
          <div class="flex items-start justify-center md:justify-start [&>div]:mx-3 animate-infinite-scroll group-hover:[animation-play-state:paused]" aria-hidden="true">
            <!-- Items -->
            <Testimonial v-for="(testimonial, index) in testimonials01" :key="testimonial.id" :testimonial="testimonial" >
              {{ testimonial.content }}
            </Testimonial>
          </div>          
        </div>
        <!-- Row #2 -->
        <div class="w-full inline-flex flex-nowrap overflow-hidden [mask-image:_linear-gradient(to_right,transparent_0,_black_28%,_black_calc(100%-28%),transparent_100%)] group">
          <div class="flex items-start justify-center md:justify-start [&>div]:mx-3 animate-infinite-scroll-inverse group-hover:[animation-play-state:paused] [animation-delay:-7.5s]">
            <!-- Items -->
            <Testimonial v-for="(testimonial, index) in testimonials01" :key="testimonial.id" :testimonial="testimonial" >
              {{ testimonial.content }}
            </Testimonial>
          </div>
          <!-- Duplicated element for infinite scroll -->
          <div class="flex items-start justify-center md:justify-start [&>div]:mx-3 animate-infinite-scroll-inverse group-hover:[animation-play-state:paused] [animation-delay:-7.5s]" aria-hidden="true">
            <!-- Items -->
            <Testimonial v-for="(testimonial, index) in testimonials02" :key="testimonial.id" :testimonial="testimonial" >
              {{ testimonial.content }}
            </Testimonial>
          </div>          
        </div>
      </div>
    </div>
  </section>
</template>
