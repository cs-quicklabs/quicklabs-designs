<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';
</script>

<NavBar />

<section class="bg-gray-50 dark:bg-gray-900 py-3 sm:py-5 min-h-screen">
	<div class="px-4 mx-auto max-w-screen-2xl lg:px-8">
		<div class="relative overflow-hidden bg-white shadow-md dark:bg-gray-800 sm:rounded-sm">
			<div class=" divide-y dark:divide-gray-700">
				<div
					class="flex-row items-center justify-between p-4 space-y-3 sm:flex sm:space-y-0 sm:space-x-4">
					<div>
						<h1 class="mr-3 form-title">Team</h1>
						<p class="form-subtitle">
							Manage all your existing <span class="font-bold">4</span> team members or add a new one.
						</p>
					</div>
					<div class="flex space-x-4">
						<div class="flex space-x-2 items-center w-full">
							<a
								type="button"
								href="/quick-certify/settings/account/team/add"
								class="btn-primary w-full">
								Add new member
							</a>
						</div>
					</div>
				</div>
			</div>
			<div
				class="flex flex-wrap pt-1 pb-4 border-t border-b  border-gray-200 dark:border-gray-200 px-4 space-y-3 sm:flex sm:space-y-0 sm:space-x-4">
				<div
					class="items-center hidden mt-3 mr-4 text-sm font-medium text-gray-900 md:flex dark:text-white">
					Show records only for:
				</div>
				<div class="flex flex-wrap">
					<a href="">
						<div class="flex items-center mt-3 mr-4">
							<input
								id="all-products"
								type="radio"
								value=""
								name="show-only"
								class="w-4 h-4 bg-gray-100 border-gray-300 text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600 cursor-pointer"
								checked />
							<label
								for="all-products"
								class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
								Admin
							</label>
						</div>
					</a>
					<a href="">
						<div class="flex items-center mt-3 mr-4">
							<input
								id="all-products"
								type="radio"
								value=""
								name="show-only"
								class="w-4 h-4 bg-gray-100 border-gray-300 text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600 cursor-pointer"
								checked />
							<label
								for="all-products"
								class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
								Managers
							</label>
						</div>
					</a>
					<a href="">
						<div class="flex items-center mt-3 mr-4">
							<input
								id="all-products"
								type="radio"
								value=""
								name="show-only"
								class="w-4 h-4 bg-gray-100 border-gray-300 text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600 cursor-pointer"
								checked />
							<label
								for="all-products"
								class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
								Designers
							</label>
						</div>
					</a>
					<a
						class="underline mt-3 mr-4 font-medium text-blue-600 dark:text-blue-500 hover:underline text-sm"
						>Show All</a>
				</div>
			</div>
			<div class="overflow-x-auto">
				<table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
					<thead
						class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
						<tr>
							<th scope="col" class="px-4 py-3">User</th>
							<th scope="col" class="px-4 py-3">Role</th>
							<th scope="col" class="px-4 py-3">Email</th>
							<th scope="col" class="px-4 py-3">Status</th>
							<th scope="col" class="px-4 py-3 whitespace-nowrap">Last Login</th>
							<th scope="col" class="px-4 py-3 whitespace-nowrap">Added On</th>
						</tr>
					</thead>
					<tbody>
						<tr class="border-b border-gray-200 dark:border-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">
							<th scope="row" class="px-4 py-2 form-text-normal">
								<div class="flex items-center">
									<a href="team/1" class="hover:underline"> Aashish Dhawan </a>
								</div>
							</th>
							<td class="px-4 py-2">
								<div
									class="inline-flex items-center bg-primary-100 text-primary-800 text-xs font-medium px-2 py-0.5 rounded dark:bg-primary-900 dark:text-primary-300">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										class="h-3.5 w-3.5 mr-1"
										viewbox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true">
										<path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z" />
										<path
											fill-rule="evenodd"
											clip-rule="evenodd"
											d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" />
									</svg>
									Super Admin
								</div>
							</td>
							<td class="px-4 py-2"> aashishdhawan-yweir8832khsd@gmail.com </td>
							<td class="px-4 py-2 form-text-normal">
								<div class="flex items-center">
									<div class="w-3 h-3 mr-2 bg-green-500 border rounded-full"></div>
									Active
								</div>
							</td>
							<td class="px-4 py-2">Nov 11, 2022</td>
							<td class="px-4 py-2">Dec 11, 2024</td>
						</tr>
						<tr class="border-b border-gray-200 dark:border-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">
							<th scope="row" class="px-4 py-2 form-text-normal">
								<div class="flex items-center">
									<a href="team/1" class="hover:underline"> Peter Parker </a>
								</div>
							</th>
							<td class="px-4 py-2">
								<div
									class="inline-flex items-center bg-primary-100 text-primary-800 text-xs font-medium px-2 py-0.5 rounded dark:bg-primary-900 dark:text-primary-300">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										class="h-3.5 w-3.5 mr-1"
										viewbox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true">
										<path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z" />
										<path
											fill-rule="evenodd"
											clip-rule="evenodd"
											d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" />
									</svg>
									Manager
								</div>
							</td>
							<td class="px-4 py-2"> spiderman@gmail.com </td>
							<td class="px-4 py-2 form-text-normal">
								<div class="flex items-center">
									<div class="w-3 h-3 mr-2 bg-green-500 border rounded-full"></div>
									Active
								</div>
							</td>
							<td class="px-4 py-2">Nov 11, 2022</td>
							<td class="px-4 py-2">Dec 11, 2024</td>
						</tr>
						<tr class="border-b border-gray-200 dark:border-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">
							<th scope="row" class="px-4 py-2 form-text-normal">
								<div class="flex items-center">
									<a href="team/1" class="hover:underline"> Nick Furry </a>
								</div>
							</th>
							<td class="px-4 py-2">
								<div
									class="inline-flex items-center bg-primary-100 text-primary-800 text-xs font-medium px-2 py-0.5 rounded dark:bg-primary-900 dark:text-primary-300">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										class="h-3.5 w-3.5 mr-1"
										viewbox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true">
										<path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z" />
										<path
											fill-rule="evenodd"
											clip-rule="evenodd"
											d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" />
									</svg>
									Designer
								</div>
							</td>
							<td class="px-4 py-2"> nick@gmail.com </td>
							<td class="px-4 py-2 form-text-normal">
								<div class="flex items-center">
									<div class="w-3 h-3 mr-2 bg-green-500 border rounded-full"></div>
									Active
								</div>
							</td>
							<td class="px-4 py-2">Nov 11, 2022</td>
							<td class="px-4 py-2">Dec 11, 2024</td>
						</tr>
						<tr class="border-b border-gray-200 dark:border-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">
							<th scope="row" class="px-4 py-2 form-text-normal">
								<div class="flex items-center">
									<a href="team/1" class="hover:underline"> Mystique </a>
								</div>
							</th>
							<td class="px-4 py-2">
								<div
									class="inline-flex items-center bg-primary-100 text-primary-800 text-xs font-medium px-2 py-0.5 rounded dark:bg-primary-900 dark:text-primary-300">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										class="h-3.5 w-3.5 mr-1"
										viewbox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true">
										<path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z" />
										<path
											fill-rule="evenodd"
											clip-rule="evenodd"
											d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" />
									</svg>
									Manager
								</div>
							</td>
							<td class="px-4 py-2"> jennifer@gmail.com </td>

							<td class="px-4 py-2 form-text-normal">
								<div class="flex items-center">
									<div class="w-3 h-3 mr-2 bg-green-500 border rounded-full"></div>
									Active
								</div>
							</td>
							<td class="px-4 py-2">Nov 11, 2022</td>
							<td class="px-4 py-2">Dec 11, 2024</td>
						</tr>
					</tbody>
				</table>
			</div>
		</div>
	</div>
</section>
