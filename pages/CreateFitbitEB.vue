<template>
    <div class="relative bg-gray-50">
        <div class="relative bg-white shadow">
            <div class="max-w-7xl mx-auto px-4 sm:px-6">
                <div class="flex justify-between items-center py-6 md:justify-start md:space-x-10">
                    <div class="flex justify-start lg:w-0 lg:flex-1">
                        <NuxtLink to="/">
                            <span class="sr-only">Workflow</span>
                            <img class="h-8 w-auto sm:h-20" src="@/static/RaspiKidd.svg" alt="Logo">
                        </NuxtLink>
                    </div>
          
                    <div class="-mr-2 -my-2 md:hidden">
                        <button type="button" class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-red-500">
                            <span class="sr-only">Open menu</span>
                        </button>
                    </div>

                    <!-- Desktop Menu -->
                    <nav class="hidden md:flex space-x-10">
                        <div class="relative">
                        <!-- Item active: "text-gray-900", Item inactive: "text-gray-500" -->
                            <button type="button" @click="isOpen =!isOpen" class="group bg-white rounded-md text-gray-500 inline-flex items-center text-base font-medium hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500">
                                <span> Tutorials </span>
                                <svg class="ml-2 h-5 w-5 text-gray-400 group-hover:text-gray-500" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                                    <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                                </svg>
                            </button>

                            <transition
                                enter-active-class="transition ease-out duration-200 transform"
                                enter-class="opacity-0 translate-y-1"
                                enter-to-class="opacity-100 translate-y-0"
                                leave-active-class="transition ease-in duration-150"
                                leave-class="opacity-100 translate-y-0"
                                leave-to-class="opacity-0 translate-y-1"
                            >
                                <div v-show="isOpen" class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg">
                                    <div class="rounded-md bg-white shadow-xs">
                                        <!-- Snipped  -->
                                        <div class="absolute -ml-4 mt-3 transform z-10 px-2 w-screen max-w-md sm:px-0 lg:ml-0 lg:left-1/2 lg:-translate-x-1/2">
                                            <div class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 overflow-hidden">
                                                <div class="relative grid gap-6 bg-white px-5 py-6 sm:gap-8 sm:p-8">
                      
                                                    <!-- <NuxtLink to="/RaspberryPi" class="-m-3 p-3 flex items-start rounded-lg hover:bg-gray-50">
                                                        <img class="flex-shrink-0 h-6 w-6" src="@/static/images/RaspberryPi.png" alt="Image of a Raspberry Pi">
                                                        <div class="ml-4">
                                                            <p class="text-base font-medium text-gray-900">
                                                                Raspberry Pi
                                                            </p>
                                                            <p class="mt-1 text-sm text-gray-500">
                                                                Raspberry Pi Tutorials
                                                            </p>
                                                        </div>
                                                    </NuxtLink> -->

                                                    <NuxtLink to="/microbit" class="-m-3 p-3 flex items-start rounded-lg hover:bg-gray-50">
                                                        <img class="flex-shrink-0 h-6 w-6" src="@/static/images/microbit.png" alt="Image of a micro:bit">
                                                        <div class="ml-4">
                                                            <p class="text-base font-medium text-gray-900">
                                                                micro:bit
                                                            </p>
                                                            <p class="mt-1 text-sm text-gray-500">
                                                                BBC micro:bit Tutorials
                                                            </p>
                                                        </div>
                                                    </NuxtLink>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </transition>
                        </div>
        
                        <NuxtLink to="/About" class="text-base font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500">
                            About
                        </NuxtLink>

                        <a href="https://blog.raspikidd.com/" class="text-base font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500">
                            Blog
                        </a>

                        <NuxtLink to="/HireMe" class="text-base font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500">
                            Hire Us
                        </NuxtLink>
                    </nav>
                    <!-- Desktop Menu END -->
                </div>
                
                <!-- Mobile Menu -->
                <div class="absolute top-0 inset-x-0 z-10 p-2 transition transform origin-top-right md:hidden">
                    <div class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 bg-white divide-y-2 divide-gray-50">
                        <div class="pt-5 pb-6 px-5">
                            <div class="flex items-center justify-between">
                                <NuxtLink to="/">
                                    <img class="h-8 w-auto sm:h-10" src="@/static/RaspiKidd.svg" alt="Logo">
                                </NuxtLink>
                                <div class="-mr-2">
                                    <button type="button" @click="isOpen = !isOpen" class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500">
                                        <span class="sr-only">Open menu</span>
                                        <svg class="h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                                        </svg>
                                    </button>
                                    <transition
                                        enter-active-class="duration-200 ease-out"
                                        enter-class="opacity-0 scale-95"
                                        enter-to-class="opacity-100 scale-100"
                                        leave-active-class="duration-100 ease-in"
                                        leave-class="opacity-100 scale-100"
                                        leave-to-class="opacity-0 scale-95"
                                    >
                                        <div v-show="isOpen" class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg">
                                            <div class="rounded-md bg-white shadow-xs">
                                                <div class="mt-6">
                                                    <nav class="grid gap-y-8">
                                                        <!-- <NuxtLink to="/RaspberryPi" class="rounded-t bg-white hover:bg-gray-400 -m-3 p-3 flex items-start rounded-lg hover:bg-gray-50">
                                                            <img class="flex-shrink-0 h-6 w-6" src="@/static/images/RaspberryPi.png" alt="Raspberry Pi Image">
                                                            <div class="ml-4">
                                                                <p class="text-base font-medium text-gray-900">
                                                                    Raspberry Pi Tutorials
                                                                </p>
                                                            </div>
                                                        </NuxtLink> -->
        
                                                        <NuxtLink to="/microbit" class="rounded-t bg-white hover:bg-gray-400 -m-3 p-3 flex items-start rounded-lg hover:bg-gray-50">
                                                            <img class="flex-shrink-0 h-6 w-6" src="@/static/images/microbit.png" alt="micro:bit Image">
                                                            <div class="ml-4">
                                                                <p class="text-base font-medium text-gray-900">
                                                                    micro:bit Tutorials
                                                                </p>
                                                            </div>
                                                        </NuxtLink>
        
                                                        <NuxtLink to="/About" class="text-base font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500 p-3">
                                                            About
                                                        </NuxtLink>
                      
                                                        <a href="https://blog.raspikidd.com/" class="text-base font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500 p-3">
                                                            Blog
                                                        </a>

                                                        <NuxtLink to="/HireMe" class="text-base font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500 p-3">
                                                            Hire Us
                                                        </NuxtLink>
                                                    </nav>
                                                </div>
                                            </div>
                                        </div>
                                    </transition>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
              </div>
            </div>

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
              <h1 class="text-4xl tracking-tight font-extrabold text-gray-900 sm:text-5xl md:text-6xl lg:text-5xl xl:text-6xl text-red-700">
                Create Your Own Fitbit
              </h1>
              <p class="mt-8 text-xl font-bold leading-8" style="color:#006494">
               We are all familiar with Fitbit and other smart watches even our phones counting our steps throughout the day. Let’s use a micro:bit to code our own.
              </p>
            </div>
    
            <div class="mt-6 prose prose-indigo prose-lg text-gray-500 mx-auto">
              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                What You Will Learn
              </h2>
              <p> How to </p>
              <ul>
                <li> Create and use a variable. </li>
                <li> The micro:bit shake function. </li>
                <li> Use a while True loop. </li>
                <li> Display a number on the LED matrix. </li>
                <li> Use the button function. </li>
              </ul>

              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                What You Will Need
              </h2>
              <ul>
                <li> 1 x micro:bit. </li>
                <li> 1 x micro USB cable. </li>
                <li> 1 x Battery pack for the micro:bit (optional). </li>
              </ul>
              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                Coding
              </h2>

              <ol>
                <li> Open your favourite browser ( we recommend Google Chrome) Within the address bar of the browser type <i> <a href="https://app.edublocks.org/"> app.edublocks.org </a> </i> and press <i> Enter </i>. This will load the EduBlocks coding environment.</li>
                <li> Click on <i> micro:bit </i> to open the coding editor. </li>
                <li> Click on <i> Basic </i>. Click and drag a <code> from microbit import * </code> block to the code area and drop it or if you are using the new editor attach it to the <code> # start code here </code> block. </li>
                <li> Click on <i> Basic</i>. Click and drag a <code> variable = 0 </code> block to the code area attach it under <code> from microbit import * </code> block. </li>
                <li> 
                  Click on <i> Variable </i> and click on <i> New variable… </i> Give it the name <i> steps </i> press <i> Enter </i>. Click on <i> 1 </i> and type <i> 0 </i>.  
                  <figure>
                    <img class="rounded-lg" src="@/static/images/FitBit_EB_01.png" alt="" width="500" height="500">
                    <figcaption> Initiating the step counter to 0 </figcaption>
                  </figure>
                </li>
                <div class="bg-blue-100 border-l-8 border-blue-400 px-8">
                  <h3 class="text-2xl tracking-tight font-extrabold sm:text-4xl md:text-4xl lg:text-3xl xl:text-4xl" style="color:#006494">
                    What is a variable
                  </h3>
                  <!--<img src="@/static/images/lightbulb.svg" alt="" width="20" height="20"> -->
                  <p class="text-gray-900"> 
                    Think of a variable as a box that stores information that can be used throughout our program. 
                    We give variables a descriptive name so we and others can understand what is going on within our program.
                  </p>
                </div>
                <li> Click on <i> Basic</i>. Click and drag a <code> while True: </code> block to the code area and attach it under <code> steps = 0 </code> block. </li>
                <li> Click on <i> Basic</i>. Click and drag an <code> if True: </code> block to the code area and attach it within the <code> while True: </code> block. </li>
                <li> Click on <i> Accelerometer</i>. Click and drag an <code> accelerometer.is_gesture(‘shake’) </code> block and attach it within the <code> True </code> of the <code> if </code> block. </li>
                <li> Click on <i> Basic</i>. Click and drag a <code> variable = 1 </code> block to the code area and attach it within the <code> if accelerometer.is_gesture(‘shake’) </code> block. Click on <i> Variable </i> and click <i> steps </i>. Click on the <i> = </i> and click <i> += </i>. </li>
                <li> Click on <i> Display</i>. Click and drag a <code> display.scroll(0) </code> block to the code area and attach it under <code> steps += 1 </code> block. </li>
                <li> 
                  Click on <i> Variables</i>. Click and drag a <code> steps </code> block to the code area and attach it within the <code> 0 </code> of the <code> display.scroll </code> block. 
                  <figure>
                    <img class="rounded-lg" src="@/static/images/FitBit_EB_02.png" alt="" width="500" height="500">
                    <figcaption> Increasing the step counter by 1 everytime the micro:bit detects a shake and displays the number of steps on the LED matrix </figcaption>
                  </figure>
                </li>
                <li> Click on <i> Basic</i>. Click and drag an <code> if True(): </code> block to the code area and attach it under the <code> if accelerometer.is_gesture(‘shake’): </code> block. </li>
                <li> Click on <i> Buttons</i>. Click and drag a <code> button_a.is_pressed(): </code> block to the code area and attach it within the <code> True </code> of the <code> if </code> block. </li>
                <li> 
                  Right-click on <i> steps = 0 </i> and click <i> duplicate </i> and attach the duplicated block within the <code> if button_.is_pressed(): </code> block. 
                  <figure>
                    <img class="rounded-lg" src="@/static/images/FitBit_EB_03.png" alt="" width="500" height="500">
                    <figcaption> Resets the step counter to 0 </figcaption>
                  </figure>
                </li>
                <li> Right-click on <code> if button_a.is_pressed(): </code> block and click <i> duplicate </i> and attach it under the <code> if button_a.is_pressed(): </code> block. Click on <i> a </i> and click <i> b </i>. </li>
                <li> Click and drag the <code> steps = 0 </code> block to the left menu to delete it. </li>
                <li> 
                  Right-click on <code> display.scroll(steps) </code> block and click <i> duplicate</i>. Attach the duplicated block within the <code> if button_b.is_pressed(): </code>  block. 
                  <p> This will display the amount of steps you have done so far when you press the B button on the micro:bit. </p>
                </li>
              </ol>

              <p> <b> Completed Code: </b> </p>

              <figure>
                <img class="rounded-lg" src="@/static/images/FitBit_EB_04.png" alt="" width="500" height="500">
                <figcaption> Completed Code </figcaption>
              </figure>

              <p> 
                Now that we have completed the code we need to download it to the micro:bit.
              </p>
              
              <h2 class="text-3xl tracking-tight font-extrabold sm:text-5xl md:text-5xl lg:text-4xl xl:text-5xl" style="color:#76B82A">
                Downloading the Code
              </h2>

              <ol>
                <li> Take the micro USB cable and connect the micro:bit to the computer. </li>
                <li> Click on Download Hex. Click on your micro:bit drive to open it and click save. </li>
              </ol>  

              <p> 
                You have created your own Fitbit step counter why not connect a battery pack and strap your micro:bit to your ankle and go for a walk and see how many steps you have done at the end.
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
              &copy; 2021 RaspiKidd. All rights reserved.
            </p>
          </div>
        </footer>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  /*name: "microbit",*/
  data: () => ({
    isOpen: false,
})
});
</script>