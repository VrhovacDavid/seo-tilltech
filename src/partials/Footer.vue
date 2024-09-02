<template>
  <footer>
    <div class="max-w-6xl mx-auto px-4 sm:px-6">

      <!-- Top area: Blocks -->
      <div class="grid sm:grid-cols-10 gap-8 py-8 md:py-12 border-t border-zinc-200">

        <!-- 1st block -->
        <div class="sm:col-span-6 md:col-span-3 lg:col-span-6 max-sm:order-1 flex flex-col">
          <div class="mb-4">
            <!-- Logo -->
            <router-link class="flex items-center justify-center bg-white w-8 h-8 rounded shadow-sm shadow-zinc-950/20" to="/">
              <img src="/images/TT-Small.svg" width="24" height="24" alt="Logo">
            </router-link>
          </div>
          <div class="grow text-sm text-zinc-500">&copy; tilltech.ch. All rights reserved.</div>
          <div class="grow text-sm text-zinc-500">E-Mail: hello@tilltech.ch</div>
          <!-- Social links -->
         
        </div>

        <!-- 2nd block -->
        <div class="sm:col-span-6 md:col-span-3 lg:col-span-2">
          <h6 class="text-sm text-zinc-800 font-medium mb-2">Unternehmen</h6>
          <ul class="text-sm space-y-2">
            <li>
              <a class="text-zinc-500 hover:text-zinc-900 transition" href="/#pricing">Angebot</a>
            </li>

          </ul>
        </div>


        <!-- 4th block -->
        <div class="sm:col-span-6 md:col-span-3 lg:col-span-2">
          <h6 class="text-sm text-zinc-800 font-medium mb-2">Legals</h6>
          <ul class="text-sm space-y-2">
            <li>
              <a class="text-zinc-500 hover:text-zinc-900 transition" href="https://rainbow-side-8bf.notion.site/Datenschutz-4f35065d70174eba91e6f96ea514e3d0">Datenschutz</a>
            </li>
            <li>
              <a class="text-zinc-500 hover:text-zinc-900 transition" href="https://rainbow-side-8bf.notion.site/AGB-e17deb03fd6543f1a5655de006bbdaf6?pvs=25">AGB</a>
            </li>
            <li>
              <a class="text-zinc-500 hover:text-zinc-900 transition" href="https://rainbow-side-8bf.notion.site/Impressum-c9bf006259e74aafb2f9db0c20bf612f">Impressum</a>
            </li>
            <li>
              <a class="text-zinc-500 hover:text-zinc-900 transition" href="https://rainbow-side-8bf.notion.site/Cookie-Richtlinie-eeb932b267c840c8b56637b20e1dadde">Cookie Richtlinie</a>
            </li>
          </ul>
        </div>

      </div>

    </div>
  </footer>
</template>
