<script>
	import UserNavBar from '$lib/tosupportme/usernavbar.svelte';
  let menu = { opened: false, filter: false};

	function toggle() {
		menu.opened = !menu.opened;    
	}

  function filter() {
		menu.filter = !menu.filter;    
	}
</script>

<UserNavBar />
<main class="mx-auto max-w-7xl pb-10 lg:py-12 lg:px-8">
    <div class="lg:grid lg:grid-cols-12 lg:gap-x-5">
      <aside class="py-6 px-2 sm:px-6 lg:col-span-3 lg:py-0 lg:px-0">
        <!--
  This example requires some changes to your config:
  
  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/forms'),
    ],
  }
  ```
-->
<div>
    <label class="text-base font-semibold text-gray-900 ">Select Categories</label>
    <p class="text-sm text-gray-500">Chose Release Categories</p>
    <fieldset class="mt-4">
      <legend class="sr-only">Notification method</legend>
      <div class="space-y-2">
        <div class="flex items-center">
            <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-600">
            <label for="email" class="ml-3 block text-sm font-medium leading-6 text-gray-900">New</label>
        </div>
  
        <div class="flex items-center">
            <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-600">
            <label for="sms" class="ml-3 block text-sm font-medium leading-6 text-gray-900">Improvements</label>
        </div>
  
        <div class="flex items-center">
            <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-600">
            <label for="push" class="ml-3 block text-sm font-medium leading-6 text-gray-900">Maintainence</label>
        </div>
        <div class="flex items-center">
            <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-600">
            <label for="push" class="ml-3 block text-sm font-medium leading-6 text-gray-900">Bug Fixes</label>
          </div>
          <div class="flex items-center">
            <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-600">
            <label for="push" class="ml-3 block text-sm font-medium leading-6 text-gray-900">Refactor</label>
          </div>
      </div>
    </fieldset>
  </div>
  
  <div class = "mt-12">
    <label class="text-base font-semibold text-gray-900 ">Select Release tags</label>
    <p class="text-sm text-gray-500">Chose Release tags</p>
    <fieldset class="mt-4">
      <legend class="sr-only">Notification method</legend>
      <div class="space-y-2">
        <div class="flex items-center">
            <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-600">
            <label for="email" class="ml-3 block text-sm font-medium leading-6 text-gray-900">iOS</label>
        </div>
  
        <div class="flex items-center">
            <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-600">
            <label for="sms" class="ml-3 block text-sm font-medium leading-6 text-gray-900">Android</label>
        </div>
  
        <div class="flex items-center">
            <input id="comments" aria-describedby="comments-description" name="comments" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-600">
            <label for="push" class="ml-3 block text-sm font-medium leading-6 text-gray-900">Web</label>
        </div>
      
      </div>
    </fieldset>
  </div>


</aside>
      <div class="space-y-6 sm:px-6 lg:col-span-9 lg:px-0">
        <main class= "max-w-2xl  border-b border-gray-100 ">
          
              
        <div class="md:flex md:items-center md:justify-between">
            
            <div class="min-w-0 flex-1">
              <h2 class="text-2xl font-bold leading-7 text-gray-900 sm:truncate sm:text-3xl sm:tracking-tight">Added Feature One</h2>
              <p class="mt-1 truncate text-sm text-gray-500">Published on October 12, 2022 as Version 3.0.2</p>
              <div class="mt-1">
                <span class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800">Improvements</span>
                <span class="inline-flex items-center rounded bg-red-100 px-2 py-0.5 text-xs font-medium text-red-800">Bug Fixes</span>
                <span class="inline-flex items-center rounded bg-green-100 px-2 py-0.5 text-xs font-medium text-green-800">New</span>
                <span class="inline-flex items-center rounded bg-yellow-100 px-2 py-0.5 text-xs font-medium text-yellow-800">Refactor</span>
                <span class="inline-flex items-center rounded bg-blue-100 px-2 py-0.5 text-xs font-medium text-blue-800">Maintainence</span>
            
              </div>
            </div>
        
          </div>
        
          <div class=" space-y-6 text-sm text-gray-800 py-12">
            <p>This is rich text description of release notes</p>
        
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita, hic? Commodi cumque similique id tempora molestiae deserunt at suscipit, dolor voluptatem, numquam, harum consequatur laboriosam voluptas tempore aut voluptatum alias?</p>
            <ul>
              <li>Tempor ultrices proin nunc fames nunc ut auctor vitae sed. Eget massa parturient vulputate fermentum id facilisis nam pharetra. Aliquet leo tellus.</li>
              <li>Turpis ac nunc adipiscing adipiscing metus tincidunt senectus tellus.</li>
              <li>Semper interdum porta sit tincidunt. Dui suspendisse scelerisque amet metus eget sed. Ut tellus in sed dignissim.</li>
            </ul>
            <div class=" text-sm text-gray-800">
                <span class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800">iOS</span>
                <span class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800">Android</span>
                <span class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800">Web</span>
              </div>
            
        </div>
        
        
        </main>
        
        <main class= "max-w-2xl  ">
          
              
            <div class="md:flex md:items-center md:justify-between">
                
                <div class="min-w-0 flex-1">
                  <h2 class="text-2xl font-bold leading-7 text-gray-900 sm:truncate sm:text-3xl sm:tracking-tight mt-4">Added Feature One</h2>
                  <p class="mt-1 truncate text-sm text-gray-500">Published on October 12, 2022 as Version 3.0.2</p>
                  <div class="mt-1">
                    <span class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800">Improvements</span>
                    <span class="inline-flex items-center rounded bg-red-100 px-2 py-0.5 text-xs font-medium text-red-800">Bug Fixes</span>
                    <span class="inline-flex items-center rounded bg-green-100 px-2 py-0.5 text-xs font-medium text-green-800">New</span>
                    <span class="inline-flex items-center rounded bg-yellow-100 px-2 py-0.5 text-xs font-medium text-yellow-800">Refactor</span>
                    <span class="inline-flex items-center rounded bg-blue-100 px-2 py-0.5 text-xs font-medium text-blue-800">Maintainence</span>
                
                  </div>
                </div>
            
              </div>
            
              <div class=" space-y-6 text-sm text-gray-800 py-12">
                <p>This is rich text description of release notes</p>
            
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita, hic? Commodi cumque similique id tempora molestiae deserunt at suscipit, dolor voluptatem, numquam, harum consequatur laboriosam voluptas tempore aut voluptatum alias?</p>
                <ul>
                  <li>Tempor ultrices proin nunc fames nunc ut auctor vitae sed. Eget massa parturient vulputate fermentum id facilisis nam pharetra. Aliquet leo tellus.</li>
                  <li>Turpis ac nunc adipiscing adipiscing metus tincidunt senectus tellus.</li>
                  <li>Semper interdum porta sit tincidunt. Dui suspendisse scelerisque amet metus eget sed. Ut tellus in sed dignissim.</li>
                </ul>
                <div class=" text-sm text-gray-800">
                    <span class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800">iOS</span>
                    <span class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800">Android</span>
                    <span class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800">Web</span>
                  </div>
                
            </div>
            
            
            </main>
    
</div>
      
      </div>    

      
      </main>

