<script>
	import NavBar from '$lib/tosupportme/navbar.svelte';
</script>

<div class="w-full bg-gray-50 h-screen">
	<NavBar />
	<main class="mx-auto max-w-4xl pb-10 lg:py-12 lg:px-8 md:py-8 md:px-4 bg-gray-50 ">
		<div class="bg-white shadow sm:rounded-lg">
			<div class="px-4 py-5 sm:p-6">
				<h3 class="text-base font-semibold leading-6 text-gray-900">Create Your Team</h3>
				<div class="mt-2 w-full text-sm text-gray-500">
					<p>
						Please select a name for your team. This will be used as slug to create a URL for your
						product as well.
					</p>
				</div>
				<form class="mt-5 sm:flex sm:items-center">
					<div class="w-full sm:max-w-xs">
						<label for="email" class="sr-only">Email</label>
						<div class="mt-1 flex rounded-md shadow-sm">
							<span class="inline-flex items-center rounded-l-md border border-r-0 border-gray-300 bg-gray-50 px-3 text-gray-500 sm:text-sm">tosupport.me/</span>
							<input type="text" name="company-website" id="company-website" class="border block w-full min-w-0 flex-1 rounded-none rounded-r-md border-gray-300 px-3 py-2 focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm" placeholder="skia" />
						</div>
					</div>
					<button type="submit" class="mt-3 inline-flex w-full items-center justify-center rounded-md border border-transparent bg-indigo-600 px-4 py-2 font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 sm:mt-0 sm:ml-3 sm:w-auto sm:text-sm">Save</button>
				</form>
				<p class="mt-2 text-sm text-red-600" id="email-error">
					The team name is already taken. Please select another.
				</p>
			</div>
		</div>
	</main>
</div>