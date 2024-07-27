<script>
	import NavBar from '$quick-learn/common/navbar/admin.svelte';
</script>

<NavBar />
<main>
	<div class="bg-gray-50 relative z-0 flex-1 overflow-x-scroll focus:outline-none h-screen">
		<div class="px-4 py-4 sm:flex sm:items-center sm:justify-center sm:px-6 lg:px-8">
			<nav class="flex" aria-label="Breadcrumb">
				<ol class="inline-flex justify-self-center space-x-1 md:space-x-2 rtl:space-x-reverse">
					<li class="inline-flex items-center">
						<a
							href="/quick-learn/content"
							class="inline-flex items-center text-sm font-medium text-gray-700 hover:text-blue-600 dark:text-gray-400 dark:hover:text-white hover:underline">
							<svg
								class="w-3 h-3 me-2.5"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								fill="currentColor"
								viewBox="0 0 20 20">
								<path
									d="m19.707 9.293-2-2-7-7a1 1 0 0 0-1.414 0l-7 7-2 2a1 1 0 0 0 1.414 1.414L2 10.414V18a2 2 0 0 0 2 2h3a1 1 0 0 0 1-1v-4a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v4a1 1 0 0 0 1 1h3a2 2 0 0 0 2-2v-7.586l.293.293a1 1 0 0 0 1.414-1.414Z" />
							</svg>
							Content Repository
						</a>
					</li>
					<li>
						<div class="flex items-center">
							<svg
								class="rtl:rotate-180 w-3 h-3 text-gray-400 mx-1"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 6 10">
								<path
									stroke="currentColor"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="m1 9 4-4-4-4" />
							</svg>
							<a
								href="/quick-learn/content/roadmap"
								class="ms-1 text-sm font-medium text-gray-700 hover:text-blue-600 md:ms-2 dark:text-gray-400 dark:hover:text-white hover:underline"
								>Web Development Roadmap</a>
						</div>
					</li>
				</ol>
			</nav>
		</div>
		<div class="px-4 mb-8 sm:flex sm:items-center sm:justify-center sm:px-6 lg:px-8">
			<div class="items-baseline">
				<h1 class="text-5xl font-extrabold leading-tight">Web Developement Roadmap</h1>
				<p
					class="mt-1 ml-1 text-sm text-gray-500 truncate sm:flex sm:items-center sm:justify-center">
					Aashish Dhawan created this roadmap on June 1, 2021
				</p>

				<p
					class="mt-1 ml-1 text-sm text-gray-500 truncate sm:flex sm:items-center sm:justify-center">
					(20 Courses, 40 Lessons, 121 participants)
				</p>
				<div class="sm:flex sm:items-center sm:justify-center mt-2">
					<button
						data-tooltip-target="tooltip-edit"
						data-modal-target="editRoadmapModal"
						data-modal-toggle="editRoadmapModal"
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
								d="m16.862 4.487 1.687-1.688a1.875 1.875 0 1 1 2.652 2.652L6.832 19.82a4.5 4.5 0 0 1-1.897 1.13l-2.685.8.8-2.685a4.5 4.5 0 0 1 1.13-1.897L16.863 4.487Zm0 0L19.5 7.125" />
						</svg>

						<span class="sr-only">Icon description</span>
					</button>
					<div
						id="tooltip-edit"
						role="tooltip"
						class="absolute z-10 invisible inline-block px-3 py-2 text-sm font-medium text-white transition-opacity duration-300 bg-gray-900 rounded-lg shadow-sm opacity-0 tooltip dark:bg-gray-700">
						Edit Roadmap
						<div class="tooltip-arrow" data-popper-arrow></div>
					</div>
					<button
						data-tooltip-target="tooltip-move"
						data-modal-target="move-course-modal"
						data-modal-toggle="move-course-modal"
						type="button"
						class="text-black bg-gray-300 hover:bg-red-800 hover:text-white focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full text-sm p-2.5 text-center inline-flex items-center me-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
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
								d="M8.25 9V5.25A2.25 2.25 0 0 1 10.5 3h6a2.25 2.25 0 0 1 2.25 2.25v13.5A2.25 2.25 0 0 1 16.5 21h-6a2.25 2.25 0 0 1-2.25-2.25V15M12 9l3 3m0 0-3 3m3-3H2.25" />
						</svg>

						<span class="sr-only">Icon description</span>
					</button>
					<div
						id="tooltip-move"
						role="tooltip"
						class="absolute z-10 invisible inline-block px-3 py-2 text-sm font-medium text-white transition-opacity duration-300 bg-gray-900 rounded-lg shadow-sm opacity-0 tooltip dark:bg-gray-700">
						Add already existing courses to this roadmap
						<div class="tooltip-arrow" data-popper-arrow></div>
					</div>

					<button
						data-tooltip-target="tooltip-delete"
						data-modal-target="delete-roadmap-modal"
						data-modal-toggle="delete-roadmap-modal"
						type="button"
						class="text-black bg-gray-300 hover:bg-red-800 hover:text-white focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full text-sm p-2.5 text-center inline-flex items-center me-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="size-4">
							<path
								stroke="currentColor"
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M5 7h14m-9 3v8m4-8v8M10 3h4a1 1 0 0 1 1 1v3H9V4a1 1 0 0 1 1-1ZM6 7h12v13a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1V7Z" />
						</svg>

						<span class="sr-only">Icon description</span>
					</button>
					<div
						id="tooltip-delete"
						role="tooltip"
						class="absolute z-10 invisible inline-block px-3 py-2 text-sm font-medium text-white transition-opacity duration-300 bg-gray-900 rounded-lg shadow-sm opacity-0 tooltip dark:bg-gray-700">
						Archive Roadmap
						<div class="tooltip-arrow" data-popper-arrow></div>
					</div>
					<button
						data-tooltip-target="tooltip-settings"
						type="button"
						class="text-black bg-gray-300 hover:bg-blue-800 hover:text-white focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full text-sm p-2.5 text-center inline-flex items-center me-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
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
								d="M9.594 3.94c.09-.542.56-.94 1.11-.94h2.593c.55 0 1.02.398 1.11.94l.213 1.281c.063.374.313.686.645.87.074.04.147.083.22.127.325.196.72.257 1.075.124l1.217-.456a1.125 1.125 0 0 1 1.37.49l1.296 2.247a1.125 1.125 0 0 1-.26 1.431l-1.003.827c-.293.241-.438.613-.43.992a7.723 7.723 0 0 1 0 .255c-.008.378.137.75.43.991l1.004.827c.424.35.534.955.26 1.43l-1.298 2.247a1.125 1.125 0 0 1-1.369.491l-1.217-.456c-.355-.133-.75-.072-1.076.124a6.47 6.47 0 0 1-.22.128c-.331.183-.581.495-.644.869l-.213 1.281c-.09.543-.56.94-1.11.94h-2.594c-.55 0-1.019-.398-1.11-.94l-.213-1.281c-.062-.374-.312-.686-.644-.87a6.52 6.52 0 0 1-.22-.127c-.325-.196-.72-.257-1.076-.124l-1.217.456a1.125 1.125 0 0 1-1.369-.49l-1.297-2.247a1.125 1.125 0 0 1 .26-1.431l1.004-.827c.292-.24.437-.613.43-.991a6.932 6.932 0 0 1 0-.255c.007-.38-.138-.751-.43-.992l-1.004-.827a1.125 1.125 0 0 1-.26-1.43l1.297-2.247a1.125 1.125 0 0 1 1.37-.491l1.216.456c.356.133.751.072 1.076-.124.072-.044.146-.086.22-.128.332-.183.582-.495.644-.869l.214-1.28Z" />
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M15 12a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" />
						</svg>

						<span class="sr-only">Icon description</span>
					</button>
					<div
						id="tooltip-settings"
						role="tooltip"
						class="absolute z-10 invisible inline-block px-3 py-2 text-sm font-medium text-white transition-opacity duration-300 bg-gray-900 rounded-lg shadow-sm opacity-0 tooltip dark:bg-gray-700">
						Roadmap Settings
						<div class="tooltip-arrow" data-popper-arrow></div>
					</div>
				</div>
			</div>
		</div>

		<div class="relative px-6 grid gap-10 pb-16" id="release_notes">
			<div id="created-spaces">
				<ul
					role="list"
					class="grid grid-cols-2 gap-x-4 gap-y-8 sm:grid-cols-3 sm:gap-x-6 lg:grid-cols-4 2xl:grid-cols-5 xl:gap-x-8">
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group content-center"
						id="space_8">
						<div
							class="cursor-pointer"
							data-modal-target="defaultModal"
							data-modal-toggle="defaultModal">
							<div class="text-center content-center">
								<svg
									class="mx-auto h-12 w-12 text-indigo-400"
									fill="none"
									viewBox="0 0 24 24"
									stroke="currentColor"
									aria-hidden="true">
									<path
										vector-effect="non-scaling-stroke"
										stroke-linecap="round"
										stroke-linejoin="round"
										stroke-width="2"
										d="M9 13h6m-3-3v6m-9 1V7a2 2 0 012-2h6l2 2h6a2 2 0 012 2v8a2 2 0 01-2 2H5a2 2 0 01-2-2z" />
								</svg>
								<h3 class="mt-2 text-sm font-semibold text-gray-900">Create New Course</h3>
							</div>
						</div>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/roadmap/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Git Baisc Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn Git basics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/roadmap/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									HTML Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn HTML basics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/roadmap/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									TailwindCSS Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn TailwindCSS basics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/roadmap/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Email Etiquette Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn etiquette basics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/roadmap/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Accelerate Book Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn Accelerate book topics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/roadmap/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Hire Smart Book Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn Hiring Smart book topics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
				</ul>
			</div>
		</div>
	</div>
