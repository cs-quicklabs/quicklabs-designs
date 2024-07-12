<script>
	import NavBar from '$quick-learn/common/navbar/admin.svelte';
</script>

<NavBar />

<main class="max-w-7xl mx-auto pb-10 lg:py-12 lg:px-8">
	<div class="lg:grid lg:grid-cols-12 lg:gap-x-5">
		<aside class="px-2 py-6 sm:px-6 lg:py-0 lg:px-0 lg:col-span-3">
			<nav class="space-y-1">
				<a
					href="/quick-learn/settings/team/general"
					class="bg-gray-200 text-gray-900 hover:bg-gray-200 rounded px-3 py-2 flex items-center text-sm font-medium">
					<!-- Heroicon name: outline/user-circle -->
					<svg
						class="w-6 h-6 text-gray-800 dark:text-white"
						aria-hidden="true"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24">
						<path
							stroke="currentColor"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M15 9h3m-3 3h3m-3 3h3m-6 1c-.3-.6-1-1-1.6-1H7.6c-.7 0-1.3.4-1.6 1M4 5h16c.6 0 1 .4 1 1v12c0 .6-.4 1-1 1H4a1 1 0 0 1-1-1V6c0-.6.4-1 1-1Zm7 5a2 2 0 1 1-4 0 2 2 0 0 1 4 0Z" />
					</svg>
					<span class="truncate ml-2"> General </span>
				</a>
				<a
					href="/quick-learn/settings/team/tags"
					class="text-gray-900 hover:text-gray-900 hover:bg-gray-50 rounded px-3 py-2 flex items-center text-sm font-medium"
					><svg
						class="w-6 h-6 text-gray-800 dark:text-white"
						aria-hidden="true"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						><path
							stroke="currentColor"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M12 14v3m-3-6V7a3 3 0 1 1 6 0v4m-8 0h10c.6 0 1 .4 1 1v7c0 .6-.4 1-1 1H7a1 1 0 0 1-1-1v-7c0-.6.4-1 1-1Z"
						></path
						></svg> <span class="truncate ml-2">Tag</span></a>
			</nav>
		</aside>

		<main class="max-w-xl pb-12 px-4 lg:col-span-6">
			<div>
				<h1 class="text-lg font-semibold dark:text-white">Team Settings</h1>
				<p class="text-gray-500 dark:text-gray-400 text-sm">Change settings of your team.</p>

				<form class="w-full mt-6">
					<div class="sm:col-span-2">
						<label
							class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
							for="file_input">Upload Team Logo</label>
						<div class="items-center w-full sm:flex">
							<img
								class="w-20 h-20 mb-4 rounded-full sm:mr-4 sm:mb-0"
								src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/helene-engels.png"
								alt="Helene avatar" />
						</div>
					</div>

					<div class="mb-5 mt-6">
						<label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
							>Team Name</label>
						<input
							type="email"
							id="email"
							class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
							value="Quick Connect"
							required />
					</div>
					<div class="mb-5">
						<label
							for="user-permissions"
							class="inline-flex items-center mb-2 text-sm font-medium text-gray-900 dark:text-white">
							Slug
							<button
								type="button"
								data-tooltip-target="tooltip-dark"
								data-tooltip-style="dark"
								class="ml-1">
								<svg
									aria-hidden="true"
									class="w-4 h-4 text-gray-400 hover:text-gray-900 dark:text-gray-500 dark:hover:text-white"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
									><path
										fill-rule="evenodd"
										d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-8-3a1 1 0 00-.867.5 1 1 0 11-1.731-1A3 3 0 0113 8a3.001 3.001 0 01-2 2.83V11a1 1 0 11-2 0v-1a1 1 0 011-1 1 1 0 100-2zm0 8a1 1 0 100-2 1 1 0 000 2z"
										clip-rule="evenodd"></path
									></svg>
								<span class="sr-only">Show information</span>
							</button>
							<div
								id="tooltip-dark"
								role="tooltip"
								class="inline-block absolute invisible z-10 py-2 px-3 max-w-sm text-xs font-normal text-white bg-gray-900 rounded-lg shadow-sm opacity-0 tooltip dark:bg-gray-700">
								Slug specifies the unique identifier for your team. It is used to create a unique
								URL for your team. You can use letters, numbers, and hyphens.
								<div class="tooltip-arrow" data-popper-arrow></div>
							</div>
						</label>

						<input
							type="text"
							id="error"
							class="bg-red-50 border border-red-500 text-red-900 placeholder-red-700 text-sm rounded-lg focus:ring-red-500 dark:bg-gray-700 focus:border-red-500 block w-full p-2.5 dark:text-red-500 dark:placeholder-red-500 dark:border-red-500"
							placeholder="Quick Connect" />
						<p class="mt-2 text-sm text-red-600 dark:text-red-500">
							<span class="font-medium">Slug is not unique</span>.
						</p>
					</div>

					<button
						type="submit"
						class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
						>Save</button>
				</form>
			</div>
		</main>
	</div>
</main>
