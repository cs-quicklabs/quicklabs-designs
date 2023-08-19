<script>
    import Fullnavbar from '$lib/bugplot/fullnavbar.svelte';
    import ProjectHeader from '../../../header.svelte';
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
        <a class="flex items-center hover:text-blue-600" href="/bugplot/projects/1/milestones">
          GraphQL APIs
          <svg class="flex-shrink-0 h-5 w-5 text-gray-400 dark:text-gray-600 mx-2" width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <path d="M6 13L10 3" stroke="currentColor" stroke-linecap="round"/>
          </svg>
        </a>
      </li>
    
      <li class="text-sm font-semibold text-gray-800 truncate dark:text-gray-200" aria-current="page">
        Milestones
      </li>
    </ol>
      <div class="sm:flex sm:items-baseline sm:justify-between">
          <div class="sm:w-0 sm:flex-1">
              <h1 class="flex-1 text-2xl font-bold text-gray-900">Milestone: Milestone 1</h1>
              <p class="mt-1 truncate text-sm text-gray-500">This is Milestone description which should not go beyond one line</p>
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
  <div class="-my-2 overflow-x-auto ">
    <div class="inline-block min-w-full py-3 align-middle sm:px-6 lg:px-8">    
  
      <div class="overflow-hidden ">
        <table class="min-w-full divide-y divide-gray-300">
          <tbody class="divide-y divide-gray-200 bg-white ml-4">
              <tr>
                  <td class="whitespace-nowrap py-3 pl-4 pr-3 text-sm font-medium text-gray-900 sm:pl-0 w-full hover:underline cursor-pointer">
                    <a href="/bugplot/projects/1/milestones/1"><span>Smoke Testing</span>
                      <div class="mt-1 flex items-center gap-x-2 text-xs leading-5 text-gray-500 font-normal">
                              <p class="whitespace-nowrap">Due on Jan 12, 2023</p>
                              <svg viewBox="0 0 2 2" class="h-0.5 w-0.5 fill-current">
                                <circle cx="1" cy="1" r="1" />
                              </svg>
                              <p class="whitespace-nowrap">100 test cases</p>

                            </div>
                          </a> 
      </td>
                  <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">
                      <span class="inline-flex items-center rounded-md bg-yellow-50 px-2 py-1 text-xs font-medium text-yellow-700 ring-1 ring-inset ring-yellow-600/20"> In Progress</span>
                    </td>
                          <td class="relative whitespace-nowrap py-3 pl-3 pr-4 text-right text-sm font-medium sm:pr-0">
                  </td>
                </tr>
              {#each Array(5) as _, index (index)}
              <tr>
                  <td class="whitespace-nowrap py-3 pl-4 pr-3 text-sm font-medium text-gray-900 sm:pl-0 w-full hover:underline cursor-pointer">
                    <a href="/bugplot/projects/1/milestones/1">Regression Testing {index + 2}
                    <div class="mt-1 flex items-center gap-x-2 text-xs leading-5 text-gray-500 font-normal">
                      <p class="whitespace-nowrap">Completed on Jan 12, 2023 by Aashish Dhawan</p>
                      <svg viewBox="0 0 2 2" class="h-0.5 w-0.5 fill-current">
                        <circle cx="1" cy="1" r="1" />
                      </svg>
                      <p class="whitespace-nowrap">80 Passed, 20 Failed, 9 Blocked</p>
                                        </div>
                                      </a> 
              </td>
                  <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">
                      <span class="inline-flex items-center rounded-md bg-green-50 px-2 py-1 text-xs font-medium text-green-700 ring-1 ring-inset ring-green-600/20">Completed</span>
                    </td>
                          <td class="relative whitespace-nowrap py-3 pl-3 pr-4 text-right text-sm font-medium sm:pr-0">
                  </td>
                </tr>
              {/each}

            <!-- More people... -->
          </tbody>
        </table>
      </div>
    </div>
  </div>
</div>
    </div>
  </div>

  <div class="shrink-0 border-t border-gray-200 px-4 py-6 sm:px-6 lg:w-96 lg:border-l lg:border-t-0 lg:pr-8 xl:pr-6 h-screen">
    <!-- Right column area -->
      
        <h3 class="text-base font-semibold leading-6 text-gray-900">Milestone 1's Test Runs</h3>
        <div class="mt-2 max-w-xl text-sm text-gray-500">
          <p>A project milestone can consist of multiple test runs. There are 2 active test runs in this milestones. For example, a product release might require testing of mobile, web and other modules separately.</p>
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
          <button type="button" class="inline-flex items-center rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-500">Add Another Test Run</button>
        </div>
  </div>
</div>