<script>
	import NavBar from '$quick-learn/common/navbar/admin.svelte';
	import { onMount } from 'svelte';
	onMount(() => {
		window.addEventListener('load', function () {
			document.querySelector('[data-modal-toggle="defaultModal"]').click();
		});
	});
</script>

<NavBar />
<main>
	<div class="bg-gray-50 relative z-0 flex-1 overflow-x-scroll focus:outline-none h-screen">
		<div class="px-4 py-4 sm:flex sm:items-center sm:justify-center sm:px-6 lg:px-8">
			<nav class="flex" aria-label="Breadcrumb">
				<ol class="inline-flex justify-self-center space-x-1 md:space-x-2 rtl:space-x-reverse">
					<li class="inline-flex items-center">
						<a
							href="/quick-learn/team"
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
							Team
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
								href="1"
								class="ms-1 text-sm font-medium text-gray-700 hover:text-blue-600 md:ms-2 dark:text-gray-400 dark:hover:text-white hover:underline"
								>Aashish Dhawan</a>
						</div>
					</li>
				</ol>
			</nav>
		</div>
		<div class="px-4 mb-8 sm:flex sm:items-center sm:justify-center sm:px-6 lg:px-8">
			<div class="items-baseline">
				<h1 class="text-5xl font-extrabold leading-tight">Aashish Dhawan</h1>
				<p
					class="mt-1 ml-1 text-sm text-gray-500 truncate sm:flex sm:items-center sm:justify-center">
					(10 Roadmaps, 20 Courses)
				</p>
				<div class="sm:flex sm:items-center sm:justify-center mt-2">
					<a
						href="/quick-learn/team/edit"
						data-tooltip-target="tooltip-edit"
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
					</a>
					<div
						id="tooltip-edit"
						role="tooltip"
						class="absolute z-10 invisible inline-block px-3 py-2 text-sm font-medium text-white transition-opacity duration-300 bg-gray-900 rounded-lg shadow-sm opacity-0 tooltip dark:bg-gray-700">
						Edit User
						<div class="tooltip-arrow" data-popper-arrow></div>
					</div>
					<button
						data-tooltip-target="tooltip-archive"
						data-modal-target="archive-user-modal"
						data-modal-toggle="archive-user-modal"
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
						id="tooltip-archive"
						role="tooltip"
						class="absolute z-10 invisible inline-block px-3 py-2 text-sm font-medium text-white transition-opacity duration-300 bg-gray-900 rounded-lg shadow-sm opacity-0 tooltip dark:bg-gray-700">
						Deactivate User
						<div class="tooltip-arrow" data-popper-arrow></div>
					</div>
					<button
						data-tooltip-target="tooltip-activities"
						data-modal-target="user-activities-modal"
						data-modal-toggle="user-activities-modal"
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
								d="M15.042 21.672 13.684 16.6m0 0-2.51 2.225.569-9.47 5.227 7.917-3.286-.672Zm-7.518-.267A8.25 8.25 0 1 1 20.25 10.5M8.288 14.212A5.25 5.25 0 1 1 17.25 10.5" />
						</svg>

						<span class="sr-only">Icon description</span>
					</button>
					<div
						id="tooltip-activities"
						role="tooltip"
						class="absolute z-10 invisible inline-block px-3 py-2 text-sm font-medium text-white transition-opacity duration-300 bg-gray-900 rounded-lg shadow-sm opacity-0 tooltip dark:bg-gray-700">
						User Activities
						<div class="tooltip-arrow" data-popper-arrow></div>
					</div>
				</div>
			</div>
		</div>

		<div class="px-8 py-8 sm:flex sm:items-center sm:justify-between sm:px-6 lg:px-8">
			<div class="flex flex-wrap items-baseline -mt-2 -ml-2">
				<h1 class="text-3xl font-bold leading-tight">Roadmaps</h1>
				<p class="mt-1 ml-1 text-sm text-gray-500 truncate">(9 roadmaps)</p>
			</div>
		</div>
		<div class="relative px-6 grid gap-10 pb-4" id="release_notes">
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
								<h3 class="mt-2 text-sm font-semibold text-gray-900">Assign New Roadmap</h3>
							</div>
						</div>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="1/roadmaps">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Backend Developer Roadmap
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									This is Space for learning things related to backend development.
								</p>
								<p class="font-bold text-xs text-gray-500 line-clamp-2 mt-4 pb-2">37% Complete</p>
								<div class="overflow-hidden rounded-full bg-gray-200">
									<div class="h-2 rounded-full bg-green-600" style="width: 37.5%"></div>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="1/roadmaps">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Frontend Developer Roadmap
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									This is Space for learning things related to Frontend development.
								</p>
								<p class="font-bold text-xs text-gray-500 line-clamp-2 mt-4 pb-2">50% Complete</p>
								<div class="overflow-hidden rounded-full bg-gray-200">
									<div class="h-2 rounded-full bg-green-600" style="width: 50%"></div>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="1/roadmaps">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Clean Code Learning Roadmap
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									This is Space for learning things related to Frontend development.
								</p>
								<p class="font-bold text-xs text-gray-500 line-clamp-2 mt-4 pb-2">10% Complete</p>
								<div class="overflow-hidden rounded-full bg-gray-200">
									<div class="h-2 rounded-full bg-green-600" style="width: 10%"></div>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="1/roadmaps">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									HR Learning Roadmap
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									This is Space for learning things related to HR deaprtment.
								</p>
								<p class="font-bold text-xs text-gray-500 line-clamp-2 mt-4 pb-2">90% Complete</p>
								<div class="overflow-hidden rounded-full bg-gray-200">
									<div class="h-2 rounded-full bg-green-600" style="width: 90%"></div>
								</div>
							</div>
						</a>
					</li>
				</ul>
			</div>
		</div>
		<div class="px-8 py-8 sm:flex sm:items-center sm:justify-between sm:px-6 lg:px-8">
			<div class="flex flex-wrap items-baseline -mt-2 -ml-2">
				<h1 class="text-3xl font-bold leading-tight">Courses</h1>
				<p class="mt-1 ml-1 text-sm text-gray-500 truncate">(19 courses)</p>
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
						<a href="1/roadmaps">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Git Baisc Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn Git basics in this course.
								</p>
								<p class="font-bold text-xs text-gray-500 line-clamp-2 mt-4 pb-2">90% Complete</p>
								<div class="overflow-hidden rounded-full bg-gray-200">
									<div class="h-2 rounded-full bg-green-600" style="width: 90%"></div>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="1/roadmaps">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									HTML Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn HTML basics in this course.
								</p>
								<p class="font-bold text-xs text-gray-500 line-clamp-2 mt-4 pb-2">10% Complete</p>
								<div class="overflow-hidden rounded-full bg-gray-200">
									<div class="h-2 rounded-full bg-green-600" style="width: 10%"></div>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="1/roadmaps">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									TailwindCSS Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn TailwindCSS basics in this course.
								</p>
								<p class="font-bold text-xs text-gray-500 line-clamp-2 mt-4 pb-2">0% Complete</p>
								<div class="overflow-hidden rounded-full bg-gray-200">
									<div class="h-2 rounded-full bg-green-600" style="width: 00%"></div>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="1/roadmaps">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Email Etiquette Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn etiquette basics in this course.
								</p>
								<p class="font-bold text-xs text-gray-500 line-clamp-2 mt-4 pb-2">100% Complete</p>
								<div class="overflow-hidden rounded-full bg-gray-200">
									<div class="h-2 rounded-full bg-green-600" style="width: 100%"></div>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="1/roadmaps">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Accelerate Book Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn Accelerate book topics in this course.
								</p>
								<p class="font-bold text-xs text-gray-500 line-clamp-2 mt-4 pb-2">75% Complete</p>
								<div class="overflow-hidden rounded-full bg-gray-200">
									<div class="h-2 rounded-full bg-green-600" style="width: 75%"></div>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="1/roadmaps">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-40">
								<h1
									id="message-heading"
									class="font-medium text-gray-900 line-clamp-2 group-hover:underline">
									Hire Smart Book Course
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-2 mt-2">
									Learn Hiring Smart book topics in this course.
								</p>
								<p class="font-bold text-xs text-gray-500 line-clamp-2 mt-4 pb-2">20% Complete</p>
								<div class="overflow-hidden rounded-full bg-gray-200">
									<div class="h-2 rounded-full bg-green-600" style="width: 20%"></div>
								</div>
							</div>
						</a>
					</li>
				</ul>
			</div>
		</div>
	</div>
