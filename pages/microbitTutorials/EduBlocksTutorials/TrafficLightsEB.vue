<template>
    <div class="relative bg-gray-50">
        <Header />
        <!-- main -->
        <div class="relative py-16 bg-white overflow-hidden">
          <div class="hidden lg:block lg:absolute lg:inset-y-0 lg:h-full lg:w-full">
            <div class="relative h-full text-lg max-w-prose mx-auto" aria-hidden="true">
              <img class="absolute top-12 left-full transform translate-x-32" width="404" height="384"  fill="none" viewBox="0 0 404 384" src="@/static/images/circuit-board.svg">
              <img class="absolute top-12 right-full transform -translate-x-32" width="404" height="384"  fill="none" viewBox="0 0 404 384" src="@/static/images/circuit-board.svg">
              <img class="absolute top-1/2 right-full transform -translate-y-1/2 -translate-x-32" width="404" height="384" fill="none" viewBox="0 0 404 384" src="@/static/images/circuit-board.svg">
              <img class="absolute top-1/2 left-full transform -translate-y-1/2 translate-x-32" width="404" height="384" fill="none" viewBox="0 0 404 384" src="@/static/images/circuit-board.svg">
              <img class="absolute bottom-12 left-full transform translate-x-32" width="404" height="384" fill="none" viewBox="0 0 404 384" src="@/static/images/circuit-board.svg">
              <img class="absolute bottom-12 right-full transform -translate-x-32" width="404" height="384" fill="none" viewBox="0 0 404 384" src="@/static/images/circuit-board.svg">
            </div>
          </div>
          <div class="relative px-4 sm:px-6 lg:px-8">
            <div class="text-lg max-w-prose mx-auto">
              <!-- <button type="button" class="inline-flex items-center px-6 py-3 border border-transparent text-base font-medium rounded-full shadow-sm text-white bg-blue-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500">
                <a href = "https://drive.google.com/file/d/1--vTxJfvK012SSbEtNa7jPxxy2kIM-nY/view?usp=sharing" target="_blank"> PDF Download </a>
              </button> -->
              <h1 class="text-4xl tracking-tight font-extrabold text-gray-900 sm:text-5xl md:text-6xl lg:text-5xl xl:text-6xl text-red-700">
                Traffic Lights Add-on Board
              </h1>
              <p class="mt-8 text-xl font-bold leading-8" style="color:#006494">
               Create your own micro:bit traffic light add-on board.
              </p>
            </div>
    
            <div class="mt-6 prose prose-indigo prose-lg text-gray-500 mx-auto">

              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                Overview
              </h2>
            
              <p>
                  By the end of this tutorial you will know what an LED is and how to connect and program them using a BBC micro:bit.
              </p>

              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                What You Will Need
              </h2>

              <ul>
                <li> 1 x Red LED </li>
                <li> 1 x Yellow LED </li>
                <li> 1 x Green LED </li>
                <li> 1 x Piece of cardboard </li>
                <li> Copper tape / aluminium foil and glue </li>
                <li> 4 x Crocodile / alligator leads </li>
                <li> 1 x micro:bit (version 1 and 2 will work) </li>
                <li> 1 x Micro USB cable </li>
                <li> 1 x Battery pack for the micro:bit (optional) </li>
              </ul>

              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                What is an LED?
              </h2>

              <figure>
                <img class="rounded-lg" src="@/static/images/LEDDiagram.png" alt="" width="300" height="300">
                <figcaption> LED diagram </figcaption>
              </figure>

              <p> 
               An LED or Light Emitting Diode is a semiconductor light source that emits (gives off) light when current flows through it.
              </p>

              <p>
                An LED has a longer leg called the anode (+) and a shorter leg called the cathode (-) as shown above.
              </p>

              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                Creating the Circuit
              </h2>

              <ol>
                <li> Place the bit of cardboard on the desk</li>
                <li> Take the red LED and bend the legs out to the sides. Place the LED on the cardboard with the longer leg to the right. 
                  <figure>
                    <img class="rounded-lg" src="@/static/images/TrafficLights01.jpg" alt="" width="300" height="300">
                    <figcaption> Red LED placed on the cardboard </figcaption>
                  </figure>
                </li>
                <li> Take a bit of copper tape or glue and some aluminium foil over the long leg of the red LED
                  <figure>
                    <img class="rounded-lg" src="@/static/images/TrafficLights02.jpg" alt="" width="300" height="300">
                    <figcaption> Taping the longer leg of the red LED </figcaption>
                  </figure>
                </li>
                <li> Complete steps 2 and 3 for the yellow and green LEDs. </li>
                <li> Take a longer bit of copper tape or foil and tape/glue all three of the short legs of the LEDs together.
                  <figure>
                    <img class="rounded-lg" src="@/static/images/TrafficLights03.jpg" alt="" width="300" height="300">
                    <figcaption> Completed Traffic lights </figcaption>
                  </figure>
                </li>
              </ol>

              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                Connecting to the micro:bit
              </h2>

              <ol>
                <li> Take one of the crocodile/alligator leads and clip one end to the long piece of copper tape/aluminium foil covering the short legs of the LEDs and clip the other end to the GND pin of the micro:bit. </li>
                <li> Take another crocodile/alligator lead and clip one end to the copper tape/aluminium foil of the longer leg of the red LED and attach the other end to pin 0 on the micro:bit. </li>
                <li> Take another crocodile/alligator lead and clip one end to the copper tape/aluminium foil of the longer leg of the yellow LED and attach the other end to pin 1 on the micro:bit. </li>
                <li> Take the last crocodile/alligator lead and clip one end to the copper tape/aluminium foil of the longer leg of the green LED and attach the other end to pin 2 on the micro:bit. </li>
              </ol>

              <figure>
                    <img class="rounded-lg" src="@/static/images/TrafficLights04.jpeg" alt="" width="300" height="300">
                    <figcaption> Completed Circuit </figcaption>
                  </figure>
              <p>
                We are now ready to code our traffic lights
              </p>

              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                Coding The Traffic Lights
              </h2>

              <ol>
                <li> Within your favourite browser (we recommend Google Chrome) go to <a href = https://app.edublocks.org/> <i> app.edublocks.org </i> </a> and press <i> Enter </i>. This will load the EduBlocks coding environment. </li>
                <li> Click on <i> micro:bit </i> and click <i> start coding </i> to open the EduBlocks coding editor for micro:bit. </li>
                <li> Click on <i> Basic </i>. Click and drag a <i> from microbit import * </i> block to the code area and drop it or if you are using the new editor attach it to the <i> # start code here </i> block. </li>
                <li> Click on <i> Basic </i>. Click and drag a <i> while True: </i> block to the code area and attach it under the <i> from microbit import * </i> block. </li>
                <li> Click on <i> Pins </i>. Click and drag a <i> pin0.write_digital(0) </i> block to the code area and attach it within the <i> while True: </i> block. </li>
                <li> Click on the 2nd <i> 0 </i> within the <i> pin0.write_digital </i> block and type <i> 1 </i>. </li>
                <li> Click on <i> Basic </i>. Click and drag a <i> sleep (1000) </i> block to the code area and attach it under <i> pin0.write_digital(1) </i> block. Your code should look like this: 
                  <figure>
                    <img class="rounded-lg" src="@/static/images/TrafficLights09.png" alt="" width="300" height="300">
                    <figcaption> Turning the red LED on </figcaption>
                  </figure>
                </li>
                <li> Right-click on <i> pin0.write_digital(1) </i> block and click <i> duplicate </i> attach the <i> duplicated </i> block under <i> sleep (1000) </i> block. Click on the <i> 0 </i> and type <i> 1 </i>. </li>
                <li> Right-click on <i> sleep (1000) </i> and click <i> duplicate </i> attach the <i> duplicated </i> block under the <i> pin1.write_digital(1) </i> block. Your code should look like this: 
                  <figure>
                    <img class="rounded-lg" src="@/static/images/TrafficLights10.png" alt="" width="300" height="300">
                    <figcaption> Turning the yellow LED on </figcaption>
                  </figure>
                </li>
                <li> Right-click on the <i> pin0.write_digital(1) </i> and click <i> duplicate </i> attach the <i> duplicated </i> block under <i> sleep (1000) </i>. Click on <i> 1 </i> and type <i> 0 </i>. </li>
                <li> Right-click on <i> pin1.write_digital(1) </i> and click <i> duplicate </i> attach the <i> duplicated </i> block under <i> pin0.write_digital(0) </i> block. Click on the 2nd <i> 1 </i> and type <i> 0 </i>. </li>
                <li> Right-click on <i> pin1.write_digital(1) </i> block and click <i> duplicate </i> attach the <i> duplicated </i> block under <i> pin1.write_digital(0) </i> block. Click on the 1st <i> 1 </i> and type <i> 2 </i>. </li>
                <li> Right Click on <i> sleep (1000) </i> and click on <i> duplicate </i> attach the <i> duplicated </i> block under <i> pin2.write_digital(1) </i>. Your code should look like this: 
                  <figure>
                    <img class="rounded-lg" src="@/static/images/TrafficLights11.png" alt="" width="300" height="300">
                    <figcaption> Turning the  red and yellow LEDs off and the green LED on </figcaption>
                  </figure>
                </li>
                <li> Right-click on <i> pin2.write_digital(1) </i> and click <i> duplicate </i> attach the <i> duplicated </i> block under <i> sleep (1000) </i>. Click on <i> 1 </i> and type <i> 0 </i>. </li>
                <li> Right-click on <i> pin1.write_digital(1) </i> block and click <i> duplicate </i> attach the <i> duplicated </i> block under <i> pin2.write_digital(0) </i> block. </li>
                <li> Right-click on <i> sleep (1000) </i> and click <i> duplicate </i> attach the <i> duplicated </i> block under <i> pin1.write_digital(1) </i> block. </li>
                <li> Right-click on <i> pin1.write_digital(0) </i> block and click <i> duplicate </i> attach the <i> duplicated </i> block under the <i> sleep (1000) </i> block. </li>
              </ol>

              <figure>
                    <img class="rounded-lg" src="@/static/images/TrafficLights12.png" alt="" width="300" height="300">
                    <figcaption> Completed Code </figcaption>
              </figure>

              <p>
                Now that we have completed the code we need to download it to our micro:bit
              </p>

              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                Downloading the Code
              </h2>

              <ol>
                <li> Attach the micro:bitt to the computer using the micro USB cable. </li>
                <li> Click on the <i> Download Hex </i> button. </li>
                <li> Locate your <i> micro:bit </i> within the <i> file manager </i> and click on it to open the drive and click <i> save </i> to download your code to the micro:bit. </li>
              </ol>  

              <p> 
                Well-done! You have just created and coded your own micro:bit add-on board.
              </p>
            </div>
          </div>
        </div>
          
        <!--footer -->
        <footer class="bg-white">
          <div class="px-4 py-12 mx-auto overflow-hidden max-w-7xl sm:px-6 lg:px-8">
            <div class="flex justify-center mt-8 space-x-6">
              <a 
                href="https://www.facebook.com/RaspiKidd" 
                class="text-gray-400 hover:text-gray-500"
              >
                <span class="sr-only">Facebook</span>
                <svg 
                  class="h-6 w-6" 
                  fill="currentColor" 
                  viewBox="0 0 24 24" 
                  aria-hidden="true"
                > 
                  <path 
                    d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z"
                  />
                </svg>
              </a>

              <a 
                href="https://www.instagram.com/raspikidd/" 
                class="text-gray-400 hover:text-gray-500"
              >
                <span class="sr-only">Instagram</span>
                <svg 
                  class="h-6 w-6" 
                  fill="currentColor" 
                  viewBox="0 0 24 24" 
                  aria-hidden="true"
                >
                  <path 
                    d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z"
                  />
                </svg>
              </a>
          
              <a
                href="https://twitter.com/RaspiKidd"
                class="text-gray-400 hover:text-gray-500"
              >
                <span class="sr-only">Twitter</span>
                <svg
                  class="w-6 h-6"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                  aria-hidden="true"
                >
                  <path
                      d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"
                  />
                </svg>
              </a>

              <a
                href="https://github.com/RaspiKidd"
                class="text-gray-400 hover:text-gray-500"
              >
                <span class="sr-only">GitHub</span>
                <svg
                  class="w-6 h-6"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                  aria-hidden="true"
                >
                  <path
                      fill-rule="evenodd"
                      d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"
                      clip-rule="evenodd"
                  />
                </svg>
              </a>

              <a
                href="mailto:kerry@raspikidd.com"
                class="text-gray-400 hover:text-gray-500"
              >
                <span class="sr-only">GitHub</span>
                <svg class="w-6 h-6" fill="currentColor">
                  <path
                      d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"
                  />
                </svg>
              </a>
            </div>
            <p class="mt-8 text-base text-center text-gray-400">
          &copy; 2022 RaspiKidd. All rights reserved. 
          <a 
          class ="text-blue-500" 
          href= "/privacy_policy.pdf"
          target="_blank"> 
            Privacy Policy 
          </a>
        </p>
          </div>
        </footer>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Header from "~/components/Header.vue";

export default Vue.extend({
    components: { 
      Header 
    }
});
</script>

