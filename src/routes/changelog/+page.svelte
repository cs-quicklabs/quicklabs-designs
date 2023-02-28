<script>
	import Fullnavbar from '../../shared/fullnavbar.svelte';
</script>

<Fullnavbar />
<!--
  This example requires some changes to your config:
  
  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/forms'),
      require('@tailwindcss/line-clamp'),
    ],
  }
  ```
-->
<!--
  This example requires updating your template:

  ```
  <html class="h-full bg-gray-100">
  <body class="h-full overflow-hidden">
  ```
-->
  
<div class="flex h-full flex-col">
   
    <div class="md:flex md:items-center md:justify-between py-4 px-6">
        <div class="min-w-0 flex-1">
          <h2 class="text-2xl font-bold leading-7 text-gray-900 sm:truncate sm:text-3xl sm:tracking-tight">Change Logs</h2>
        </div>
        <div class="mt-4 flex md:mt-0 md:ml-4">
          <button type="button" class="ml-3 inline-flex items-center rounded-md border border-transparent bg-indigo-600 px-4 py-2 text-sm font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2">Add New</button>
        </div>
      </div>
        <!-- Bottom section -->
    <div class="flex min-h-0 flex-1 overflow-hidden">
    
      <!-- Main area -->
      <main class="min-w-0 flex-1 border-t border-gray-200 xl:flex">
        <section aria-labelledby="message-heading" class="flex h-full min-w-0 flex-1 flex-col overflow-hidden xl:order-last">
          <!-- Top section -->
       
  
          <div class="min-h-0 flex-1 overflow-y-auto">
            <div class="bg-white pt-5 pb-6 shadow">
              <div class="px-4 sm:flex sm:items-baseline sm:justify-between sm:px-6 lg:px-8">
                <div class="sm:w-0 sm:flex-1">
                  <h1 id="message-heading" class="text-lg font-medium text-gray-900">Added Feature number one
                </h1>
                  <p class="mt-1 truncate text-sm text-gray-500">Aashish Dhawan on October 12, 2022 </p>
                </div>
  
                <div class="mt-4 flex items-center justify-between sm:mt-0 sm:ml-6 sm:flex-shrink-0 sm:justify-start">
                  <span class="inline-flex items-center rounded-full bg-green-100 px-3 py-0.5 text-sm font-medium text-green-800">Published</span>
                  <div class="relative ml-3 inline-block text-left">
                    <div>
                      <button type="button" class="-my-2 flex items-center rounded-full bg-white p-2 text-gray-400 hover:text-gray-600 focus:outline-none focus:ring-2 focus:ring-blue-600" id="menu-3-button" aria-expanded="false" aria-haspopup="true">
                        <span class="sr-only">Open options</span>
                        <svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                          <path d="M10 3a1.5 1.5 0 110 3 1.5 1.5 0 010-3zM10 8.5a1.5 1.5 0 110 3 1.5 1.5 0 010-3zM11.5 15.5a1.5 1.5 0 10-3 0 1.5 1.5 0 003 0z" />
                        </svg>
                      </button>
                    </div>
  
                    <!--
                      Dropdown menu, show/hide based on menu state.
  
                      Entering: "transition ease-out duration-100"
                        From: "transform opacity-0 scale-95"
                        To: "transform opacity-100 scale-100"
                      Leaving: "transition ease-in duration-75"
                        From: "transform opacity-100 scale-100"
                        To: "transform opacity-0 scale-95"
                    -->
                    <div class="absolute right-0 z-10 mt-2 w-56 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none" role="menu" aria-orientation="vertical" aria-labelledby="menu-3-button" tabindex="-1">
                      <div class="py-1" role="none">
                        <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
                        <button type="button" class="text-gray-700 flex w-full justify-between px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-3-item-0">
                          <span>Edit</span>
                        </button>
                        <a href="#" class="text-gray-700 flex justify-between px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-3-item-1">
                          <span>Archive</span>
                        </a>
                        <a href="#" class="text-gray-700 flex justify-between px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-3-item-2">
                          <span>Delete</span>
                        </a>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <!-- Thread section-->
            <ul role="list" class="space-y-2 bg-gray-50 h-screen py-4 sm:space-y-4 sm:px-6 lg:px-8">
              <li class="bg-white px-4 py-6 shadow sm:rounded-lg sm:px-6">
                <div class=" space-y-6 text-sm text-gray-800"><p>This is a rich Text area where content will be published </p></div>
              </li>
  
             
            </ul>
          </div>
        </section>
  
        <!-- Message list-->
        <aside class="hidden xl:order-first xl:block xl:flex-shrink-0">
          <div class="relative flex h-full w-96 flex-col border-r border-gray-200 bg-gray-100">
            <div class="flex-shrink-0">            
              <div class="border-b border-gray-200 bg-gray-50 px-6 py-2 text-sm font-medium text-gray-500">List of changes</div>
            </div>
            <nav aria-label="Message list" class="min-h-0 flex-1 overflow-y-auto">
              <ul role="list" class="divide-y divide-gray-200 border-b border-gray-200">
                <li class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50">
                  <div class="flex justify-between space-x-3">
                    <div class="min-w-0 flex-1">
                      <a href="#" class="block focus:outline-none">
                        <span class="absolute inset-0" aria-hidden="true"></span>
                        <p class="truncate text-sm font-medium text-gray-900">Added feature Number one</p>
                        <p class="truncate text-sm text-gray-500">Added by Aashish on October 12, 2022</p>
                      </a>
                    </div>
                  </div>
                  <div class="mt-1">
                    <p class="text-sm text-gray-600 line-clamp-2">Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum natus facere. Enim rerum eaque qui facilis. Numquam laudantiu....</p>
                  </div>
                  <span class="inline-flex items-center rounded-full bg-green-100 px-2.5 py-0.5 text-xs font-medium text-green-800">Published</span>

                </li>
  
                <li class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50">
                  <div class="flex justify-between space-x-3">
                    <div class="min-w-0 flex-1">
                      <a href="#" class="block focus:outline-none">
                        <span class="absolute inset-0" aria-hidden="true"></span>
                        <p class="truncate text-sm font-medium text-gray-900">This is a Draft</p>
                        <p class="truncate text-sm text-gray-500">Nemo mollitia repudiandae adipisci explicabo optio consequatur tempora ut nihil</p>

                      </a>
                    </div>
                  </div>
                  <div class="mt-1">
                    <p class="text-sm text-gray-600 line-clamp-2">Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum natus facere. Enim rerum eaque qui facilis. Numquam laudantiu....</p>
                  </div>
                  <span class="inline-flex items-center rounded-full bg-yellow-100 px-2.5 py-0.5 text-xs font-medium text-yellow-800">Draft</span>
                </li>
  
                <li class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50">
                  <div class="flex justify-between space-x-3">
                    <div class="min-w-0 flex-1">
                      <a href="#" class="block focus:outline-none">
                        <span class="absolute inset-0" aria-hidden="true"></span>
                        <p class="truncate text-sm font-medium text-gray-900">Kyle Gulgowski</p>
                        <p class="truncate text-sm text-gray-500">Doloremque reprehenderit et harum quas explicabo nulla architecto dicta voluptatibus</p>
                      </a>
                    </div>
                  </div>
                  <div class="mt-1">
                    <p class="text-sm text-gray-600 line-clamp-2">Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum natus facere. Enim rerum eaque qui facilis. Numquam laudantiu....</p>
                  </div>
                </li>
  
                <li class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50">
                  <div class="flex justify-between space-x-3">
                    <div class="min-w-0 flex-1">
                      <a href="#" class="block focus:outline-none">
                        <span class="absolute inset-0" aria-hidden="true"></span>
                        <p class="truncate text-sm font-medium text-gray-900">Hattie Haag</p>
                        <p class="truncate text-sm text-gray-500">Eos sequi et aut ex impedit</p>
                      </a>
                    </div>
                  </div>
                  <div class="mt-1">
                    <p class="text-sm text-gray-600 line-clamp-2">Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum natus facere. Enim rerum eaque qui facilis. Numquam laudantiu....</p>
                  </div>
                </li>
  
                <li class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50">
                  <div class="flex justify-between space-x-3">
                    <div class="min-w-0 flex-1">
                      <a href="#" class="block focus:outline-none">
                        <span class="absolute inset-0" aria-hidden="true"></span>
                        <p class="truncate text-sm font-medium text-gray-900">Wilma Glover</p>
                        <p class="truncate text-sm text-gray-500">Quisquam veniam explicabo</p>
                      </a>
                    </div>
                  </div>
                  <div class="mt-1">
                    <p class="text-sm text-gray-600 line-clamp-2">Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum natus facere. Enim rerum eaque qui facilis. Numquam laudantiu....</p>
                  </div>
                </li>
  
                <li class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50">
                  <div class="flex justify-between space-x-3">
                    <div class="min-w-0 flex-1">
                      <a href="#" class="block focus:outline-none">
                        <span class="absolute inset-0" aria-hidden="true"></span>
                        <p class="truncate text-sm font-medium text-gray-900">Dolores Morissette</p>
                        <p class="truncate text-sm text-gray-500">Est ratione molestiae modi maiores consequatur eligendi et excepturi magni</p>
                      </a>
                    </div>
                  </div>
                  <div class="mt-1">
                    <p class="text-sm text-gray-600 line-clamp-2">Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum natus facere. Enim rerum eaque qui facilis. Numquam laudantiu....</p>
                  </div>
                </li>
  
                <li class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50">
                  <div class="flex justify-between space-x-3">
                    <div class="min-w-0 flex-1">
                      <a href="#" class="block focus:outline-none">
                        <span class="absolute inset-0" aria-hidden="true"></span>
                        <p class="truncate text-sm font-medium text-gray-900">Guadalupe Walsh</p>
                        <p class="truncate text-sm text-gray-500">Commodi deserunt aut veniam rem ipsam</p>
                      </a>
                    </div>
                  </div>
                  <div class="mt-1">
                    <p class="text-sm text-gray-600 line-clamp-2">Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum natus facere. Enim rerum eaque qui facilis. Numquam laudantiu....</p>
                  </div>
                </li>
  
                <li class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50">
                  <div class="flex justify-between space-x-3">
                    <div class="min-w-0 flex-1">
                      <a href="#" class="block focus:outline-none">
                        <span class="absolute inset-0" aria-hidden="true"></span>
                        <p class="truncate text-sm font-medium text-gray-900">Jasmine Hansen</p>
                        <p class="truncate text-sm text-gray-500">Illo illum aut debitis earum</p>
                      </a>
                    </div>
                  </div>
                  <div class="mt-1">
                    <p class="text-sm text-gray-600 line-clamp-2">Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum natus facere. Enim rerum eaque qui facilis. Numquam laudantiu....</p>
                  </div>
                </li>
  
                <li class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50">
                  <div class="flex justify-between space-x-3">
                    <div class="min-w-0 flex-1">
                      <a href="#" class="block focus:outline-none">
                        <span class="absolute inset-0" aria-hidden="true"></span>
                        <p class="truncate text-sm font-medium text-gray-900">Ian Volkman</p>
                        <p class="truncate text-sm text-gray-500">Qui dolore iste ut est cumque sed</p>
                      </a>
                    </div>
                  </div>
                  <div class="mt-1">
                    <p class="text-sm text-gray-600 line-clamp-2">Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum natus facere. Enim rerum eaque qui facilis. Numquam laudantiu....</p>
                  </div>
                </li>
  
                <li class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50">
                  <div class="flex justify-between space-x-3">
                    <div class="min-w-0 flex-1">
                      <a href="#" class="block focus:outline-none">
                        <span class="absolute inset-0" aria-hidden="true"></span>
                        <p class="truncate text-sm font-medium text-gray-900">Rafael Klocko</p>
                        <p class="truncate text-sm text-gray-500">Aut sed aut illum delectus maiores laboriosam ex</p>
                      </a>
                    </div>
                  </div>
                  <div class="mt-1">
                    <p class="text-sm text-gray-600 line-clamp-2">Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum natus facere. Enim rerum eaque qui facilis. Numquam laudantiu....</p>
                  </div>
                </li>
              </ul>
            </nav>
          </div>
        </aside>
      </main>
    </div>
  </div>
  