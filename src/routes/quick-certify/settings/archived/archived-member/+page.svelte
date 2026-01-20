<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';
	import SideBar from '$quick-certify/common/navbar/archived-member.svelte';
	import InfoButton from '$lib/tooltip.svelte';
</script>

<NavBar />

<main class="max-w-7xl mx-auto pb-10 lg:py-12 lg:px-8">
	<div class="lg:grid lg:grid-cols-12 lg:gap-x-5">
		<SideBar />

		<main class="max-w-xl px-4 pb-12 lg:col-span-8">
				<div class="pb-4 ml-4">
					<h1 class="text-lg font-medium text-gray-900">Archived Users</h1>
					<p class="mt-1 text-sm text-gray-500">Following users have been deactivated.</p>
				</div>

				<!-- Search -->
				<div class="flex space-x-4 ml-4 mb-4">
					<div class="flex-1 min-w-0" data-behavior="autocomplete" data-controller="nav-search" data-nav-search-url-value="/search/deactivated">
						<label for="search" class="sr-only">Search</label>
						<div class="relative rounded-md shadow-sm">
							<input
								type="search"
								id="search"
								name="search"
								class="pl-10 form-input-field"
								placeholder="Search"
								data-nav-search-target="input"
								autocomplete="off"
								spellcheck="false"
							/>
						</div>
						<ul data-nav-search-target="results" hidden class="absolute left-0 z-10 w-full mt-1 origin-top-right bg-white rounded-md shadow-lg"></ul>
					</div>
				</div>

				<!-- Users Table -->
				
					<table class="table border-separate mt-4 w-full">
						<thead class="bg-gray-50"></thead>
						<tbody id="employees" data-infinite-scroll-target="entries" class="table-body">

							<!-- User Row Component -->
							{#each [1,2] as userId}
								<tr id="user_{userId}">
									<td class="table-cell whitespace-nowrap">
										<div class="flex items-center">
											<div class="flex-1 min-w-0 sm:flex sm:items-center sm:justify-between">
												<div>
													<a href="/quick-learn/team/1" class="truncate hover:text-gray-600 hover:underline">
														<div class="flex text-sm font-medium text-gray-600 truncate">
															<p>Rohit Sharma</p>
															<p class="ml-1 font-normal text-gray-500">Manager</p>
														</div>
													</a>
													<div class="flex-1 w-full mt-2">
														<div class="flex items-center text-sm text-gray-500">
															<svg class="flex-shrink-0 mr-1.5 h-5 w-5 text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
																<path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"/>
															</svg>
															<p>Deactivated on July 23, 2024 by Aashish Dhawan</p>
														</div>
													</div>
												</div>
											</div>
										</div>
									</td>
									<td class="table-cell">
										<div class="flex justify-end space-x-2">
											<button class="btn-Secondary link" data-modal-target="popup-modal-activate" data-modal-toggle="popup-modal-activate" href="/1/employees/426">Activate</button>
											<button class="btn-inline-red" data-modal-target="popup-modal" data-modal-toggle="popup-modal" href="/1/employees/426">Delete</button>
										</div>
									</td>
								</tr>
							{/each}

						</tbody>
					</table>
		</main>
	</div>
</main>

<!-- Delete Modal -->
<div id="popup-modal" tabindex="-1" class="hidden fixed inset-0 z-50 flex justify-center items-center overflow-auto p-4">
	<div class="relative w-full max-w-md max-h-full">
		<div class="relative bg-white rounded-lg shadow dark:bg-gray-700 text-center p-5">
			<button type="button" class="absolute top-3 right-2.5 text-gray-400 hover:bg-gray-200 hover:text-gray-900 rounded-lg w-8 h-8 flex justify-center items-center dark:hover:bg-gray-600 dark:hover:text-white" data-modal-hide="popup-modal">
				<svg class="w-3 h-3" fill="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 14 14" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
					<path d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6"/>
				</svg>
				<span class="sr-only">Close modal</span>
			</button>
			<svg class="mx-auto mb-4 w-12 h-12 text-red-600 dark:text-gray-200" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 20 20" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
				<path d="M10 11V6m0 8h.01M19 10a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"/>
			</svg>
			<h3 class="text-lg font-bold text-gray-700 dark:text-gray-400">Are you sure you want to delete this user?</h3>
			<p class="mb-4 text-xs text-gray-500">All the information regarding this user will be lost. If this user has created content, it will be assigned to the super admin.</p>
			<div class="flex justify-center mt-4">
				<button data-modal-hide="popup-modal" class="text-white bg-red-600 hover:bg-red-800 focus:ring-4 focus:outline-none focus:ring-red-300 font-medium rounded-lg text-sm px-5 py-2.5">Yes, Delete</button>
				<button data-modal-hide="popup-modal" class="ml-3 text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-lg px-5 py-2.5 hover:bg-gray-100 hover:text-blue-700">No, Cancel</button>
			</div>
		</div>
	</div>
</div>

<!-- Activate Modal -->
<div id="popup-modal-activate" tabindex="-1" class="hidden fixed inset-0 z-50 flex justify-center items-center overflow-auto p-4">
	<div class="relative w-full max-w-md max-h-full">
		<div class="relative bg-white rounded-lg shadow dark:bg-gray-700 text-center p-5">
			<button type="button" class="absolute top-3 right-2.5 text-gray-400 hover:bg-gray-200 hover:text-gray-900 rounded-lg w-8 h-8 flex justify-center items-center dark:hover:bg-gray-600 dark:hover:text-white" data-modal-hide="popup-modal-activate">
				<svg class="w-3 h-3" fill="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 14 14" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
					<path d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6"/>
				</svg>
				<span class="sr-only">Close modal</span>
			</button>
			<svg class="mx-auto mb-4 w-12 h-12 text-blue-600 dark:text-gray-200" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 20 20" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
				<path d="M10 11V6m0 8h.01M19 10a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"/>
			</svg>
			<h3 class="text-lg font-bold text-gray-700 dark:text-gray-400">Are you sure you want to activate this user?</h3>
			<p class="mb-4 text-xs text-gray-500">Once this user is activated, they will be able to access the system and perform actions based on their roles and permissions.</p>
			<div class="flex justify-center mt-4">
				<button data-modal-hide="popup-modal-activate" class="btn-primary">Yes, Activate</button>
				<button data-modal-hide="popup-modal-activate" class="ml-3 text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-lg px-5 py-2.5 hover:bg-gray-100 hover:text-blue-700">No, Cancel</button>
			</div>
		</div>
	</div>
</div>
