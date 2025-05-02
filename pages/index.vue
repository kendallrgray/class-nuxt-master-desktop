<template>
   <div class="max-7xl mx-auto">
      <!-- Hero Section -->
      <section>
         <div
            class="h-screen w-full bg-cover bg-center relative"
            style="background-image: url('https://images2.alphacoders.com/914/thumb-1920-914664.jpg');"
         >
            <!-- Overlay for better text visibility -->
            <div class="absolute inset-0 bg- bg-opacity-50"></div>

            <!-- Hero content -->
            <div class="relative flex flex-col items-center justify-center h-full text-white text-center">
               <h1 class="text-5xl font-bold mb-4">KENDALL GRAY</h1>
               <p class="text-2xl font-light">Creativity Overload</p>
               <nuxt-link
                  to="/projects"
                  class="bg-green-900/70 hover:bg-black text-white font-bold py-3 px-4 rounded gap-y-5 m-5"
               >
                  Here's Proof
               </nuxt-link>
            </div>
         </div>
      </section>

      <!-- Other Sections -->
      <section class="flex flex-row gap-9 py-12 justify-between">
         <article class="flex-0.5 h-96 w-96 text-black text-2xl text-center py-15">to listen
            <a href="https://open.spotify.com/album/1SePKD46mKjmAuugWuCXug?si=aaEvfXUHTKCbcx7Ug50NQg" target="Another Word for Grateful - Spotify">
               <img src="file:///Users/kendallgray/Desktop/class-nuxt-master-desktop/public/awfgcoverart.png" alt="Another Word for Grateful" class="w-full h-full object-cover" />
            </a>
         </article>
         <article class="flex-0.5 h-96 w-96 text-black text-2xl text-center py-15">to watch
            <a href="https://www.youtube.com/watch?v=7Mrbd14T5Tg" target="A Documentary I made">
               <img src="file:///Users/kendallgray/Desktop/class-nuxt-master-desktop/public/docuclip.gif" alt="I made an album and a documentary about it" class="w-full h-full object-cover" />
            </a>
         </article>
         <article class="flex-0.5 h-96 w-96 text-black text-2xl text-center py-15">to write
            <a href="https://a.co/d/hQ1oZOt" target="Overthinky Journal Prompt Book">
               <img src="file:///Users/kendallgray/Desktop/class-nuxt-master-desktop/public/journalclip.gif" alt="why won't an image load here?" class="w-full h-full object-cover" />
            </a>
         </article>
      </section>
   </div>
</template>