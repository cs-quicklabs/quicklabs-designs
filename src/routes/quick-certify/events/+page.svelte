<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';
  let selectedType = 'all';
	const Events = [
	{
			id: 1,
			name: 'CS Quarterly Awards',
			type: 'Badge',
			date: '12 Dec 2024',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 2,
			name: 'CS Quarterly Awards',
			type: 'badge',
			date: '08 Dec 2024',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 3,
			name: 'CS Quarterly Awards',
			type: 'Badge',
			date: '12 Dec 2024',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 4,
			name: 'CS Quarterly Awards',
			type: 'badge',
			date: '08 Dec 2024',
			image: '/quick-certify/rashi.png'
		}
	];
	
	$: filteredEvents =
		selectedType === 'all' ? Events : Events.filter((e) => e.type === selectedType);
</script>

<NavBar />

<section>
<div class="px-4 mx-auto max-w-screen-2xl lg:px-8">
    <div class="bg-white border border-gray-200 rounded-md shadow-sm overflow-hidden">

      <!-- Header -->
      <div class="flex items-center justify-between px-4 py-4 border-b border-gray-200">
        <div>
          <h1 class="text-lg font-semibold text-gray-900">Groups of Events</h1>
          <p class="text-sm text-gray-500">4 Groups</p>
        </div>

        <button
          class="btn-primary">
          Add New Events
        </button>
      </div>

      <!-- Filters -->
      <div class="flex flex-wrap items-center gap-4 px-4 py-3 border-b border-gray-200">

        <!-- Filter dropdown -->
        <details class="relative">
          <summary
            class="cursor-pointer flex items-center gap-2 px-3 py-2 text-sm
                   border border-gray-200 rounded-md bg-gray-50 hover:bg-gray-100 list-none">
            <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                d="M3 4h18M6 10h12M10 16h4" />
            </svg>
            Filter by Events
          </summary>

          <div
            class="absolute z-10 mt-2 w-48 bg-white border border-gray-200 rounded-md shadow p-3">
            <p class="text-xs font-medium text-gray-500 mb-2">Select Events</p>

            {#each ['Course Completion','Top Performer','Participation','Achievement'] as event}
              <label class="flex items-center gap-2 py-1 text-sm text-gray-700">
                <input type="checkbox" class="rounded border-gray-300" />
                {event}
              </label>
            {/each}
          </div>
        </details>

        <!-- Search -->
        <div class="ml-auto">
          <input
            type="text"
            placeholder="Search Event by name..."
            class="w-48 px-3 py-2 text-sm border border-gray-200 rounded-md
                   bg-gray-50 focus:ring-1 focus:ring-gray-300 focus:outline-none" />
        </div>
      </div>

			<!-- Table -->
			<div class="overflow-x-auto">
				<table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">

					<tbody>
						{#each filteredEvents as Events}
							<tr class="border-b border-gray-200 dark:border-gray-600">
								<!-- Design column -->
								<td class="p-2">
									<div class="flex items-center gap-3">
										<img
											src={Events.image}
											alt={Events.type}
											class="w-24 md:w-24 max-w-full  shadow-md" />

										<div>
											<div class="font-medium text-gray-900 dark:text-white">
												{Events.name}
											</div>

											<div class="text-xs text-gray-500 flex gap-2">
												<span class="capitalize py-0.5 rounded"
													>Created on:
													{Events.date}
												</span>
											</div>

											<div class="text-xs text-gray-500 mt-1 flex gap-2">
												<span
													class="capitalize bg-brand-softer border border-brand-subtle text-fg-brand-strong text-xs font-medium px-1.5 py-0.5 rounded">
													{Events.type}
												</span>
											</div>
										</div>
									</div>
								</td>

								<!-- Actions -->
								<td class="px-4 py-1 text-right">
									<div class="flex justify-end gap-1">
										<button
											title="Preview"
											on:click={() =>
												(window.location.href = '/quick-certify/credential')}
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
											<span>View Credential</span>
										</button>

										<button
											title="Edit"
			
											class="flex items-center gap-2 px-3 py-1.5 text-sm font-medium rounded-xs
		bg-gray-100 text-gray-700 hover:bg-gray-200 cursor-pointer">
											<svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
												<path
													stroke-linecap="round"
													stroke-linejoin="round"
													stroke-width="1.5"
													d="M16.5 3.5l4 4L7 21H3v-4L16.5 3.5z" />
											</svg>
											<span>Issue Credential</span>
										</button>

										
									</div>
								</td>
							</tr>
						{/each}

						{#if filteredEvents.length === 0}
							<tr>
								<td colspan="2" class="text-center py-6 text-gray-500"> No designs found </td>
							</tr>
						{/if}
					</tbody>
				</table>
			</div>
		</div>
	
    
<nav aria-label="Page navigation example" class="flex justify-end p-4">
  <ul class="flex -space-x-px text-sm">
    <li>
      <a href="#"
        class="flex items-center justify-center px-3 h-9 text-sm font-medium
               bg-neutral-secondary-medium border border-default-medium
               rounded-s-base hover:bg-neutral-tertiary-medium">
        Previous
      </a>
    </li>

    <li>
      <a href="#" class="flex items-center justify-center w-9 h-9 text-sm border border-default-medium">
        1
      </a>
    </li>

    <li>
      <a href="#" class="flex items-center justify-center w-9 h-9 text-sm border border-default-medium">
        2
      </a>
    </li>

    <li>
      <a href="#" aria-current="page"
        class="flex items-center justify-center w-9 h-9 text-sm font-medium
               text-fg-brand bg-neutral-tertiary-medium border border-default-medium">
        3
      </a>
    </li>

    <li>
      <a href="#" class="flex items-center justify-center w-9 h-9 text-sm border border-default-medium">
        4
      </a>
    </li>

    <li>
      <a href="#" class="flex items-center justify-center w-9 h-9 text-sm border border-default-medium">
        5
      </a>
    </li>

    <li>
      <a href="#"
        class="flex items-center justify-center px-3 h-9 text-sm font-medium
               bg-neutral-secondary-medium border border-default-medium
               rounded-e-base hover:bg-neutral-tertiary-medium">
        Next
      </a>
    </li>
  </ul>
</nav>
</section>

