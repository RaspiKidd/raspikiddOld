<template>
  <div v-if="isUnlocked" class="relative bg-gray-50">
    <Header />
    <!-- main -->
    <div class="relative bg-gray-50 pt-16 pb-20 px-4 sm:px-6 lg:pt-24 lg:pb-28 lg:px-8">
      <div class="absolute inset-0">
        <div class="bg-white h-1/3 sm:h-2/3"></div>
      </div>
      
      <div class="relative max-w-7xl mx-auto">
        <div class="text-center">
          <h1 class="text-4xl tracking-tight font-extrabold sm:text-5xl md:text-6xl lg:text-5xl xl:text-6xl" style="color:#A42530">
            Lesson Packs
          </h1>
                
          <!-- <p class="mt-3 max-w-2xl mx-auto text-xl text-gray-500 sm:mt-4">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsa libero labore natus atque, ducimus sed.
          </p> -->
        </div>

        <div class="mt-12 max-w-lg mx-auto grid gap-5 lg:grid-cols-3 lg:max-w-none">
          <NuxtLink to="/GettingStartedMB" class="block mt-2">
            <div class="flex flex-col rounded-lg shadow-lg overflow-hidden">
              <div class="flex-shrink-0">
                <img class="h-48 w-full object-scale-down" src="@/static/images/microbit.png" alt="Rock Paper Scissors image">
              </div>
                    
              <div class="flex-1 bg-white p-6 flex flex-col justify-between">
                <div class="flex-1">
                  <p class="text-xl font-bold" style="color:#A42530">
                    Getting Started Guide
                  </p>
                        
                  <p class="mt-3 text-base text-gray-500">
                    An introduction to the BBC micro:bit and how to program it
                  </p>
                </div>
              </div>
            </div>    
          </NuxtLink>
        </div>
              
        <div class="mt-12 max-w-lg mx-auto grid gap-5 lg:grid-cols-3 lg:max-w-none" style="background-color:#a1c4b5">
          <!-- <NuxtLink to="/TrafficLightsEB" class="block mt-2">
            <div class="flex flex-col rounded-lg shadow-lg overflow-hidden">
              <div class="flex-shrink-0">
                <img class="h-48 w-full object-scale-down" src="@/static/images/TrafficLights03.jpg" alt="carboard traffic lights">
              </div>
                    
              <div class="flex-1 bg-white p-6 flex flex-col justify-between">
                <div class="flex-1">
                  <p class="text-xl font-bold" style="color:#A42530">
                    Traffic Lights add-on board
                  </p>
                      
                  <p class="mt-3 text-base text-gray-500">
                    Create your own micro:bit traffic light add-on board.
                  </p>
                </div>
              </div>
            </div>
          </NuxtLink> -->
              
          <!-- <NuxtLink to="/ThrowGhostEB" class="block mt-2">
            <div class="flex flex-col rounded-lg shadow-lg overflow-hidden">
              <div class="flex-shrink-0">
                <img class="h-48 w-full object-scale-down" src="@/static/images/ThrowGhost_Cover.png" alt="micro:bit ghost icon">
              </div>
                    
              <div class="flex-1 bg-white p-6 flex flex-col justify-between">
                <div class="flex-1">
                  <p class="text-xl font-bold" style="color:#A42530">
                    Throw a Ghost
                  </p>
                    
                  <p class="mt-3 text-base text-gray-500">
                    Exploring the micro:bit radio function by throwing a ghost between 2 micro:bits
                  </p>
                </div>
              </div>
            </div>
          </NuxtLink> -->
        </div>
      </div>
    </div>

    <Footer />
  </div>
</template>

<script lang="ts">
  import Vue from "vue";
  import Header from "~/components/Header.vue";
  import Footer from "~/components/Footer.vue";

  export default Vue.extend({
    mounted() {
      let password;
      const pass1 = "HelloWorld";
      password = prompt("Enter Password", " ");
      if (password === pass1) {
        this.isUnlocked = true;
          alert("Correct Password! Click OK to Enter!");
        }
      else {
        // location.href = "https://dev.raspikidd.com/";
        location.href = "https://raspikidd.com/";
      }
    },
    components: {
      Header,
      Footer
    }
  });
</script>