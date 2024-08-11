<script>
	import NavBar from '$quick-learn/common/navbar/superadmin.svelte';
</script>

<NavBar />
<main>
	<div class="bg-gray-50 relative z-0 flex-1 overflow-x-scroll focus:outline-none h-screen">
		<div class="px-4 mb-8 sm:flex sm:items-center sm:justify-center sm:px-6 lg:px-8">
			<div class="items-baseline mt-8">
				<h1 class="text-5xl font-extrabold text-center leading-tight">Community Courses</h1>
				<p
					class="mt-1 ml-1 text-sm text-gray-500 truncate sm:flex sm:items-center sm:justify-center">
					Following courses have been made public by community members. You can copy these courses
					to your organization and make changes as per your requirements.
				</p>

				<p
					class="mt-1 ml-1 text-sm text-gray-500 truncate sm:flex sm:items-center sm:justify-center">
					(20 Courses)
				</p>
			</div>
		</div>

		<div class="relative px-6 grid gap-10 pb-16" id="release_notes">
			<div id="created-spaces">
				<ul
					role="list"
					class="grid grid-cols-2 gap-x-4 gap-y-8 sm:grid-cols-3 sm:gap-x-6 lg:grid-cols-4 2xl:grid-cols-5 xl:gap-x-8">
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/community/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Git Baisc Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn Git basics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-2 pb-2">
									Published by Crownstack Technologies
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/community/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									HTML Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn HTML basics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-2 pb-2">
									Published by Crownstack Technologies
								</p>

								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/community/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									TailwindCSS Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn TailwindCSS basics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-2 pb-2">
									Published by Crownstack Technologies
								</p>

								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/community/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Email Etiquette Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn etiquette basics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-2 pb-2">
									Published by Crownstack Technologies
								</p>

								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/community/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Accelerate Book Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn Accelerate book topics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-2 pb-2">
									Published by Crownstack Technologies
								</p>

								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20 Lessons</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/community/course">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Hire Smart Book Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn Hiring Smart book topics in this course.
								</p>
								<p class="font-normal text-xs text-gray-500 line-clamp-2 mt-2 pb-2">
									Published by Crownstack Technologies
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
							<span class="inline-block pb-2 pr-1 text-gray-700" id="brand-tab">
								Select Courses
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
