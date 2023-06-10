<script>
	import { goto } from '$app/navigation';
	import Fullnavbar from '$lib/tosupportme/fullnavbar.svelte';
	let menu = { opened: false, filter: false };

	function toggle() {
		menu.opened = !menu.opened;
	}

	function filter() {
		menu.filter = !menu.filter;
	}
</script>

<Fullnavbar />

<div class="flex h-full flex-col">
	<div class="md:flex md:items-center md:justify-between py-4 px-6">
		<div class="min-w-0 flex-1">
			<h2
				class="text-2xl font-bold leading-7 text-gray-900 sm:truncate sm:text-3xl sm:tracking-tight"
			>
				Change Logs
			</h2>
		</div>
		<div class="mt-4 flex md:mt-0 md:ml-4">
			<a href="/changelog/new">
				<button
					type="button"
					class="ml-3 inline-flex items-center rounded-md border border-transparent bg-indigo-600 px-4 py-2 text-sm font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2"
					>Add New</button
				>
			</a>
		</div>
	</div>
	<!-- Bottom section -->
	<div class="flex min-h-0 flex-1 overflow-hidden">
		<!-- Main area -->
		<main class="min-w-0 flex-1 border-t border-gray-200 xl:flex">
			<section
				aria-labelledby="message-heading"
				class="flex h-full min-w-0 flex-1 flex-col overflow-hidden xl:order-last"
			>
				<!-- Top section -->

				<div class="min-h-0 flex-1 overflow-y-auto">
					<div class="bg-white pt-5 pb-6 shadow border-b border-gray-200">
						<div class="px-4 sm:flex sm:items-baseline sm:justify-between sm:px-6 lg:px-8">
							<div class="sm:w-0 sm:flex-1">
								<div class="flex items-center">
									<h1 id="message-heading" class="text-lg font-medium text-gray-900">
										Added Feature number one
									</h1>
									<a href="/changelog/1">
										<svg
											xmlns="http://www.w3.org/2000/svg"
											fill="none"
											viewBox="0 0 24 24"
											stroke-width="1.5"
											stroke="currentColor"
											class="w-4 h-4 ml-2"
										>
											<path
												stroke-linecap="round"
												stroke-linejoin="round"
												d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
											/>
										</svg>
									</a>
								</div>
								<p class="mt-1 truncate text-sm text-gray-500">
									Created by Aashish Dhawan on October 12, 2022
								</p>
							</div>

							<div
								class="mt-4 flex items-center justify-between sm:mt-0 sm:ml-6 sm:flex-shrink-0 sm:justify-start"
							>
								<p class="flex-shrink-0 whitespace-nowrap text-sm text-gray-500 mr-2">
									Version 3.0.5
								</p>

								<span
									class="inline-flex items-center rounded-full bg-green-100 px-3 py-0.5 text-sm font-medium text-green-800"
									>Published</span
								>
								<div class="relative ml-3 inline-block text-left">
									<div>
										<button
											on:click={toggle}
											type="button"
											class="-my-2 flex items-center rounded-full bg-white p-2 text-gray-400 hover:text-gray-600 focus:outline-none focus:ring-2 focus:ring-blue-600"
											id="menu-3-button"
											aria-expanded="false"
											aria-haspopup="true"
										>
											<span class="sr-only">Open options</span>
											<svg
												class="h-5 w-5"
												viewBox="0 0 20 20"
												fill="currentColor"
												aria-hidden="true"
											>
												<path
													d="M10 3a1.5 1.5 0 110 3 1.5 1.5 0 010-3zM10 8.5a1.5 1.5 0 110 3 1.5 1.5 0 010-3zM11.5 15.5a1.5 1.5 0 10-3 0 1.5 1.5 0 003 0z"
												/>
											</svg>
										</button>
									</div>

									<!--
                      Dropdown menu, show/hide based on menu state.
  
                      Entering: "transition ease-out duration-100"
                        From: "transform opacity-0 scale-95"
                        To: "transform opacity-100 scale-100"
                      Leaving: "transition ease-in duration-75"
                        From: "transform opacity-100 scale-100"
                        To: "transform opacity-0 scale-95"
                    -->
									{#if menu.opened}
										<div
											class="absolute right-0 z-10 mt-2 w-32 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
											role="menu"
											aria-orientation="vertical"
											aria-labelledby="menu-3-button"
											tabindex="-1"
										>
											<div class="py-1" role="none">
												<!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
												<a
													href="#"
													class="text-gray-700 flex justify-between px-4 py-2 text-sm hover:bg-gray-50"
													role="menuitem"
													tabindex="-1"
													id="menu-3-item-1"
												>
													<span>Edit</span>
												</a>

												<a
													href="#"
													class="text-gray-700 flex justify-between px-4 py-2 text-sm hover:bg-gray-50"
													role="menuitem"
													tabindex="-1"
													id="menu-3-item-2"
												>
													<span>Delete</span>
												</a>
											</div>
										</div>
									{/if}
								</div>
							</div>
						</div>
					</div>
					<!-- Thread section-->
					<ul role="list" class="space-y-2 bg-gray-50 h-screen py-4 sm:space-y-4 sm:px-6 lg:px-8">
						<li class="bg-white px-4 py-6 shadow sm:rounded-lg sm:px-6">
							<span
								class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800"
								>Improvements</span
							>
							<span
								class="inline-flex items-center rounded bg-red-100 px-2 py-0.5 text-xs font-medium text-red-800"
								>Bug Fixes</span
							>
							<span
								class="inline-flex items-center rounded bg-green-100 px-2 py-0.5 text-xs font-medium text-green-800"
								>New</span
							>
							<span
								class="inline-flex items-center rounded bg-yellow-100 px-2 py-0.5 text-xs font-medium text-yellow-800"
								>Refactor</span
							>
							<span
								class="inline-flex items-center rounded bg-blue-100 px-2 py-0.5 text-xs font-medium text-blue-800"
								>Maintainence</span
							>

							<div class=" space-y-6 text-sm text-gray-800 mt-4">
								<p>This is rich text description of release notes</p>

								<p>
									Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita, hic? Commodi
									cumque similique id tempora molestiae deserunt at suscipit, dolor voluptatem,
									numquam, harum consequatur laboriosam voluptas tempore aut voluptatum alias?
								</p>
								<ul role="list">
									<li>
										Tempor ultrices proin nunc fames nunc ut auctor vitae sed. Eget massa parturient
										vulputate fermentum id facilisis nam pharetra. Aliquet leo tellus.
									</li>
									<li>Turpis ac nunc adipiscing adipiscing metus tincidunt senectus tellus.</li>
									<li>
										Semper interdum porta sit tincidunt. Dui suspendisse scelerisque amet metus eget
										sed. Ut tellus in sed dignissim.
									</li>
								</ul>
							</div>
						</li>
						<li class="bg-white px-4 py-6 shadow sm:rounded-lg sm:px-6">
							<div class="sm:flex sm:items-baseline sm:justify-between">
								<h3 class="text-base font-medium">
									<span class="text-gray-900">Release Tags</span>
								</h3>
							</div>
							<div class="space-y-2 text-sm text-gray-800">
								<span
									class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800"
									>iOS</span
								>
								<span
									class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800"
									>Android</span
								>
								<span
									class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800"
									>Web</span
								>
							</div>
						</li>

						<div class="rounded-md bg-green-50 p-4 shadow-sm shadow-green">
							<div class="flex">
								<div class="flex-shrink-0">
									<svg
										class="h-5 w-5 text-green-400"
										viewBox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true"
									>
										<path
											fill-rule="evenodd"
											d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a.75.75 0 000 1.5h.253a.25.25 0 01.244.304l-.459 2.066A1.75 1.75 0 0010.747 15H11a.75.75 0 000-1.5h-.253a.25.25 0 01-.244-.304l.459-2.066A1.75 1.75 0 009.253 9H9z"
											clip-rule="evenodd"
										/>
									</svg>
								</div>
								<div class="ml-3 flex-1 md:flex md:justify-between">
									<p class="text-sm text-green-700">
										Aashish Dhawan published this changelog on October 12, 2022
									</p>
									<p class="mt-3 text-sm md:mt-0 md:ml-6">
										<a
											href="#"
											class="whitespace-nowrap font-medium text-green-700 hover:text-green-600"
										>
											See Details
											<span aria-hidden="true"> &rarr;</span>
										</a>
									</p>
								</div>
							</div>
						</div>

						<div class="rounded-md bg-yellow-50 p-4 shadow-sm shadow-yellow">
							<div class="flex">
								<div class="flex-shrink-0">
									<svg
										class="h-5 w-5 text-yellow-400"
										viewBox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true"
									>
										<path
											fill-rule="evenodd"
											d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a.75.75 0 000 1.5h.253a.25.25 0 01.244.304l-.459 2.066A1.75 1.75 0 0010.747 15H11a.75.75 0 000-1.5h-.253a.25.25 0 01-.244-.304l.459-2.066A1.75 1.75 0 009.253 9H9z"
											clip-rule="evenodd"
										/>
									</svg>
								</div>
								<div class="ml-3 flex-1 md:flex md:justify-between">
									<p class="text-sm text-yellow-700">
										Aashish Dhawan created this draft on October 12, 2022
									</p>
									<p class="mt-3 text-sm md:mt-0 md:ml-6">
										<a
											href="#"
											class="whitespace-nowrap font-medium text-yellow-700 hover:text-yellow-600"
										>
											Continue Editing
											<span aria-hidden="true"> &rarr;</span>
										</a>
									</p>
								</div>
							</div>
						</div>

						<div class="rounded-md bg-gray-100 p-4 shadow-sm shadow-gray">
							<div class="flex">
								<div class="flex-shrink-0">
									<svg
										class="h-5 w-5 text-gray-400"
										viewBox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true"
									>
										<path
											fill-rule="evenodd"
											d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a.75.75 0 000 1.5h.253a.25.25 0 01.244.304l-.459 2.066A1.75 1.75 0 0010.747 15H11a.75.75 0 000-1.5h-.253a.25.25 0 01-.244-.304l.459-2.066A1.75 1.75 0 009.253 9H9z"
											clip-rule="evenodd"
										/>
									</svg>
								</div>
								<div class="ml-3 flex-1 md:flex md:justify-between">
									<p class="text-sm text-gray-700">
										Aashish Dhawan scheduled this changelog to be published on October 12, 2022
									</p>
									<p class="mt-3 text-sm md:mt-0 md:ml-6">
										<a
											href="#"
											class="whitespace-nowrap font-medium text-gray-700 hover:text-gray-600"
										>
											Publish Now
											<span aria-hidden="true"> &rarr;</span>
										</a>
									</p>
								</div>
							</div>
						</div>

						<div class="rounded-md bg-red-100 p-4 shadow-sm shadow-red">
							<div class="flex">
								<div class="flex-shrink-0">
									<svg
										class="h-5 w-5 text-red-400"
										viewBox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true"
									>
										<path
											fill-rule="evenodd"
											d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a.75.75 0 000 1.5h.253a.25.25 0 01.244.304l-.459 2.066A1.75 1.75 0 0010.747 15H11a.75.75 0 000-1.5h-.253a.25.25 0 01-.244-.304l.459-2.066A1.75 1.75 0 009.253 9H9z"
											clip-rule="evenodd"
										/>
									</svg>
								</div>
								<div class="ml-3 flex-1 md:flex md:justify-between">
									<p class="text-sm text-red-700">
										Aashish Dhawan archived this changelog on October 12, 2022
									</p>
									<p class="mt-3 text-sm md:mt-0 md:ml-6">
										<a
											href="#"
											class="whitespace-nowrap font-medium text-red-700 hover:text-red-600"
										>
											Unarchive
											<span aria-hidden="true"> &rarr;</span>
										</a>
									</p>
								</div>
							</div>
						</div>
					</ul>
				</div>
			</section>

			<!-- Message list-->
			<aside class="hidden xl:order-first xl:block xl:flex-shrink-0">
				<div class="relative flex h-full w-96 flex-col border-r border-gray-200 bg-gray-100">
					<div class="flex-shrink-0">
						<div
							class="flex border-b border-gray-200 bg-gray-50 px-6 py-2 text-sm font-medium text-gray-500"
						>
							<span class="w-full">Change Logs</span>
							<div class="relative inline-block text-left">
								<button
									on:click={filter}
									type="submit"
									class="inline-flex justify-center rounded-md border border-gray-300 bg-white px-2 py-1 text-sm font-medium text-gray-700 shadow-sm hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2"
								>
									<svg
										class="h-3 w-3 text-gray-400"
										viewBox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true"
									>
										<path
											fill-rule="evenodd"
											d="M2.628 1.601C5.028 1.206 7.49 1 10 1s4.973.206 7.372.601a.75.75 0 01.628.74v2.288a2.25 2.25 0 01-.659 1.59l-4.682 4.683a2.25 2.25 0 00-.659 1.59v3.037c0 .684-.31 1.33-.844 1.757l-1.937 1.55A.75.75 0 018 18.25v-5.757a2.25 2.25 0 00-.659-1.591L2.659 6.22A2.25 2.25 0 012 4.629V2.34a.75.75 0 01.628-.74z"
											clip-rule="evenodd"
										/>
									</svg>
								</button>
								{#if menu.filter}
									<div
										class="absolute right-0 z-10 mt-2 w-48 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
										role="menu"
										aria-orientation="vertical"
										aria-labelledby="menu-button"
										tabindex="-1"
									>
										<div class="px-4 py-2 border-b border-gray-100" role="none">
											<p class="text-sm" role="none">Filter by Status</p>
										</div>
										<div class="py-1" role="none">
											<!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
											<a
												href="#"
												class="text-gray-700 flex justify-left px-4 py-2 text-sm hover:bg-gray-50"
												role="menuitem"
												tabindex="-1"
												id="menu-3-item-1"
											>
												<span
													class="inline-block h-2 w-2 mt-1.5 mr-2 flex-shrink-0 rounded-full bg-green-400"
													aria-hidden="true"
												/>

												<span>Published</span>
											</a>
											<a
												href="#"
												class="text-gray-700 flex justify-left px-4 py-2 text-sm  hover:bg-gray-50"
												role="menuitem"
												tabindex="-1"
												id="menu-3-item-2"
											>
												<span
													class="inline-block h-2 w-2 mt-1.5 mr-2 flex-shrink-0 rounded-full bg-yellow-400"
													aria-hidden="true"
												/>

												<span>Drafts</span>
											</a>
											<a
												href="#"
												class="text-gray-700 flex justify-left px-4 py-2 text-sm  hover:bg-gray-50"
												role="menuitem"
												tabindex="-1"
												id="menu-3-item-2"
											>
												<span
													class="inline-block h-2 w-2 mt-1.5 mr-2 flex-shrink-0 rounded-full bg-red-400"
													aria-hidden="true"
												/>

												<span>Archived</span>
											</a>
											<a
												href="#"
												class="text-gray-700 flex justify-left px-4 py-2 text-sm  hover:bg-gray-50"
												role="menuitem"
												tabindex="-1"
												id="menu-3-item-2"
											>
												<span
													class="inline-block h-2 w-2 mt-1.5 mr-2 flex-shrink-0 rounded-full bg-gray-400"
													aria-hidden="true"
												/>

												<span>Scheduled</span>
											</a>
											<div class="px-4 py-2 border-t border-gray-100  hover:bg-gray-50" role="none">
												<button
													type="submit"
													class="text-gray-700 block w-full py-1 text-left text-sm"
													role="menuitem"
													tabindex="-1"
													id="menu-item-3">Clear Filter</button
												>
											</div>
										</div>
									</div>
								{/if}
							</div>
						</div>
					</div>
					<nav aria-label="Message list" class="min-h-0 flex-1 overflow-y-auto">
						<ul role="list" class="divide-y divide-gray-200 border-b border-gray-200">
							<li
								class="relative bg-gray-50 py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50"
							>
								<div class="flex justify-between space-x-3">
									<div class="min-w-0 flex-1">
										<a href="#" class="block focus:outline-none">
											<span class="absolute inset-0" aria-hidden="true" />
											<p class="truncate text-sm font-medium text-gray-900">
												Added feature Number one
											</p>
											<p class="truncate text-sm text-gray-500">
												Aashish Dhawan on October 12, 2022
											</p>
										</a>
									</div>

									<p class="flex-shrink-0 whitespace-nowrap text-sm text-gray-500">3.0.5</p>
								</div>
								<div class="mt-1">
									<p class="text-sm text-gray-600 line-clamp-2">
										Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum cere.
										Enim rerum ....
									</p>
								</div>
								<span
									class="inline-flex items-center rounded-full bg-green-100 px-2.5 py-0.5 text-xs font-medium text-green-800"
									>Published</span
								>
							</li>

							<li
								class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50"
							>
								<div class="flex justify-between space-x-3">
									<div class="min-w-0 flex-1">
										<a href="#" class="block focus:outline-none">
											<span class="absolute inset-0" aria-hidden="true" />
											<p class="truncate text-sm font-medium text-gray-900">This is a Draft</p>
											<p class="truncate text-sm text-gray-500">
												Nemo mollitia repudiandae adipisci explicabo optio consequatur tempora ut
												nihil
											</p>
										</a>
									</div>
									<p class="flex-shrink-0 whitespace-nowrap text-sm text-gray-500">3.0.4</p>
								</div>
								<div class="mt-1">
									<p class="text-sm text-gray-600 line-clamp-2">
										Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum cere.
										Enim rerum ....
									</p>
								</div>
								<span
									class="inline-flex items-center rounded-full bg-yellow-100 px-2.5 py-0.5 text-xs font-medium text-yellow-800"
									>Draft</span
								>
							</li>

							<li
								class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50"
							>
								<div class="flex justify-between space-x-3">
									<div class="min-w-0 flex-1">
										<a href="#" class="block focus:outline-none">
											<span class="absolute inset-0" aria-hidden="true" />
											<p class="truncate text-sm font-medium text-gray-900">Kyle Gulgowski</p>
											<p class="truncate text-sm text-gray-500">
												Doloremque reprehenderit et harum quas explicabo nulla architecto dicta
												voluptatibus
											</p>
										</a>
									</div>
									<p class="flex-shrink-0 whitespace-nowrap text-sm text-gray-500">3.0.3</p>
								</div>
								<div class="mt-1">
									<p class="text-sm text-gray-600 line-clamp-2">
										Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum cere.
										Enim rerum ....
									</p>
								</div>
								<span
									class="inline-flex items-center rounded-full bg-red-100 px-2.5 py-0.5 text-xs font-medium text-red-800"
									>Archived</span
								>
							</li>

							<li
								class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50"
							>
								<div class="flex justify-between space-x-3">
									<div class="min-w-0 flex-1">
										<a href="#" class="block focus:outline-none">
											<span class="absolute inset-0" aria-hidden="true" />
											<p class="truncate text-sm font-medium text-gray-900">Hattie Haag</p>
											<p class="truncate text-sm text-gray-500">Eos sequi et aut ex impedit</p>
										</a>
									</div>
									<p class="flex-shrink-0 whitespace-nowrap text-sm text-gray-500">3.0.2</p>
								</div>
								<div class="mt-1">
									<p class="text-sm text-gray-600 line-clamp-2">
										Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum cere.
										Enim rerum ....
									</p>
								</div>
								<span
									class="inline-flex items-center rounded-full bg-gray-100 px-2.5 py-0.5 text-xs font-medium text-gray-800"
									>Scheduled</span
								>
							</li>

							<li
								class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50"
							>
								<div class="flex justify-between space-x-3">
									<div class="min-w-0 flex-1">
										<a href="#" class="block focus:outline-none">
											<span class="absolute inset-0" aria-hidden="true" />
											<p class="truncate text-sm font-medium text-gray-900">Wilma Glover</p>
											<p class="truncate text-sm text-gray-500">Quisquam veniam explicabo</p>
										</a>
									</div>
								</div>
								<div class="mt-1">
									<p class="text-sm text-gray-600 line-clamp-2">
										Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum cere.
										Enim rerum ....
									</p>
								</div>
							</li>

							<li
								class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50"
							>
								<div class="flex justify-between space-x-3">
									<div class="min-w-0 flex-1">
										<a href="#" class="block focus:outline-none">
											<span class="absolute inset-0" aria-hidden="true" />
											<p class="truncate text-sm font-medium text-gray-900">Dolores Morissette</p>
											<p class="truncate text-sm text-gray-500">
												Est ratione molestiae modi maiores consequatur eligendi et excepturi magni
											</p>
										</a>
									</div>
								</div>
								<div class="mt-1">
									<p class="text-sm text-gray-600 line-clamp-2">
										Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum cere.
										Enim rerum ....
									</p>
								</div>
							</li>

							<li
								class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50"
							>
								<div class="flex justify-between space-x-3">
									<div class="min-w-0 flex-1">
										<a href="#" class="block focus:outline-none">
											<span class="absolute inset-0" aria-hidden="true" />
											<p class="truncate text-sm font-medium text-gray-900">Guadalupe Walsh</p>
											<p class="truncate text-sm text-gray-500">
												Commodi deserunt aut veniam rem ipsam
											</p>
										</a>
									</div>
								</div>
								<div class="mt-1">
									<p class="text-sm text-gray-600 line-clamp-2">
										Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum cere.
										Enim rerum ....
									</p>
								</div>
							</li>

							<li
								class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50"
							>
								<div class="flex justify-between space-x-3">
									<div class="min-w-0 flex-1">
										<a href="#" class="block focus:outline-none">
											<span class="absolute inset-0" aria-hidden="true" />
											<p class="truncate text-sm font-medium text-gray-900">Jasmine Hansen</p>
											<p class="truncate text-sm text-gray-500">Illo illum aut debitis earum</p>
										</a>
									</div>
								</div>
								<div class="mt-1">
									<p class="text-sm text-gray-600 line-clamp-2">
										Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum cere.
										Enim rerum ....
									</p>
								</div>
							</li>

							<li
								class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50"
							>
								<div class="flex justify-between space-x-3">
									<div class="min-w-0 flex-1">
										<a href="#" class="block focus:outline-none">
											<span class="absolute inset-0" aria-hidden="true" />
											<p class="truncate text-sm font-medium text-gray-900">Ian Volkman</p>
											<p class="truncate text-sm text-gray-500">
												Qui dolore iste ut est cumque sed
											</p>
										</a>
									</div>
								</div>
								<div class="mt-1">
									<p class="text-sm text-gray-600 line-clamp-2">
										Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum cere.
										Enim rerum ....
									</p>
								</div>
							</li>

							<li
								class="relative bg-white py-5 px-6 focus-within:ring-2 focus-within:ring-inset focus-within:ring-blue-600 hover:bg-gray-50"
							>
								<div class="flex justify-between space-x-3">
									<div class="min-w-0 flex-1">
										<a href="#" class="block focus:outline-none">
											<span class="absolute inset-0" aria-hidden="true" />
											<p class="truncate text-sm font-medium text-gray-900">Rafael Klocko</p>
											<p class="truncate text-sm text-gray-500">
												Aut sed aut illum delectus maiores laboriosam ex
											</p>
										</a>
									</div>
								</div>
								<div class="mt-1">
									<p class="text-sm text-gray-600 line-clamp-2">
										Doloremque dolorem maiores assumenda dolorem facilis. Velit vel in a rerum cere.
										Enim rerum ....
									</p>
								</div>
							</li>
						</ul>
					</nav>
				</div>
			</aside>
		</main>
	</div>
</div>
