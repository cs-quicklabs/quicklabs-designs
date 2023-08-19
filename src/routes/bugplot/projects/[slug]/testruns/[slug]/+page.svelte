<script>
    import Fullnavbar from '$lib/bugplot/fullnavbar.svelte';
    let menu = { opened: false };

function toggle() {
  menu.opened = !menu.opened;
}

</script>
<Fullnavbar/>

<div class="bg-gray-50/50">
  
  <div class="mx-auto px-4 pt-4 border-b pb-4 sm:px-6 lg:px-8">
    <ol class="flex items-center whitespace-nowrap min-w-0 pb-2" aria-label="Breadcrumb">
      <li class="text-sm text-gray-600 dark:text-gray-400">
        <a class="flex items-center hover:text-blue-600" href="/bugplot/projects">
          Projects
          <svg class="flex-shrink-0 h-5 w-5 text-gray-400 dark:text-gray-600 mx-2" width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <path d="M6 13L10 3" stroke="currentColor" stroke-linecap="round"/>
          </svg>
        </a>
      </li>
    
      <li class="text-sm text-gray-600 dark:text-gray-400">
        <a class="flex items-center hover:text-blue-600" href="/bugplot/projects/1/testruns">
          GraphQL APIs
          <svg class="flex-shrink-0 h-5 w-5 text-gray-400 dark:text-gray-600 mx-2" width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <path d="M6 13L10 3" stroke="currentColor" stroke-linecap="round"/>
          </svg>
        </a>
      </li>
    
      <li class="text-sm font-semibold text-gray-800 truncate dark:text-gray-200" aria-current="page">
        Test Runs
      </li>
    </ol>
      <div class="sm:flex sm:items-baseline sm:justify-between">
          <div class="sm:w-0 sm:flex-1">
              <h1 class="flex-1 text-2xl font-bold text-gray-900">Test Run: Smoke Testing 1</h1>
              <p class="mt-1 truncate text-sm text-gray-500">This is test run description which should not go beyond one line</p>
          </div>
          <div class="mt-4 flex items-center justify-between sm:ml-6 sm:mt-0 sm:flex-shrink-0 sm:justify-start">
              <span class="inline-flex items-center rounded-md bg-green-50 px-2 py-1 text-xs font-medium text-green-700 ring-1 ring-inset ring-green-600/20">Completed</span>

              <div class="relative ml-3 inline-block text-left">
                  <div>
                      <button
                      on:click={toggle}
                          type="button"
                          class="-my-2 flex items-center rounded-full bg-white p-2 text-gray-400 hover:text-gray-600 focus:outline-none focus:ring-2 focus:ring-indigo-500"
                          id="menu-0-button"
                          aria-expanded="false"
                          aria-haspopup="true"
                      >
                          <span class="sr-only">Open options</span>
                          <svg
                              class="h-5 w-5"
                              viewBox="0 0 20 20"
                              fill="currentColor"
                              aria-hidden="true"
                          >
                              <path d="M10 3a1.5 1.5 0 110 3 1.5 1.5 0 010-3zM10 8.5a1.5 1.5 0 110 3 1.5 1.5 0 010-3zM11.5 15.5a1.5 1.5 0 10-3 0 1.5 1.5 0 003 0z"/>
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
                  {#if menu.opened}
                  <div
                      class="absolute right-0 z-10 mt-2 w-56 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
                      role="menu"
                      aria-orientation="vertical"
                      aria-labelledby="menu-0-button"
                      tabindex="-1"
                  >
                      <div class="py-1" role="none">
                          <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
                          <a
                              href="#"
                              class="text-gray-700 flex justify-between px-4 py-2 text-sm hover:bg-gray-50"
                              role="menuitem"
                              tabindex="-1"
                              id="menu-0-item-0"
                          >
                              <span>Edit</span>
                          </a>
                          <button
                              type="button"
                              class="text-gray-700 flex w-full justify-between px-4 py-2 text-sm hover:bg-gray-50"
                              role="menuitem"
                              tabindex="-1"
                              id="menu-0-item-2"
                          >
                              <span>Delete</span>
                          </button>
                          <button
                              type="button"
                              class="text-gray-700 flex w-full justify-between px-4 py-2 text-sm hover:bg-gray-50"
                              role="menuitem"
                              tabindex="-1"
                              id="menu-0-item-2"
                          >
                              <span>Mark As Complete</span>
                          </button>
                      </div>
                  </div>
                  {/if}
              </div>
          </div>
      </div>
  </div>
  
</div>
<!-- 3 column wrapper -->
<div class="mx-auto w-full grow lg:flex">
  <!-- Left sidebar & main wrapper -->
  <div class="flex-1 xl:flex">
    <div class="xl:flex-1">
      <!-- Main area -->
      <div class="flow-root">
  <div class="overflow-x-auto ">
    <div class="inline-block min-w-full align-middle">    
  
<div class="overflow-hidden min-h-300"><table class="min-w-full divide-y divide-gray-200 mb-6"><thead class="bg-gray-50 border-b"><tr><th scope="col" class="px-6 py-2 text-left text-sm font-normal text-gray-900 uppercase w-1/12">Sr.No.</th><th scope="col" class="px-6 py-2 text-left text-sm font-normal text-gray-900 uppercase w-8/12">Title</th><th scope="col" class="px-6 py-2 text-right text-sm font-normal text-gray-900 uppercase w-8/12">Action</th><th scope="col" class="px-6 py-2 text-right text-sm font-normal text-gray-900 uppercase"></th></tr></thead><tbody class="bg-white divide-y divide-gray-200"><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>1</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify if a user will be able to login with a valid username and valid password. </span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-0" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-290" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>2</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify if a user cannot login with a valid username and an invalid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-1" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-291" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>3</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify the login page for both, when the field is blank and Submit button is clicked.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-2" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-292" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>4</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify if a user cannot login with invalid username and an invalid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-3" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-293" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>5</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify if a user will be able to login with a valid username and valid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-4" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-294" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>6</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify if a user is not able to login with a valid username and an invalid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-5" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-295" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>7</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify login functionality keeping both the field as blank</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-6" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-296" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>8</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify if a useris not able to login with invalid username and an invalid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-7" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-297" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>9</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify user is  able to login with a valid username and valid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-8" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-298" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>10</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify if a user is not able to login with a valid username and invalid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-9" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-299" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>11</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify login functionality keeping both the fields as blank</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-10" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-300" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>12</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify if a user is not able to login with invalid username and an invalid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-11" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-301" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>13</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify user will be able to login with a valid username and valid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-12" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-302" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>14</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify if user is not able to login with a valid username and an invalid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-13" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-303" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>15</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify login functionality keeping both email and password  field as blank</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-14" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-304" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>16</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Verify if  user is not able to login with invalid username and an invalid password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-15" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-305" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>17</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Check the forget password link is available in the login screen or not.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-16" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-306" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>18</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Check on click of forget password link user should be redirected to the forget password page.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-17" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-307" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>19</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Check is the email field is present on the forget password page to recover the password.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-18" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-308" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr><tr class="rounded"><td class="px-6 py-2 whitespace-nowrap text-sm font-normal text-gray-900"><span class="truncate hover:underline cursor-pointer"><span>20</span></span></td><td class="px-6 py-2 font-normal text-sm text-gray-900"><span class="truncate break-normal whitespace-normal hover:underline cursor-pointer">Check the forgot password functionality when user enter the valid email id and click on send button.</span></td><td class="px-6 py-2 whitespace-nowrap text-right text-xs font-normal"><span class="capitalize inline-flex items-center px-2 py-0.5 rounded font-medium bg-green-100 text-green-800">passed</span></td><td class="pr-6"><div data-cy="three-dots-menu-19" class="relative flex justify-end items-center"><button class="w-8 h-8 bg-white inline-flex items-center justify-center text-gray-400 rounded-full hover:text-gray-500 focus:outline-none false" id="headlessui-menu-button-309" type="button" aria-haspopup="true" aria-expanded="false"><span class="sr-only">Open options</span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5" aria-hidden="true"><path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path></svg></button></div></td></tr></tbody></table></div>    </div>
  </div>
</div>
    </div>
  </div>

  <div class="shrink-0 border-t border-gray-200 px-4 py-6 sm:px-6 lg:w-96 lg:border-l lg:border-t-0 lg:pr-8 xl:pr-6 h-screen">
    <!-- Right column area -->
      
        <h3 class="text-base font-semibold leading-6 text-gray-900">Test Run</h3>
        <div class="mt-2 max-w-xl text-sm text-gray-500">
          <p>A test run is a collection of test cases which are tested to create a report about passing and failing tests.</p>
        </div>
        <div class="flex justify-between">
        <div class="mt-4 text-sm">
          <label for="small" class="font-medium text-gray-900">Start Date</label>
          <p id="small-description" class="text-gray-500">Jan 13, 2023</p>
        </div>

        <div class="mt-4 text-sm">
          <label for="small" class="font-medium text-gray-900">End Date</label>
          <p id="small-description" class="text-gray-500">Jan 13, 2024</p>
        </div>
      </div>
      <div class="flex justify-between">
        <div class="mt-4 text-sm">
          <label for="small" class="font-medium text-gray-900">Created By</label>
          <p id="small-description" class="text-gray-500">Aashish Dhawan</p>
        </div>

        <div class="mt-4 text-sm">
          <label for="small" class="font-medium text-gray-900">Created on</label>
          <p id="small-description" class="text-gray-500">Jan 13, 2024</p>
        </div>
      </div>
        <div class="mt-5">
          <button type="button" class="inline-flex items-center rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-500">Mark as Complete</button>
          <button type="button" class="rounded-md bg-white px-3 py-2 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50 ml-2">Generate Report</button>

        </div>
  </div>
</div>