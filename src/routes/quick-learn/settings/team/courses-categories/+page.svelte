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
				<h1 class="text-lg font-semibold dark:text-white">Courses Categories</h1>
				<p class="text-gray-500 dark:text-gray-400 text-sm">
					Courses can belong to a category. A category could be a way to group learning courses. For
					example, a you can create a learning course from a book, a blog, a video, for a software
					application or for any onboarding needs.
				</p>

				<form class="w-full mt-6">
					<div class="mb-5 mt-6">
						<label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
							>Add New Course Category</label>
						<input
							type="email"
							id="email"
							class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
							placeholder="Engineering"
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
								<th scope="col" class="px-6 py-3 w-full"> Category name </th>
								<th scope="col" class="px-6 py-3"> Action </th>
							</tr>
						</thead>
						<tbody>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-b dark:border-gray-700">
								<th
									scope="row"
									class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
									Book
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
									Software Application
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
							</tr>
							<tr>
								<th class="p-2">
									<input
										type="text"
										id="last_name"
										class="p-2 bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
										placeholder="Engineering"
										value="Production Deployment"
										required />
								</th>
								<td>
									<button
										type="submit"
										class="text-white ml-2 bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
										>Save</button>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-b dark:border-gray-700 border-t">
								<th
									scope="row"
									class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
									Recruitment Process
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