</main>

<!-- Add Course modal -->
<div
	id="defaultModal"
	tabindex="-1"
	aria-hidden="true"
	class="hidden overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-modal md:h-full">
	<div class="relative p-4 w-full max-w-2xl h-full md:h-auto">
		<!-- Modal content -->
		<div class="relative p-4 bg-white rounded-lg shadow dark:bg-gray-800 sm:p-5">
			<!-- Modal header -->
			<div
				class="flex justify-between items-center pb-4 mb-4 rounded-t border-b sm:mb-5 dark:border-gray-600">
				<h3 class="text-lg font-semibold text-gray-900 dark:text-white">Create New Course</h3>
				<button
					type="button"
					class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white"
					data-modal-toggle="defaultModal">
					<svg
						aria-hidden="true"
						class="w-5 h-5"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
							clip-rule="evenodd"></path
						></svg>
					<span class="sr-only">Close modal</span>
				</button>
			</div>
			<!-- Modal body -->
			<form action="#">
				<div class="grid gap-4 mb-4 sm:grid-cols-1">
					<div class="sm:col-span-2">
						<label for="name" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
							>Name</label>
						<input
							type="text"
							name="name"
							id="name"
							class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
							placeholder="Type course name"
							required="" />
					</div>
					<div class="sm:col-span-2">
						<label
							for="category"
							class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
							>Course Category</label>
						<select
							id="category"
							class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500">
							<option selected="">Select category</option>
							<option value="TV">Software Application</option>
							<option value="PC">Production Deployment process</option>
							<option value="GA">Recruitment Process</option>
							<option value="PH">Book</option>
						</select>
					</div>
					<div class="sm:col-span-2">
						<label
							for="description"
							class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
							>Description</label>
						<textarea
							id="description"
							rows="4"
							class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
							placeholder="Write course description here"></textarea>
					</div>
					<div class="mb-4 space-y-4 sm:flex sm:space-y-0">
						<div class="flex">
							<div class="flex items-center h-5">
								<input
									id="helper-checkbox"
									aria-describedby="helper-checkbox-text"
									type="checkbox"
									value=""
									class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />
							</div>
							<div class="ms-2 text-sm">
								<label for="helper-checkbox" class="font-medium text-gray-900 dark:text-gray-300"
									>Make this course public and available for community.</label>
								<p
									id="helper-checkbox-text"
									class="text-xs font-normal text-gray-400 dark:text-gray-300">
									If checked, this will make this course available to all organizations and their
									users. If unchecked, only your organization users will be able to access this
									course. Please do this carefully and never make any confidential course public.
								</p>
							</div>
						</div>
					</div>
				</div>
				<button
					type="submit"
					class="text-white inline-flex items-center bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:outline-none focus:ring-primary-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800">
					Create New Course
				</button>
				<button
					data-modal-toggle="defaultModal"
					class="py-2.5 px-5 ml-2 text-sm font-medium text-gray-900 focus:outline-none bg-white rounded-lg border border-gray-200 hover:bg-gray-100 hover:text-primary-700 focus:z-10 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700">
					Cancel
				</button>
			</form>
		</div>
	</div>
