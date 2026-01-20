<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';

	let selectedType = 'all';

	const designs = [
		{
			id: 1,
			name: 'Course Completion Certificate',
			type: 'certificate',
			date: '12 Dec 2024',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 2,
			name: 'Top Performer Badge',
			type: 'badge',
			date: '08 Dec 2024',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 3,
			name: 'Course Completion Certificate',
			type: 'certificate',
			date: '12 Dec 2024',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 4,
			name: 'Top Performer Badge',
			type: 'badge',
			date: '08 Dec 2024',
			image: '/quick-certify/rashi.png'
		}
	];

	$: filteredDesigns =
		selectedType === 'all' ? designs : designs.filter((d) => d.type === selectedType);
</script>

<NavBar />

<section class="bg-gray-50 dark:bg-gray-900 py-3 sm:py-5 min-h-screen">
	<div class="px-4 mx-auto max-w-screen-2xl lg:px-8">
		<div class="relative overflow-hidden bg-white shadow-md dark:bg-gray-800 sm:rounded-sm">
			<div class=" divide-y dark:divide-gray-700">
				<div
					class="flex-row items-center justify-between p-4 space-y-3 sm:flex sm:space-y-0 sm:space-x-4">
					<div>
						<h1 class="mr-3 text-lg font-semibold dark:text-white">Designs Library</h1>
						<p class="text-gray-500 dark:text-gray-400 text-sm">Manage certificate and badge designs</p>
					</div>
					<!-- <div class="flex space-x-4">

						<div class="flex space-x-2 items-center w-full">
							<a
								type="button"
								href="/quick-certify/designs/add-design"
								class="btn-primary w-full">
								Add New Certificate
							</a>
						</div>
                        
					</div> -->

					<button
						id="dropdownDefaultButton"
						data-dropdown-toggle="dropdownId"
						class="btn-primary flex"
						type="button">
						Add New Design
						<svg
							class="w-4 h-4 ms-1.5 -me-0.5"
							aria-hidden="true"
							xmlns="http://www.w3.org/2000/svg"
							width="24"
							height="24"
							fill="none"
							viewBox="0 0 24 24"
							><path
								stroke="currentColor"
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="m19 9-7 7-7-7" /></svg>
					</button>

					<!-- Dropdown menu -->
					<div
						id="dropdownId"
						class="z-50 hidden w-44 rounded-md border border-gray-200
         bg-white shadow-lg">
						<ul class="p-2 text-sm font-medium text-gray-700">
							<li>
								<a
									href="/quick-certify/designs/add-design"
									class="inline-flex w-full gap-3 items-center rounded-md p-2
               hover:bg-gray-100 hover:text-gray-900">
			   						<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"  class="w-5 h-5">
  <path stroke-linecap="round" stroke-linejoin="round" d="M6.429 9.75 2.25 12l4.179 2.25m0-4.5 5.571 3 5.571-3m-11.142 0L2.25 7.5 12 2.25l9.75 5.25-4.179 2.25m0 0L21.75 12l-4.179 2.25m0 0 4.179 2.25L12 21.75 2.25 16.5l4.179-2.25m11.142 0-5.571 3-5.571-3" />
</svg>

									Certificate
			
								</a>
							</li>
							<li>
			
								<a
								
									href="/quick-certify/designs/add-design"
									class="inline-flex w-full gap-3 items-center rounded-md p-2
               hover:bg-gray-100 hover:text-gray-900">
			    <svg
    xmlns="http://www.w3.org/2000/svg"
    fill="none"
    viewBox="0 0 24 24"
    stroke-width="1.5"
    stroke="currentColor"
    class="w-5 h-5"
  >
    <path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M9 12.75 11.25 15 15 9.75M21 12c0 1.268-.63 2.39-1.593 3.068a3.745 3.745 0 0 1-1.043 3.296 3.745 3.745 0 0 1-3.296 1.043A3.745 3.745 0 0 1 12 21c-1.268 0-2.39-.63-3.068-1.593a3.746 3.746 0 0 1-3.296-1.043 3.746 3.746 0 0 1-1.043-3.296A3.745 3.745 0 0 1 3 12c0-1.268.63-2.39 1.593-3.068a3.745 3.746 0 0 1 1.043-3.296 3.746 3.746 0 0 1 3.296-1.043A3.746 3.746 0 0 1 12 3c1.268 0 2.39.63 3.068 1.593a3.746 3.746 0 0 1 3.296 1.043 3.746 3.746 0 0 1 1.043 3.296A3.745 3.745 0 0 1 21 12Z"
    />
  </svg>
									Badge

									
								</a>
							</li>
						</ul>
					</div>
				</div>
			</div>

	<div class="flex flex-wrap pt-1 pb-4 border-t border-b border-gray-200 dark:border-gray-700 px-4 space-y-3 sm:flex sm:space-y-0 sm:space-x-4">
          <div class="flex-items-center hidden mt-3 mr-4 text-sm font-medium text-gray-900 md:flex dark:text-white">
            Show records only for:
          </div>
          <div class="flex flex-wrap">
              <a href="">
                <div class="flex items-center mt-3 mr-4">
                    <input id="all-products" type="radio" value="" name="show-only" class="radio">
                  <label for="all-products" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">Badges</label>
                </div>
              </a>
              <a href="">
                <div class="flex items-center mt-3 mr-4">
                    <input id="all-products" type="radio" value="" name="show-only" class="radio">
                  <label for="all-products" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">Certificates</label>
                </div>
              </a>
			  <a class="underline mt-3 mr-4 font-medium text-blue-600 dark:text-blue-500 hover:underline text-sm" href="">Show All</a>
          </div>
		  <div class="flex items-center mt-3 mr-4 ml-auto">   
 <div class="relative w-48">
  <input
    type="text"
    id="simple-search"
    class="w-full px-2 py-1.5 bg-neutral-secondary-medium border border-default-medium rounded-md text-heading text-sm focus:ring-brand focus:border-brand placeholder:text-body"
    placeholder="Search Design..."
    required
  />
