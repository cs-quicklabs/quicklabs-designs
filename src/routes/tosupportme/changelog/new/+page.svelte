<script>
	import Fullnavbar from '$lib/tosupportme/fullnavbar.svelte';
  let menu = { opened: false, filter: false};

	function toggle() {
		menu.opened = !menu.opened;    
	}

  function filter() {
		menu.filter = !menu.filter;    
	}
</script>
<Fullnavbar />
  
  
  <main class="mx-auto max-w-2xl  px-4 pt-10 pb-12 lg:pb-16">
    <form>
      <div class="space-y-6">
        <div>
          <h1 class="text-lg font-medium leading-6 text-gray-900">Add New Change Log</h1>
          <p class="mt-1 text-sm text-gray-500">Let’s get started by filling in the information below to create your new changelog.</p>
        </div>
  
        <div>
          <label for="project-name" class="block text-sm font-medium leading-6 text-gray-900">Title</label>
          <div class="mt-2">
            <input type="text" name="project-name" id="project-name" class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-sky-500 sm:text-sm sm:leading-6" value="">
          </div>
        </div>
  
        <div>
          <label for="description" class="block text-sm font-medium leading-6 text-gray-900">Description</label>
          <div class="mt-2">
            <textarea id="description" name="description" rows="3" class="block w-full h-56 rounded-md border-0 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-sky-500 sm:py-1.5 sm:text-sm sm:leading-6"></textarea>
          </div>
        </div>

        <div>
            <label for="project-name" class="block text-sm font-medium leading-6 text-gray-900">Release Version (Optional)</label>
            <div class="mt-2">
              <input type="text" name="project-name" id="project-name" class="px-2 block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-sky-500 sm:text-sm sm:leading-6" value="" placeholder="1.0.0">
            </div>
          </div>
  
          <fieldset>
            <label for="project-name" class="block text-sm font-medium leading-6 text-gray-900">Release Categories (Optional)</label>

          <div class="space-y-1 flex items-center space-x-4" >
            <div class="relative flex items-start">
              <div class="flex h-6 items-center">
                <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-green-300 text-green-600 focus:ring-green-600">
              </div>
              <div class="ml-1 text-sm leading-6">
                <span class="inline-flex items-center rounded bg-green-100 px-2 py-0.5 text-xs font-medium text-green-800">                   
                    New
                  </span>            
              </div>
            </div>
         

            <div class="relative flex items-start">
                <div class="flex h-6 items-center">
                  <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-gray-600 focus:ring-gray-600">
                </div>
                <div class="ml-1 text-sm leading-6">
                  <span class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800">                   
                      Improvements
                    </span>            
                </div>
              </div>



              <div class="relative flex items-start">
                <div class="flex h-6 items-center">
                  <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-red-300 text-red-600 focus:ring-red-600">
                </div>
                <div class="ml-1 text-sm leading-6">
                  <span class="inline-flex items-center rounded bg-red-100 px-2 py-0.5 text-xs font-medium text-red-800">                   
                      Bug Fixes
                    </span>            
                </div>
              </div>


              <div class="relative flex items-start">
                <div class="flex h-6 items-center">
                  <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-600">
                </div>
                <div class="ml-1 text-sm leading-6">
                  <span class="inline-flex items-center rounded bg-indigo-100 px-2 py-0.5 text-xs font-medium text-indigo-800">                   
                      Maintainence
                    </span>            
                </div>
              </div>


              <div class="relative flex items-start">
                <div class="flex h-6 items-center">
                  <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-yellow-300 text-yellow-600 focus:ring-yellow-600">
                </div>
                <div class="ml-1 text-sm leading-6">
                  <span class="inline-flex items-center rounded bg-yellow-100 px-2 py-0.5 text-xs font-medium text-yellow-800">                   
                      Refactor
                    </span>            
                </div>
              </div>
        
          </div>
        </fieldset>
        <div>
          <label for="tags" class="block text-sm font-medium leading-6 text-gray-900">Release Tags (Optional)</label>
          <input type="text" name="tags" id="tags" class="mt-2 block w-full rounded-md border-0 py-1.5 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-sky-500 sm:text-sm sm:leading-6">
        
        </div>
  
        <div>
            <label for="tags" class="block text-sm font-medium leading-6 text-gray-900">Schedule Date and time</label>
            <input type="text" name="tags" id="tags" class="mt-2 block w-full rounded-md border-0 py-1.5 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-sky-500 sm:text-sm sm:leading-6">
          
          </div>
        <div class="flex justify-end gap-x-3">
            <a href="/changelog">
          <button type="button" class="rounded-md bg-white py-2 px-3 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50">Cancel</button>
        </a>
        <div>
            <label id="listbox-label" class="sr-only">Change published status</label>
            <div class="relative">
              <div class="inline-flex divide-x divide-indigo-700 rounded-md shadow-sm">
                <div class="inline-flex items-center gap-x-1.5 rounded-l-md bg-indigo-600 py-2 px-3 text-white shadow-sm">
                  <svg class="-ml-0.5 h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                    <path fill-rule="evenodd" d="M16.704 4.153a.75.75 0 01.143 1.052l-8 10.5a.75.75 0 01-1.127.075l-4.5-4.5a.75.75 0 011.06-1.06l3.894 3.893 7.48-9.817a.75.75 0 011.05-.143z" clip-rule="evenodd" />
                  </svg>
                  <p class="text-sm font-semibold">Publish Changelog</p>
                </div>
                <button type="button" class="inline-flex items-center rounded-l-none rounded-r-md bg-indigo-600 p-2 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-600 focus:ring-offset-2 focus:ring-offset-gray-50" aria-haspopup="listbox" aria-expanded="true" aria-labelledby="listbox-label">
                  <span class="sr-only">Change published status</span>
                  <svg class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                    <path fill-rule="evenodd" d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z" clip-rule="evenodd" />
                  </svg>
                </button>
              </div>
          
              <!--
                Select popover, show/hide based on select state.
          
                Entering: ""
                  From: ""
                  To: ""
                Leaving: "transition ease-in duration-100"
                  From: "opacity-100"
                  To: "opacity-0"
              -->
              <ul class="absolute right-0 z-10 mt-2 w-72 origin-top-right divide-y divide-gray-200 overflow-hidden rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none" tabindex="-1" role="listbox" aria-labelledby="listbox-label" aria-activedescendant="listbox-option-0">
                <!--
                  Select option, manage highlight styles based on mouseenter/mouseleave and keyboard navigation.
          
                  Highlighted: "bg-indigo-600 text-white", Not Highlighted: "text-gray-900"
                -->
                <li class="text-gray-900 cursor-default select-none p-4 text-sm" id="listbox-option-0" role="option">
                  <div class="flex flex-col">
                    <div class="flex justify-between">
                      <!-- Selected: "font-semibold", Not Selected: "font-normal" -->
                      <p class="font-normal">Publish Now</p>
                      <!--
                        Checkmark, only display for selected option.
          
                        Highlighted: "text-white", Not Highlighted: "text-indigo-600"
                      -->
                      <span class="text-indigo-600">
                        <svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                          <path fill-rule="evenodd" d="M16.704 4.153a.75.75 0 01.143 1.052l-8 10.5a.75.75 0 01-1.127.075l-4.5-4.5a.75.75 0 011.06-1.06l3.894 3.893 7.48-9.817a.75.75 0 011.05-.143z" clip-rule="evenodd" />
                        </svg>
                      </span>
                    </div>
                    <!-- Highlighted: "text-indigo-200", Not Highlighted: "text-gray-500" -->
                    <p class="text-gray-500 mt-2">Publish your change log now</p>
                  </div>
                </li>
          
                <!-- More items... -->

                <li class="text-gray-900 cursor-default select-none p-4 text-sm" id="listbox-option-0" role="option">
                    <div class="flex flex-col">
                      <div class="flex justify-between">
                        <!-- Selected: "font-semibold", Not Selected: "font-normal" -->
                        <p class="font-normal">Save as Draft</p>
                        <!--
                          Checkmark, only display for selected option.
            
                          Highlighted: "text-white", Not Highlighted: "text-indigo-600"
                        -->
                        
                      </div>
                      <!-- Highlighted: "text-indigo-200", Not Highlighted: "text-gray-500" -->
                      <p class="text-gray-500 mt-2">Save as draft and edit in future</p>
                    </div>
                  </li>

                    <!-- More items... -->

                <li class="text-gray-900 cursor-default select-none p-4 text-sm" id="listbox-option-0" role="option">
                    <div class="flex flex-col">
                      <div class="flex justify-between">
                        <!-- Selected: "font-semibold", Not Selected: "font-normal" -->
                        <p class="font-normal">Schedule</p>
                        <!--
                          Checkmark, only display for selected option.
            
                          Highlighted: "text-white", Not Highlighted: "text-indigo-600"
                        -->
                       
                      </div>
                      <!-- Highlighted: "text-indigo-200", Not Highlighted: "text-gray-500" -->
                      <p class="text-gray-500 mt-2">Schedule your release to publish automatically on specified date</p>
                    </div>
                  </li>

              </ul>
            </div>
          </div>
          

        </div>
      </div>
    </form>
  </main>
  