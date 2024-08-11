<script>
	import NavBar from '$quick-learn/common/navbar/superadmin.svelte';
</script>

<NavBar />
<main>
	<div class="bg-gray-50 relative z-0 flex-1 overflow-x-scroll focus:outline-none h-screen">
		<div class="px-4 mb-8 sm:flex sm:items-center sm:justify-center sm:px-6 lg:px-8">
			<div class="items-baseline mt-8">
				<h1 class="text-5xl text-center font-extrabold leading-tight">HTML Course</h1>
				<p
					class="mt-1 ml-1 text-sm text-gray-500 truncate sm:flex sm:items-center sm:justify-center">
					Crownstack Technologies published this course on June 1, 2021
				</p>

				<p
					class="mt-1 ml-1 text-sm text-gray-500 truncate sm:flex sm:items-center sm:justify-center">
					(40 Lessons)
				</p>
				<div class="sm:flex sm:items-center sm:justify-center mt-2">
					<button
						data-tooltip-target="tooltip-edit"
						data-modal-target="defaultModal"
						data-modal-toggle="defaultModal"
						type="button"
						class="text-black bg-gray-300 hover:bg-blue-800 hover:text-white
						focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full text-sm
						p-2.5 text-center inline-flex items-center me-2 dark:bg-blue-600 dark:hover:bg-blue-700
						dark:focus:ring-blue-800">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="size-4">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M8.25 7.5V6.108c0-1.135.845-2.098 1.976-2.192.373-.03.748-.057 1.123-.08M15.75 18H18a2.25 2.25 0 0 0 2.25-2.25V6.108c0-1.135-.845-2.098-1.976-2.192a48.424 48.424 0 0 0-1.123-.08M15.75 18.75v-1.875a3.375 3.375 0 0 0-3.375-3.375h-1.5a1.125 1.125 0 0 1-1.125-1.125v-1.5A3.375 3.375 0 0 0 6.375 7.5H5.25m11.9-3.664A2.251 2.251 0 0 0 15 2.25h-1.5a2.251 2.251 0 0 0-2.15 1.586m5.8 0c.065.21.1.433.1.664v.75h-6V4.5c0-.231.035-.454.1-.664M6.75 7.5H4.875c-.621 0-1.125.504-1.125 1.125v12c0 .621.504 1.125 1.125 1.125h9.75c.621 0 1.125-.504 1.125-1.125V16.5a9 9 0 0 0-9-9Z" />
						</svg>

						<span class="sr-only">Icon description</span>
					</button>
					<div
						id="tooltip-edit"
						role="tooltip"
						class="absolute z-10 invisible inline-block px-3 py-2 text-sm font-medium text-white transition-opacity duration-300 bg-gray-900 rounded-lg shadow-sm opacity-0 tooltip dark:bg-gray-700">
						Copy Course
						<div class="tooltip-arrow" data-popper-arrow></div>
					</div>
				</div>
			</div>
		</div>

		<div class="relative px-6 grid gap-10 pb-16" id="release_notes">
			<div id="created-spaces">
				<ul
					role="list"
					class="grid grid-cols-2 gap-x-2 gap-y-4 sm:grid-cols-3 sm:gap-x-4 lg:grid-cols-6 2xl:grid-cols-8 xl:gap-x-6">
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/normal">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-56">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									First HTML Code
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<p class="text-xs text-gray-500 line-clamp-2 mt-4">Added on June 1, 2021</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/normal">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-56">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									First HTML Code
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<p class="text-xs text-gray-500 line-clamp-2 mt-4">Added on June 1, 2021</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/normal">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-56">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									Exploring the document
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<p class="text-xs text-gray-500 line-clamp-2 mt-4">Added on June 1, 2021</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/normal">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-56">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									Comments, White Space and line breaks
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<p class="text-xs text-gray-500 line-clamp-2 mt-4">Added on June 1, 2021</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/normal">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-56">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									The Rest of the HTML tags
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<p class="text-xs text-gray-500 line-clamp-2 mt-4">Added on June 1, 2021</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/normal">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-56">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									Inserting Pictures and Styling
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<p class="text-xs text-gray-500 line-clamp-2 mt-4">Added on June 1, 2021</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/normal">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-56">
								<h1 id="message-heading" class="font-medium text-gray-900">
									Inserting Pictures and Styling
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<p class="text-xs text-gray-500 line-clamp-2 mt-4">Added on June 1, 2021</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/normal">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-56">
								<h1 id="message-heading" class="font-medium text-gray-900">
									Inserting Pictures Via CSS
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<p class="text-xs text-gray-500 line-clamp-2 mt-4">Added on June 1, 2021</p>
							</div>
						</a>
					</li>
				</ul>
			</div>
		</div>
	</div>
</main>

