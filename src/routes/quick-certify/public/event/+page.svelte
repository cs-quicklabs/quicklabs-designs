<script>
	import Header from '$quick-certify/common/navbar/header.svelte';
	import Footer from '$quick-certify/common/navbar/footer.svelte';
</script>

<Header />
<div class="bg-gray-50 p-4">
	<div
		class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 p-4 rounded-sm border border-stroke-dark bg-white border-gray-200">
		<div>
			<nav class="sm:hidden" aria-label="Back">
				<a href="#" class="flex items-center text-sm font-medium text-gray-500 hover:text-gray-700">
					<svg
						class="mr-1 -ml-1 size-5 shrink-0 text-gray-400"
						viewBox="0 0 20 20"
						fill="currentColor"
						aria-hidden="true"
						data-slot="icon">
						<path
							fill-rule="evenodd"
							d="M11.78 5.22a.75.75 0 0 1 0 1.06L8.06 10l3.72 3.72a.75.75 0 1 1-1.06 1.06l-4.25-4.25a.75.75 0 0 1 0-1.06l4.25-4.25a.75.75 0 0 1 1.06 0Z"
							clip-rule="evenodd" />
					</svg>
					Back
				</a>
			</nav>
			<nav class="hidden sm:flex" aria-label="Breadcrumb">
				<ol role="list" class="flex items-center space-x-2">
					<li>
						<div class="flex">
							<a
								href="/quick-certify/public/company"
								class="text-sm font-medium text-gray-500 hover:text-gray-700 hover:underline"
								>Issuer Profile</a>
						</div>
					</li>
					<li>
						<div class="flex items-center">
							<svg
								class="size-5 shrink-0 text-gray-400"
								viewBox="0 0 20 20"
								fill="currentColor"
								aria-hidden="true"
								data-slot="icon">
								<path
									fill-rule="evenodd"
									d="M8.22 5.22a.75.75 0 0 1 1.06 0l4.25 4.25a.75.75 0 0 1 0 1.06l-4.25 4.25a.75.75 0 0 1-1.06-1.06L11.94 10 8.22 6.28a.75.75 0 0 1 0-1.06Z"
									clip-rule="evenodd" />
							</svg>
							<a
								href="/quick-certify/public/event"
								class="ml-2 text-sm font-medium text-gray-500 hover:text-gray-700 hover:underline"
								>Events</a>
						</div>
					</li>
				</ol>
			</nav>
		</div>
		<div class="mt-2 md:flex md:items-center md:justify-between">
			<div class="min-w-0 flex-1">
				<h2 class="text-2xl/7 font-bold text-gray-900 sm:truncate sm:text-3xl sm:tracking-tight">
					Events
				</h2>
			</div>
		</div>
	</div>
	<div
		class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 p-4 rounded-sm border border-stroke-dark bg-white mt-4 border-gray-200">
		<!-- Start coding here -->
		<div class="relative bg-white dark:bg-gray-800 sm:rounded-sm">
			<div class="flex flex-col items-center justify-between md:flex-row md:space-y-0">
				<div class="w-full me-4">
					<form class="flex items-center">
						<label for="simple-search" class="sr-only">Search</label>
						<div class="relative w-full">
							<div class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
								<svg
									aria-hidden="true"
									class="w-5 h-5 text-gray-500 dark:text-gray-400"
									fill="currentColor"
									viewbox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg">
									<path
										fill-rule="evenodd"
										d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
										clip-rule="evenodd" />
								</svg>
							</div>
							<input
								type="text"
								id="simple-search"
								class="block w-full p-1.5 pl-10 text-sm text-gray-900 border border-gray-300 rounded-sm bg-gray-50 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
								placeholder="Search event by name"
								required="" />
						</div>
					</form>
				</div>
				<div
					class="flex flex-col items-stretch justify-end flex-shrink-0 w-full space-y-2 md:w-auto md:flex-row md:space-y-0 md:items-center md:space-x-3">
					<div class="flex items-center w-full space-x-3 md:w-auto">
						<button
							id="filterDropdownButton"
							data-dropdown-toggle="filterDropdown"
							class="flex items-center justify-center w-full px-4 py-1.5 text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-sm md:w-auto focus:outline-none hover:bg-gray-100 hover:text-primary-700 focus:z-10 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700"
							type="button">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								aria-hidden="true"
								class="w-4 h-4 mr-2 text-gray-400"
								viewbox="0 0 20 20"
								fill="currentColor">
								<path
									fill-rule="evenodd"
									d="M3 3a1 1 0 011-1h12a1 1 0 011 1v3a1 1 0 01-.293.707L12 11.414V15a1 1 0 01-.293.707l-2 2A1 1 0 018 17v-5.586L3.293 6.707A1 1 0 013 6V3z"
									clip-rule="evenodd" />
							</svg>
							Sort By
							<svg
								class="-mr-1 ml-1.5 w-5 h-5"
								fill="currentColor"
								viewbox="0 0 20 20"
								xmlns="http://www.w3.org/2000/svg"
								aria-hidden="true">
								<path
									clip-rule="evenodd"
									fill-rule="evenodd"
									d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" />
							</svg>
						</button>
						<!-- Dropdown menu -->
						<div
							id="filterDropdown"
							class="z-10 hidden w-48 p-3 bg-white rounded-sm shadow dark:bg-gray-700">
							<ul class="space-y-2 text-sm cursor-pointer" aria-labelledby="dropdownDefault">
								<li class="flex items-center hover:underline cursor-pointer">
									<label
										for="apple"
										class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-100 cursor-pointer">
										Newest First
									</label>
								</li>
								<li class="flex items-center hover:underline cursor-pointer">
									<label
										for="fitbit"
										class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-100 cursor-pointer">
										Oldest First
									</label>
								</li>
							</ul>
						</div>
					</div>
				</div>
			</div>
			<div class="grid grid-cols-1 gap-4 sm:grid-cols-3 mt-8">
				<div
					class="max-w-sm bg-white border border-gray-200 rounded-sm shadow-sm dark:bg-gray-800 dark:border-gray-700">
					<a href="#">
						<img class="rounded-t-sm" src="/quick-certify/rashi.png" alt="" />
					</a>
					<div class="p-5">
						<a href="#">
							<h5 class="mb-2 text-xl font-bold tracking-tight text-gray-900 dark:text-white">
								Understanding Clean Coding Practices
							</h5>
						</a>
						<p class="mb-3 font-normal text-sm text-gray-700 dark:text-gray-400">
							Created on June 12, 2024
						</p>
					</div>
				</div>
				<div
					class="max-w-sm bg-white border border-gray-200 rounded-sm shadow-sm dark:bg-gray-800 dark:border-gray-700">
					<a href="#">
						<img class="rounded-t-sm" src="/quick-certify/rashi.png" alt="" />
					</a>
					<div class="p-5">
						<a href="#">
							<h5 class="mb-2 text-xl font-bold tracking-tight text-gray-900 dark:text-white">
								Understanding Clean Coding Practices
							</h5>
						</a>
						<p class="mb-3 font-normal text-sm text-gray-700 dark:text-gray-400">
							Created on June 12, 2024
						</p>
					</div>
				</div>
				<div
					class="max-w-sm bg-white border border-gray-200 rounded-sm shadow-sm dark:bg-gray-800 dark:border-gray-700">
					<a href="#">
						<img class="rounded-t-sm" src="/quick-certify/rashi.png" alt="" />
					</a>
					<div class="p-5">
						<a href="#">
							<h5 class="mb-2 text-xl font-bold tracking-tight text-gray-900 dark:text-white">
								Understanding Clean Coding Practices
							</h5>
						</a>
						<p class="mb-3 font-normal text-sm text-gray-700 dark:text-gray-400">
							Created on June 12, 2024
						</p>
					</div>
				</div>
				<div
					class="max-w-sm bg-white border border-gray-200 rounded-sm shadow-sm dark:bg-gray-800 dark:border-gray-700">
					<a href="#">
						<img class="rounded-t-sm" src="/quick-certify/rashi.png" alt="" />
					</a>
					<div class="p-5">
						<a href="#">
							<h5 class="mb-2 text-xl font-bold tracking-tight text-gray-900 dark:text-white">
								Understanding Clean Coding Practices
							</h5>
						</a>
						<p class="mb-3 font-normal text-sm text-gray-700 dark:text-gray-400">
							Created on June 12, 2024
						</p>
					</div>
				</div>
				<div
					class="max-w-sm bg-white border border-gray-200 rounded-sm shadow-sm dark:bg-gray-800 dark:border-gray-700">
					<a href="#">
						<img class="rounded-t-sm" src="/quick-certify/rashi.png" alt="" />
					</a>
					<div class="p-5">
						<a href="#">
							<h5 class="mb-2 text-xl font-bold tracking-tight text-gray-900 dark:text-white">
								Understanding Clean Coding Practices
							</h5>
						</a>
						<p class="mb-3 font-normal text-sm text-gray-700 dark:text-gray-400">
							Created on June 12, 2024
						</p>
					</div>
				</div>
				<div
					class="max-w-sm bg-white border border-gray-200 rounded-sm shadow-sm dark:bg-gray-800 dark:border-gray-700">
					<a href="#">
						<img class="rounded-t-sm" src="/quick-certify/rashi.png" alt="" />
					</a>
					<div class="p-5">
						<a href="#">
							<h5 class="mb-2 text-xl font-bold tracking-tight text-gray-900 dark:text-white">
								Understanding Clean Coding Practices
							</h5>
						</a>
						<p class="mb-3 font-normal text-sm text-gray-700 dark:text-gray-400">
							Created on June 12, 2024
						</p>
					</div>
				</div>
			</div>
			<div class="relative overflow-hidden bg-white mt-8">
				<nav
					class="flex flex-col items-start justify-end p-4 space-y-3 md:flex-row md:items-center md:space-y-0"
					aria-label="Table navigation">
					<span class="text-sm font-normal text-gray-500 dark:text-gray-400"
						>Showing <span class="font-semibold text-gray-900 dark:text-white">1-10</span> of
						<span class="font-semibold text-gray-900 dark:text-white me-8">1000</span></span>
					<ul class="inline-flex items-stretch -space-x-px">
						<li>
							<a
								href="#"
								class="flex items-center justify-center h-full py-1.5 px-3 ml-0 text-gray-500 bg-white rounded-l-lg border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white">
								<span class="sr-only">Previous</span>
								<svg
									class="w-5 h-5"
									aria-hidden="true"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg">
									<path
										fill-rule="evenodd"
										d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"
										clip-rule="evenodd"></path>
								</svg>
							</a>
						</li>
						<li>
							<a
								href="#"
								class="flex items-center justify-center px-3 py-2 text-sm leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
								>1</a>
						</li>
						<li>
							<a
								href="#"
								class="flex items-center justify-center px-3 py-2 text-sm leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
								>2</a>
						</li>
						<li>
							<a
								href="#"
								aria-current="page"
								class="z-10 flex items-center justify-center px-3 py-2 text-sm leading-tight border text-primary-600 bg-primary-50 border-primary-300 hover:bg-primary-100 hover:text-primary-700 dark:border-gray-700 dark:bg-gray-700 dark:text-white"
								>3</a>
						</li>
						<li>
							<a
								href="#"
								class="flex items-center justify-center px-3 py-2 text-sm leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
								>...</a>
						</li>
						<li>
							<a
								href="#"
								class="flex items-center justify-center px-3 py-2 text-sm leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
								>100</a>
						</li>
						<li>
							<a
								href="#"
								class="flex items-center justify-center h-full py-1.5 px-3 leading-tight text-gray-500 bg-white rounded-r-lg border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white">
								<span class="sr-only">Next</span>
								<svg
									class="w-5 h-5"
									aria-hidden="true"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg">
									<path
										fill-rule="evenodd"
										d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
										clip-rule="evenodd"></path>
								</svg>
							</a>
						</li>
					</ul>
				</nav>
			</div>
		</div>
	</div>
</div>
<Footer />
