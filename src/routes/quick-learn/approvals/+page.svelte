<script>
	import NavBar from '$quick-learn/common/navbar/admin.svelte';
</script>

<NavBar />
<section class="bg-gray-50 dark:bg-gray-900 py-3 sm:py-5 min-h-screen">
	<div class="px-4 mx-auto max-w-screen-2xl lg:px-8">
		<div class="relative overflow-hidden bg-white shadow-md dark:bg-gray-800 sm:rounded-sm">
			<div class=" divide-y dark:divide-gray-700">
				<div
					class="flex-row items-center justify-between p-4 space-y-3 sm:flex sm:space-y-0 sm:space-x-4">
					<div>
						<h1 class="mr-3 text-lg font-semibold dark:text-white">Lesson Approvals</h1>
						<p class="text-gray-500 dark:text-gray-400 text-sm">
							Following lessons are waiting for approval after being created or updated by the team.
						</p>
					</div>
				</div>
			</div>

			<div class="overflow-x-auto">
				<table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
					<thead
						class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
						<tr>
							<th scope="col" class="px-4 py-3">Lesson</th>
							<th scope="col" class="px-4 py-3">Updated On</th>
							<th scope="col" class="px-4 py-3">Created On</th>
							<th scope="col" class="px-4 py-3">Created By</th>
						</tr>
					</thead>
					<tbody>
						<tr class="border-b dark:border-gray-600 hover:bg-gray-100 dark:hover:bg-gray-700">
							<th
								scope="row"
								class="px-4 py-2 font-medium text-gray-900 whitespace-nowrap dark:text-white">
								<div class="flex items-center">
									<a href="content/lesson/approve" class="ml-2 hover:underline">
										Git Cherry Pick command and its usage
									</a>
								</div>
							</th>
							<td class="px-4 py-2">June 12, 2024</td>

							<td class="px-4 py-2">June 12, 2024</td>
							<td class="px-4 py-2"> Aashish Dhawan </td>
						</tr>
						<tr class="border-b dark:border-gray-600 hover:bg-gray-100 dark:hover:bg-gray-700">
							<th
								scope="row"
								class="px-4 py-2 font-medium text-gray-900 whitespace-nowrap dark:text-white">
								<div class="flex items-center">
									<a href="content/lesson/approve" class="ml-2 hover:underline">
										Git Cherry Pick command and its usage
									</a>
								</div>
							</th>
							<td class="px-4 py-2">June 12, 2024</td>

							<td class="px-4 py-2">June 12, 2024</td>
							<td class="px-4 py-2"> Aashish Dhawan </td>
						</tr>
						<tr class="border-b dark:border-gray-600 hover:bg-gray-100 dark:hover:bg-gray-700">
							<th
								scope="row"
								class="px-4 py-2 font-medium text-gray-900 whitespace-nowrap dark:text-white">
								<div class="flex items-center">
									<a href="content/lesson/approve" class="ml-2 hover:underline">
										Git Cherry Pick command and its usage
									</a>
								</div>
							</th>
							<td class="px-4 py-2">June 12, 2024</td>
							<td class="px-4 py-2">June 12, 2024</td>

							<td class="px-4 py-2"> Aashish Dhawan </td>
						</tr>
						<tr class="border-b dark:border-gray-600 hover:bg-gray-100 dark:hover:bg-gray-700">
							<th
								scope="row"
								class="px-4 py-2 font-medium text-gray-900 whitespace-nowrap dark:text-white">
								<div class="flex items-center">
									<a href="content/lesson/approve" class="ml-2 hover:underline">
										Git Cherry Pick command and its usage
									</a>
								</div>
							</th>
							<td class="px-4 py-2">June 12, 2024</td>
							<td class="px-4 py-2">June 12, 2024</td>

							<td class="px-4 py-2"> Aashish Dhawan </td>
						</tr>
					</tbody>
				</table>
			</div>
		</div>
	</div>
</section>
