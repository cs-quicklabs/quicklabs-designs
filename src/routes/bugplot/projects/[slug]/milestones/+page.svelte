<script>
    import Fullnavbar from '$lib/bugplot/fullnavbar.svelte';
    import ProjectHeader from '../../header.svelte';
</script>
<Fullnavbar/>
<ProjectHeader selection="Milestones"/>
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
                    <td class="whitespace-nowrap py-3 pl-4 pr-3 text-sm font-medium text-gray-900 sm:pl-0 w-full">Milestone 0 </td>
                    <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">1 active Test runs</td>
                    <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">Due on 12 Jan, 2024</td>
                    <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">
                        <span class="inline-flex items-center rounded-md bg-yellow-50 px-2 py-1 text-xs font-medium text-yellow-700 ring-1 ring-inset ring-yellow-600/20"> In Progress</span>
                      </td>
                            <td class="relative whitespace-nowrap py-3 pl-3 pr-4 text-right text-sm font-medium sm:pr-0">
                      <a href="#" class="text-indigo-600 hover:text-indigo-900">Edit<span class="sr-only">, Lindsay Walton</span></a>
                    </td>
                  </tr>
                {#each Array(5) as _, index (index)}
                <tr>
                    <td class="whitespace-nowrap py-3 pl-4 pr-3 text-sm font-medium text-gray-900 sm:pl-0 w-full">Milestone 1 </td>
                    <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">No Active test runs</td>
                    <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">Completed on 12 Jan, 2024</td>
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
        
          <h3 class="text-base font-semibold leading-6 text-gray-900">Manage Milestones</h3>
          <div class="mt-2 max-w-xl text-sm text-gray-500">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae voluptatibus corrupti atque repudiandae nam.</p>
          </div>
          <div class="mt-5">
            <button type="button" class="inline-flex items-center rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-500">Add Milestone</button>
          </div>
    </div>
  </div>