</main>

<!-- Delete Roadmap modal -->
<div
	id="archive-user-modal"
	tabindex="-1"
	class="hidden overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-[calc(100%-1rem)] max-h-full">
	<div class="relative p-4 w-full max-w-md max-h-full">
		<div class="relative bg-white rounded-lg shadow dark:bg-gray-700">
			<button
				type="button"
				class="absolute top-3 end-2.5 text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm w-8 h-8 ms-auto inline-flex justify-center items-center dark:hover:bg-gray-600 dark:hover:text-white"
				data-modal-hide="archive-user-modal">
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
					Are you sure you want to deactivate this user?
				</h3>
				<p class="mb-5 font-xs text-gray-500">
					When deactivated, this user will no longer be able to access the platform.
				</p>
				<button
					data-modal-hide="archive-user-modal"
					type="button"
					class="text-white bg-red-600 hover:bg-red-800 focus:ring-4 focus:outline-none focus:ring-red-300 dark:focus:ring-red-800 font-medium rounded-lg text-sm inline-flex items-center px-5 py-2.5 text-center">
					Yes, I'm sure
				</button>
				<button
					data-modal-hide="archive-user-modal"
					type="button"
					class="py-2.5 px-5 ms-3 text-sm font-medium text-gray-900 focus:outline-none bg-white rounded-lg border border-gray-200 hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-4 focus:ring-gray-100 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700"
					>No, cancel</button>
			</div>
		</div>
	</div>
