<script>
	import NavBar from '$quick-learn/common/navbar/admin.svelte';
	import TeamSettingsNavBar from '$quick-learn/common/navbar/team.svelte';
</script>

<NavBar />

<main class="max-w-7xl mx-auto pb-10 lg:py-12 lg:px-8">
	<div class="lg:grid lg:grid-cols-12 lg:gap-x-5">
		<aside class="px-2 py-6 sm:px-6 lg:py-0 lg:px-0 lg:col-span-3">
			<TeamSettingsNavBar />
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
					<button
						type="submit"
						class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
						>Save</button>
				</form>
			</div>
		</main>
	</div>
</main>