</div>

<!-- Edit Roadmap modal -->
<div
	id="editRoadmapModal"
	tabindex="-1"
	aria-hidden="true"
	class="hidden overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-modal md:h-full">
	<div class="relative p-4 w-full max-w-2xl h-full md:h-auto">
		<!-- Modal content -->
		<div class="relative p-4 bg-white rounded-lg shadow dark:bg-gray-800 sm:p-5">
			<!-- Modal header -->
			<div
				class="flex justify-between items-center pb-4 mb-4 rounded-t border-b sm:mb-5 dark:border-gray-600">
				<h3 class="text-lg font-semibold text-gray-900 dark:text-white">Edit Roadmap</h3>
				<button
					type="button"
					class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white"
					data-modal-toggle="editRoadmapModal">
					<svg
						aria-hidden="true"
						class="w-5 h-5"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
							clip-rule="evenodd"></path
						></svg>
					<span class="sr-only">Close modal</span>
				</button>
			</div>
			<!-- Modal body -->
			<form action="#">
				<div class="grid gap-4 mb-4 sm:grid-cols-1">
					<div class="sm:col-span-2">
						<label for="name" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
							>Name</label>
						<input
							type="text"
							name="name"
							id="name"
							class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
							value="Web Development Roadmap"
							required="" />
					</div>
					<div class="sm:col-span-2">
						<label
							for="category"
							class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
							>Roadmap Category</label>
						<select
							id="category"
							class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500">
							<option selected="TV">Select category</option>
							<option value="TV">HR</option>
							<option value="PC">Sales</option>
							<option value="GA">Engineering</option>
							<option value="PH">Recruitment</option>
						</select>
					</div>
					<div class="sm:col-span-2">
						<label
							for="description"
							class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
							>Description</label>
						<textarea
							id="description"
							rows="4"
							class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
							placeholder="Write roadmap description here"></textarea>
					</div>
				</div>
				<button
					type="submit"
					class="text-white inline-flex items-center bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:outline-none focus:ring-primary-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800">
					Edit Roadmap
				</button>
				<button
					data-modal-toggle="editRoadmapModal"
					class="py-2.5 px-5 ml-2 text-sm font-medium text-gray-900 focus:outline-none bg-white rounded-lg border border-gray-200 hover:bg-gray-100 hover:text-primary-700 focus:z-10 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700">
					Cancel
				</button>
			</form>
		</div>
	</div>
