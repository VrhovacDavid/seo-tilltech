<script setup>
import { ref } from 'vue'

const tab = ref('1')
</script>

<template>
    <section class="relative bg-zinc after:absolute  max-lg:after:hidden">
        <div class="py-12 md:py-20">

            <!-- Carousel -->
            <div class="max-w-xl lg:max-w-6xl mx-auto px-4 sm:px-6">
                <div class="lg:flex space-y-12 lg:space-y-0 lg:space-x-12 xl:space-x-24">

                    <!-- Content -->
                    <div class="lg:max-w-none lg:min-w-[524px]">
                        <div class="mb-8">
                            <div
                                class="inline-flex text-sm font-medium text-gray-200 px-4 py-0.5 border border-transparent [background:linear-gradient(theme(colors.gray.800),theme(colors.gray.800))_padding-box,linear-gradient(120deg,theme(colors.gray.700),theme(colors.gray.700/0),theme(colors.gray.700))_border-box] rounded-full mb-4">
                                SEO, made in St. Gallen, powered by TillTech</div>
                            <h3 class="font-inter-tight text-3xl font-bold text-gray-900 mb-4">Moment mal, das gibt's
                                wirklich?</h3>
                            <p class="text-lg text-gray-500">Absolut! Bei TillTech ist SEO nicht nur ein Service, es ist
                                unsere Leidenschaft. Wir leben und atmen SEO.</p>
                            <br>
                            <p class="text-lg text-gray-500">Mal ehrlich: Wenn SEO in der Schweiz so simpel wäre, dass
                                man es nach ein paar YouTube-Tutorials meistern könnte, wäre es kinderleicht, die
                                Top-Rankings bei Google zu erobern.</p>
                            <br>
                            <p class="text-lg text-gray-500">Aber in der Realität ändern sich die über 200 Faktoren des
                                Google-Algorithmus ständig. Viele Agenturen, die SEO nebenbei anbieten, sind längst
                                nicht mehr auf dem aktuellen Stand und laufen Gefahr, an den entscheidenden Updates
                                vorbeizuarbeiten.</p>
                            <br>
                            <p class="text-lg text-gray-500">Wussten sie das Täglich bis zu 15'000 noch nie gefragte
                                Suchbegriffe auf Google gesucht werden?</p>
                            <br>
                            <p class="text-lg text-gray-500">Bei TillTech setzen wir auf Präzision statt Vermutungen:
                                Mit unseren datengestützten Strategien erzielen wir für Sie schnelle und nachhaltige
                                Erfolge.</p>
                        </div>
                    </div>


                    <!-- Tabs items -->
                    <div class="relative lg:max-w-none">
                        <div class="relative flex flex-col">
                            <!-- Item 1 -->
                            <transition enter-active-class="transition ease-in-out duration-700 transform order-first"
                                enter-from-class="opacity-0 translate-x-8" enter-to-class="opacity-100 translate-x-0"
                                leave-active-class="transition ease-in-out duration-300 transform absolute"
                                leave-from-class="opacity-100 translate-x-0" leave-to-class="opacity-0 -translate-x-8">
                                <div class="w-full" v-show="tab === '1'">
                                    <div>
                                        <img class="lg:max-w-none mx-auto rounded-lg shadow-2xl"
                                            src="/images/St.Gallen.webp" width="800" height="620" alt="Carousel 01" />
                                    </div>
                                </div>
                            </transition>


                        </div>
                        <!-- Gear illustration -->
                        <img class="absolute left-0 bottom-0 -translate-x-1/2 translate-y-1/3 mix-blend-exclusion max-lg:w-32"
                            src="/images/features-illustration.png" alt="Features 02 illustration" width="173"
                            height="167" aria-hidden="true">
                    </div>

                </div>
            </div>



        </div>
    </section>
</template>
