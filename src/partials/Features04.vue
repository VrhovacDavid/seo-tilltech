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

                            <h3 class="font-inter-tight text-3xl font-bold text-gray-900 mb-4">Warum ist SEO der
                                Schlüssel zum Erfolg Ihrer Webseite?</h3>
                            <p class="text-lg text-gray-500">Sie haben eine beeindruckende, benutzerfreundliche Webseite
                                erstellt, aber der Kundenstrom bleibt aus? Fragen Sie sich, warum Ihre Mitbewerber auf
                                der ersten Seite von Google erscheinen und deutlich mehr Traffic und potenzielle Kunden
                                generieren? Wir kennen die Antwort! – Vom technischen Feinschliff bis hin zu einem
                                soliden Backlink-Profil – SEO ist der Dreh- und Angelpunkt für den Erfolg Ihrer
                                Webseite.</p>
                            <br>

                            <p class="text-lg text-gray-500">Für alle, die online sichtbar sein und Erfolge erzielen
                                möchten, ist SEO ein unverzichtbares Element. Eine durchdachte SEO-Strategie kann
                                bereits nach wenigen Monaten die Position Ihrer Webseite erheblich verbessern und
                                langfristig dafür sorgen, dass Sie auf der ersten Seite von Google stehen. Aber keine
                                Sorge, wir gehen Schritt für Schritt vor.</p>
                            <br>
                            <p class="text-lg text-gray-500">Wir führen Sie durch die wichtigsten Phasen der SEO, um
                                Ihre Webseite auf das nächste Level zu bringen:</p>
                            <br>

                        </div>
                        <!-- Tabs buttons -->

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
                                            src="/images/YouTubeTut.webp" width="800" height="620"
                                            alt="Carousel 01" />
                                    </div>
                                </div>
                            </transition>


                        </div>
                        <!-- Gear illustration -->
                        <img class="absolute left-0 bottom-0 -translate-x-1/2 translate-y-1/3  max-lg:w-32"
                            src="/images/Fire.webp" alt="Features 02 illustration" width="173" height="167"
                            aria-hidden="true">
                    </div>

                </div>
            </div>



        </div>
    </section>
</template>