</div>

<!-- Delete Roadmap modal -->
<div
	id="delete-roadmap-modal"
	tabindex="-1"
	class="hidden overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-[calc(100%-1rem)] max-h-full">
	<div class="relative p-4 w-full max-w-md max-h-full">
		<div class="relative bg-white rounded-lg shadow dark:bg-gray-700">
			<button
				type="button"
				class="absolute top-3 end-2.5 text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm w-8 h-8 ms-auto inline-flex justify-center items-center dark:hover:bg-gray-600 dark:hover:text-white"
				data-modal-hide="delete-roadmap-modal">
				<svg
					class="w-3 h-3"
					aria-hidden="true"
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 14 14">
					<path
						stroke="currentColor"
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6" />
				</svg>
				<span class="sr-only">Close modal</span>
			</button>
			<div class="p-4 md:p-5 text-center">
				<svg
					class="mx-auto mb-4 text-red-600 w-12 h-12 dark:text-gray-200"
					aria-hidden="true"
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 20 20">
					<path
						stroke="currentColor"
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M10 11V6m0 8h.01M19 10a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z" />
				</svg>
				<h3 class="text-lg font-bold text-gray-700 dark:text-gray-400">
					Are you sure you want to Archive this roadmap?
				</h3>
				<p class="mb-5 font-xs text-gray-500">
					When this roadmaps is archived, all courses and lessons under this are archived.
					Additionally, other users can not see this roadmaps and its courses even if it was
					assigned to them.
				</p>
				<button
					data-modal-hide="delete-roadmap-modal"
					type="button"
					class="text-white bg-red-600 hover:bg-red-800 focus:ring-4 focus:outline-none focus:ring-red-300 dark:focus:ring-red-800 font-medium rounded-lg text-sm inline-flex items-center px-5 py-2.5 text-center">
					Yes, I'm sure
				</button>
				<button
					data-modal-hide="delete-roadmap-modal"
					type="button"
					class="py-2.5 px-5 ms-3 text-sm font-medium text-gray-900 focus:outline-none bg-white rounded-lg border border-gray-200 hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-4 focus:ring-gray-100 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700"
					>No, cancel</button>
			</div>
		</div>
	</div>
