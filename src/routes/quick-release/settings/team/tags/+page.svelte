<script>
	import Fullnavbar from '$quick-release/shared/fullnavbar.svelte';
</script>

<Fullnavbar />

<main class="max-w-7xl mx-auto pb-10 lg:py-12 lg:px-8">
	<div class="lg:grid lg:grid-cols-12 lg:gap-x-5">
		<aside class="px-2 py-6 sm:px-6 lg:py-0 lg:px-0 lg:col-span-3">
			<nav class="space-y-1">
				<a
					href="/quick-release/settings/team/general"
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
					href="/quick-release/settings/team/tags"
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
						></svg> <span class="truncate ml-2">Tags</span></a>
			</nav>
		</aside>

		<main class="max-w-xl pb-12 px-4 lg:col-span-6">
			<div>
				<h1 class="text-lg font-semibold dark:text-white">Tags</h1>
				<p class="text-gray-500 dark:text-gray-400 text-sm">
					Tags can be assigned to changelogs or posts to define the categories they belong to.
				</p>

				<form class="w-full mt-6">
					<div class="mb-5 mt-6">
						<label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
							>Add new Tag</label>
						<input
							type="email"
							id="email"
							class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
							placeholder="iOS"
							required />
					</div>
					<button
						type="submit"
						class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
						>Save</button>
				</form>

				<div class="relative overflow-x-auto mt-8">
					<table class="w-full text-sm text-left rtl:text-right text-gray-500 dark:text-gray-400">
						<thead
							class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
							<tr>
								<th scope="col" class="px-6 py-3 w-full"> Tag name </th>
								<th scope="col" class="px-6 py-3"> Action </th>
							</tr>
						</thead>
						<tbody>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-b dark:border-gray-700">
								<th
									scope="row"
									class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
									Mobile
								</th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline"
										>Edit</a>
									<a
										href="#"
										class="ml-2 font-medium text-red-600 dark:text-red-500 hover:underline"
										>Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-b dark:border-gray-700">
								<th
									scope="row"
									class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
									Web
								</th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline"
										>Edit</a>
									<a
										href="#"
										class="ml-2 font-medium text-red-600 dark:text-red-500 hover:underline"
										>Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-b dark:border-gray-700">
								<th
									scope="row"
									class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
									Backend
								</th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline"
										>Edit</a>
									<a
										href="#"
										class="ml-2 font-medium text-red-600 dark:text-red-500 hover:underline"
										>Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-b dark:border-gray-700">
								<th
									scope="row"
									class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
									Refactoring
								</th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline"
										>Edit</a>
									<a
										href="#"
										class="ml-2 font-medium text-red-600 dark:text-red-500 hover:underline"
										>Delete</a>
								</td>
							</tr>
							<tr>
								<th
									scope="row"
									class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
									Enhancements
								</th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline"
										>Edit</a>
									<a
										href="#"
										class="ml-2 font-medium text-red-600 dark:text-red-500 hover:underline"
										>Delete</a>
								</td>
							</tr>
						</tbody>
					</table>
				</div>
			</div>
		</main>
	</div>
</main>