</div>


</div>
        </div>

		
		

			<!-- Table -->
			<div class="overflow-x-auto">
				<table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
					<thead class="text-xs uppercase bg-gray-50 dark:bg-gray-700">
						<tr>
							<th class="px-4 py-3">Design</th>
							<th class="px-4 py-3 text-right">Actions</th>
						</tr>
					</thead>

					<tbody>
						{#each filteredDesigns as design}
							<tr class="border-b border-gray-200 dark:border-gray-600">
								<!-- Design column -->
								<td class="p-4">
									<div class="flex items-center gap-3">
										<img
											src={design.image}
											alt={design.type}
											class="w-24 md:w-24 max-w-full max-h-full shadow-md" />

										<div>
											<div class="font-medium text-gray-900 dark:text-white">
												{design.name}
											</div>

											<div class="text-xs text-gray-500 flex gap-2">
												<span class="capitalize py-0.5 rounded"
													>Created on:
													{design.date}
												</span>
											</div>

											<div class="text-xs text-gray-500 mt-1 flex gap-2">
												<span
													class="capitalize bg-brand-softer border border-brand-subtle text-fg-brand-strong text-xs font-medium px-1.5 py-0.5 rounded">
													{design.type}
												</span>
											</div>
										</div>
									</div>
								</td>

								<!-- Actions -->
								<td class="px-4 py-2 text-right">
									<div class="flex justify-end gap-2">
										<button
											title="Preview"
											class="flex items-center gap-2 px-3 py-1.5 text-sm font-medium rounded-xs
		bg-blue-50 text-blue-700 hover:bg-blue-100 cursor-pointer">
											<svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
												<path
													stroke-linecap="round"
													stroke-linejoin="round"
													stroke-width="1.5"
													d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
												<path
													stroke-linecap="round"
													stroke-linejoin="round"
													stroke-width="1.5"
													d="M2.5 12S6.5 5 12 5s9.5 7 9.5 7-4 7-9.5 7-9.5-7-9.5-7z" />
											</svg>
											<span>Preview</span>
										</button>

										<button
											title="Edit"
											on:click={() =>
												(window.location.href = '/quick-certify/designs/edit-design')}
											class="flex items-center gap-2 px-3 py-1.5 text-sm font-medium rounded-xs
		bg-gray-100 text-gray-700 hover:bg-gray-200 cursor-pointer">
											<svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
												<path
													stroke-linecap="round"
													stroke-linejoin="round"
													stroke-width="1.5"
													d="M16.5 3.5l4 4L7 21H3v-4L16.5 3.5z" />
											</svg>
											<span>Edit</span>
										</button>

										<button
											title="Delete"
											class="flex items-center gap-2 px-3 py-1.5 text-sm font-medium rounded-xs
		bg-red-50 text-red-700 hover:bg-red-100 cursor-pointer">
											<svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
												<path
													stroke-linecap="round"
													stroke-linejoin="round"
													stroke-width="1.5"
													d="M6 7h12M9 7V4h6v3M10 11v6M14 11v6M5 7l1 13h12l1-13" />
											</svg>
											<span>Delete</span>
										</button>
									</div>
								</td>
							</tr>
						{/each}

						{#if filteredDesigns.length === 0}
							<tr>
								<td colspan="2" class="text-center py-6 text-gray-500"> No designs found </td>
							</tr>
						{/if}
					</tbody>
				</table>
			</div>
		</div>
	</div>
</section>