</div>

<div
	id="user-activities-modal"
	tabindex="-1"
	aria-hidden="true"
	class="fixed left-0 right-0 top-0 z-50 hidden h-[calc(100%-1rem)] max-h-full w-full items-center justify-center overflow-y-auto overflow-x-hidden antialiased md:inset-0">
	<div class="relative max-h-full w-full max-w-4xl p-4">
		<!-- Modal content -->
		<div class="relative rounded-lg bg-white p-4 shadow dark:bg-gray-800 sm:p-5">
			<!-- Modal header -->
			<div
				class="mb-4 flex items-center justify-between rounded-t border-b pb-4 dark:border-gray-700 sm:mb-5">
				<h3 class="text-lg font-semibold text-gray-900 dark:text-white">
					Aashish Dhawan's Activities
				</h3>
				<button
					type="button"
					class="ml-auto inline-flex items-center rounded-lg bg-transparent p-1.5 text-sm text-gray-400 hover:bg-gray-200 hover:text-gray-900 dark:hover:bg-gray-600 dark:hover:text-white"
					data-modal-toggle="user-activities-modal">
					<svg
						aria-hidden="true"
						class="h-5 w-5"
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
			<div class="grid md:grid-cols-2 gap-5 md:gap-8">
				<ol class="relative ms-3 border-s border-dashed border-gray-200 dark:border-gray-700">
					<li class="mb-6 ms-6">
						<span
							class="absolute -start-4 flex h-8 w-8 items-center justify-center rounded-full bg-white ring-4 ring-white dark:bg-gray-800 dark:ring-gray-800">
							<svg
								class="h-5 w-5 text-green-500"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								fill="none"
								viewBox="0 0 24 24">
								<path
									stroke="currentColor"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M10 3v4a1 1 0 0 1-1 1H5m4 6 2 2 4-4m4-8v16a1 1 0 0 1-1 1H6a1 1 0 0 1-1-1V7.914a1 1 0 0 1 .293-.707l3.914-3.914A1 1 0 0 1 9.914 3H18a1 1 0 0 1 1 1Z" />
							</svg>
						</span>
						<h3
							class="mb-0.5 flex items-center pt-1 text-base font-semibold text-gray-900 dark:text-white">
							Git Cherry Pick command and its usage
						</h3>
						<time class="mb-2 block text-gray-500 dark:text-gray-400 text-xs">
							Marked completed on September 12, 2024 at 12:07 AM
						</time>
					</li>

					<li class="mb-6 ms-6">
						<span
							class="absolute -start-4 flex h-8 w-8 items-center justify-center rounded-full bg-white ring-4 ring-white dark:bg-gray-800 dark:ring-gray-800">
							<svg
								class="h-5 w-5 text-green-500"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								fill="none"
								viewBox="0 0 24 24">
								<path
									stroke="currentColor"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M10 3v4a1 1 0 0 1-1 1H5m4 6 2 2 4-4m4-8v16a1 1 0 0 1-1 1H6a1 1 0 0 1-1-1V7.914a1 1 0 0 1 .293-.707l3.914-3.914A1 1 0 0 1 9.914 3H18a1 1 0 0 1 1 1Z" />
							</svg>
						</span>

						<h3
							class="mb-0.5 flex items-center pt-1 text-base font-semibold text-gray-900 dark:text-white">
							Git Installation and its usage
						</h3>
						<time class="mb-2 block text-gray-500 dark:text-gray-400 text-xs">
							Marked completed on September 11, 2024 at 09:07 AM
						</time>
					</li>
					<li class="mb-6 ms-6">
						<span
							class="absolute -start-4 flex h-8 w-8 items-center justify-center rounded-full bg-white ring-4 ring-white dark:bg-gray-800 dark:ring-gray-800">
							<svg
								class="h-5 w-5 text-gray-500 dark:text-gray-400"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								fill="none"
								viewBox="0 0 24 24">
								<path
									stroke="currentColor"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M13 7h6l2 4m-8-4v8m0-8V6a1 1 0 0 0-1-1H4a1 1 0 0 0-1 1v9h2m8 0H9m4 0h2m4 0h2v-4m0 0h-5m3.5 5.5a2.5 2.5 0 1 1-5 0 2.5 2.5 0 0 1 5 0Zm-10 0a2.5 2.5 0 1 1-5 0 2.5 2.5 0 0 1 5 0Z" />
							</svg>
						</span>
						<h3
							class="mb-0.5 flex items-center pt-1 text-base font-semibold text-gray-900 dark:text-white">
							Git Stash and Squash Commands
						</h3>
						<time class="mb-2 block text-gray-500 dark:text-gray-400 text-xs">
							Missed on September 12, 2024 at 12:07 AM
						</time>
					</li>

					<li class="mb-6 ms-6">
						<span
							class="absolute -start-4 flex h-8 w-8 items-center justify-center rounded-full bg-white ring-4 ring-white dark:bg-gray-800 dark:ring-gray-800">
							<svg
								class="h-5 w-5 text-green-500"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								fill="none"
								viewBox="0 0 24 24">
								<path
									stroke="currentColor"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M10 3v4a1 1 0 0 1-1 1H5m4 6 2 2 4-4m4-8v16a1 1 0 0 1-1 1H6a1 1 0 0 1-1-1V7.914a1 1 0 0 1 .293-.707l3.914-3.914A1 1 0 0 1 9.914 3H18a1 1 0 0 1 1 1Z" />
							</svg>
						</span>
						<h3
							class="mb-0.5 flex items-center pt-1 text-base font-semibold text-gray-900 dark:text-white">
							Git Cherry Pick command and its usage
						</h3>
						<time class="mb-2 block text-gray-500 dark:text-gray-400 text-xs">
							Marked completed on September 12, 2024 at 12:07 AM
						</time>
					</li>

					<li class="ms-6">
						<span
							class="absolute -start-4 flex h-8 w-8 items-center justify-center rounded-full bg-white ring-4 ring-white dark:bg-gray-800 dark:ring-gray-800">
							<svg
								class="h-5 w-5 text-green-500"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								width="24"
								height="24"
								fill="none"
								viewBox="0 0 24 24">
								<path
									stroke="currentColor"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M10 3v4a1 1 0 0 1-1 1H5m4 6 2 2 4-4m4-8v16a1 1 0 0 1-1 1H6a1 1 0 0 1-1-1V7.914a1 1 0 0 1 .293-.707l3.914-3.914A1 1 0 0 1 9.914 3H18a1 1 0 0 1 1 1Z" />
							</svg>
						</span>

						<h3
							class="mb-0.5 flex items-center pt-1 text-base font-semibold text-gray-900 dark:text-white">
							Git Installation and its usage
						</h3>
						<time class="mb-2 block text-gray-500 dark:text-gray-400 text-xs">
							Marked completed on September 11, 2024 at 09:07 AM
						</time>
					</li>
				</ol>
			</div>
		</div>
	</div>
</div>