</div>

<!-- Move Courses modal -->
<form
	action="#"
	method="get"
	id="move-course-modal"
	tabindex="-1"
	aria-hidden="true"
	class="fixed top-0 left-0 right-0 z-50 hidden w-full p-4 overflow-x-hidden overflow-y-auto md:inset-0 h-modal md:h-full justify-center items-center">
	<div class="relative w-full h-full max-w-4xl md:h-auto">
		<!-- Modal content -->
		<div class="relative bg-white rounded-lg shadow dark:bg-gray-800">
			<!-- Modal header -->
			<div class="flex items-start justify-between p-4 rounded-t">
				<h3 class="text-xl font-semibold text-gray-900 dark:text-gray-400">Add existing Courses</h3>
				<button
					type="button"
					class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white"
					data-modal-toggle="move-course-modal">
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
							<button
								class="inline-block pb-2 pr-1"
								id="brand-tab"
								data-tabs-target="#brand"
								type="button"
								role="tab"
								aria-controls="profile"
								aria-selected="false">
								Select Courses
							</button>
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
							<h5 class="text-lg font-medium text-black dark:text-white">Book</h5>

							<div class="flex items-center">
								<input
									id="apple"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="apple"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Accelerate
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
									Hire Smart From Start
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="acer"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label for="acer" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Song of Ice and Fire
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
									High Output Management
								</label>
							</div>
						</div>

						<div class="space-y-2">
							<h5 class="text-lg font-medium text-black dark:text-white">Engineering</h5>

							<div class="flex items-center">
								<input
									id="beats"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label
									for="beats"
									class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Production Deployment Course
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
									Clear Coding Course
								</label>
							</div>

							<div class="flex items-center">
								<input
									id="benq"
									type="checkbox"
									value=""
									class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />

								<label for="benq" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
									Github Etiquette Course
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
									Onboarding Course
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
									Cold Calling Course
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
									Account Nurturing Course
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
									Email Marketing Course
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
									Other Sales Course
								</label>
							</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Modal footer -->
			<div class="flex items-center p-6 space-x-4 rounded-b dark:border-gray-600">
				<button
					data-modal-toggle="move-course-modal"
					class="text-white bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:outline-none focus:ring-primary-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-primary-700 dark:hover:bg-primary-800 dark:focus:ring-primary-800">
					Save
				</button>
				<button
					data-modal-toggle="move-course-modal"
					class="py-2.5 px-5 text-sm font-medium text-gray-900 focus:outline-none bg-white rounded-lg border border-gray-200 hover:bg-gray-100 hover:text-primary-700 focus:z-10 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700">
					Cancel
				</button>
			</div>
		</div>
	</div>
</form>