<!-- Main modal -->
<form
	action="#"
	method="get"
	id="defaultModal"
	tabindex="-1"
	aria-hidden="true"
	class="fixed top-0 left-0 right-0 z-50 hidden w-full p-4 overflow-x-hidden overflow-y-auto md:inset-0 h-modal md:h-full justify-center items-center">
	<div class="relative w-full h-full max-w-4xl md:h-auto">
		<!-- Modal content -->
		<div class="relative bg-white rounded-lg shadow dark:bg-gray-800">
			<!-- Modal header -->
			<div class="flex items-start justify-between p-4 rounded-t">
				<h3 class="text-xl font-semibold text-gray-900 dark:text-gray-400">
					Copy course into Roadmap
				</h3>
				<button
					type="button"
					class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white"
					data-modal-toggle="defaultModal">
					<svg
						aria-hidden="true"
						class="w-5 h-5"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg">
						<path
							fill-rule="evenodd"
							d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
							clip-rule="evenodd"></path>
					</svg>
					<span class="sr-only">Close modal</span>
				</button>
			</div>
			<!-- Modal body -->
			<div class="px-4 md:px-6">
				<div class="mb-4 border-b border-gray-200 dark:border-gray-700">
					<ul
						class="flex flex-wrap -mb-px text-sm font-medium text-center"
						id="myTab"
						data-tabs-toggle="#myTabContent"
						role="tablist">
						<li class="mr-1" role="presentation">
							<span class="inline-block pb-2 pr-1 text-gray-700" id="brand-tab">
								Select Roadmaps
							</span>
						</li>
					</ul>
				</div>
				<div id="myTabContent">
					<div
						class="grid grid-cols-2 gap-4 md:grid-cols-3"
						id="brand"
						role="tabpanel"
						aria-labelledby="brand-tab">
						<div class="space-y-2">
							<h5 class="text-lg font-medium text-black dark:text-white">Engineering</h5>

							<div class="flex items-center">
								<input
									id="apple"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="apple"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Web Development Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="asus"
									type="checkbox"
									value=""
									checked
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label for="asus" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Backend Development Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="acer"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label for="acer" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Frontend Development Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="allview"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="allview"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Learning Clean Code Roadmap
								</label>
							</div>
						</div>

						<div class="space-y-2">
							<h5 class="text-lg font-medium text-black dark:text-white">HR</h5>

							<div class="flex items-center">
								<input
									id="beats"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="beats"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									HR Learning Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="bose"
									type="checkbox"
									value=""
									checked
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label for="bose" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Recruitment Learning Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="benq"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label for="benq" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Team Leadership Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="bosch"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="bosch"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Onboarding Learning Roadmap
								</label>
							</div>
						</div>

						<div class="space-y-2">
							<h5 class="text-lg font-medium text-black dark:text-white">Sales</h5>

							<div class="flex items-center">
								<input
									id="canon"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="canon"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Cold Calling Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="cisco"
									type="checkbox"
									value=""
									checked
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="cisco"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Account Nurturing Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="cowon"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="cowon"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Email Marketing Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="clevo"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="clevo"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Other Roadmap
								</label>
							</div>
						</div>
						<div class="space-y-2 mt-4">
							<h5 class="text-lg font-medium text-black dark:text-white">Engineering</h5>

							<div class="flex items-center">
								<input
									id="apple"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="apple"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Web Development Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="asus"
									type="checkbox"
									value=""
									checked
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label for="asus" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Backend Development Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="acer"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label for="acer" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Frontend Development Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="allview"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="allview"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Learning Clean Code Roadmap
								</label>
							</div>
						</div>

						<div class="space-y-2 mt-4">
							<h5 class="text-lg font-medium text-black dark:text-white">HR</h5>

							<div class="flex items-center">
								<input
									id="beats"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="beats"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									HR Learning Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="bose"
									type="checkbox"
									value=""
									checked
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label for="bose" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Recruitment Learning Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="benq"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label for="benq" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Team Leadership Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="bosch"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="bosch"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Onboarding Learning Roadmap
								</label>
							</div>
						</div>

						<div class="space-y-2 mt-4">
							<h5 class="text-lg font-medium text-black dark:text-white">Sales</h5>

							<div class="flex items-center">
								<input
									id="canon"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="canon"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Cold Calling Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="cisco"
									type="checkbox"
									value=""
									checked
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="cisco"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Account Nurturing Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="cowon"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="cowon"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Email Marketing Roadmap
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="clevo"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="clevo"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Other Roadmap
								</label>
							</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Modal footer -->
			<div class="flex items-center p-6 space-x-4 rounded-b dark:border-gray-600">
				<button
					data-modal-toggle="defaultModal"
					class="text-white bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:outline-none focus:ring-primary-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-primary-700 dark:hover:bg-primary-800 dark:focus:ring-primary-800">
					Copy Course
				</button>
				<button
					data-modal-toggle="defaultModal"
					class="py-2.5 px-5 text-sm font-medium text-gray-900 focus:outline-none bg-white rounded-lg border border-gray-200 hover:bg-gray-100 hover:text-primary-700 focus:z-10 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700">
					Cancel
				</button>
			</div>
		</div>
	</div>
</form>
