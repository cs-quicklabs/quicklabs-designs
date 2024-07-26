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
			<nav class="flex" aria-label="Breadcrumb"></nav>
		</div>
		<div class="px-4 mb-8 sm:flex sm:items-center sm:justify-center sm:px-6 lg:px-8">
			<div class="items-baseline">
				<h1 class="text-5xl font-extrabold leading-tight">Content Repository</h1>
				<p
					class="mt-1 ml-1 text-sm text-gray-500 truncate sm:flex sm:items-center sm:justify-center">
					(10 Roadmaps, 20 Courses)
				</p>
			</div>
		</div>

		<div class="px-8 py-8 sm:flex sm:items-center sm:justify-between sm:px-6 lg:px-8">
			<div class="flex flex-wrap items-baseline -mt-2 -ml-2">
				<h1 class="text-3xl font-bold leading-tight">All Roadmaps</h1>
				<p class="mt-1 ml-1 text-sm text-gray-500 truncate">(10 roadmaps)</p>
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
								<h3 class="mt-2 text-sm font-semibold text-gray-900">Create New Roadmap</h3>
							</div>
						</div>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/roadmap">
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
						<a href="/quick-learn/content/roadmap">
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
						<a href="/quick-learn/content/roadmap">
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
						<a href="/quick-learn/content/roadmap">
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
				<h1 class="text-3xl font-bold leading-tight">All Courses</h1>
				<p class="mt-1 ml-1 text-sm text-gray-500 truncate">(20 courses)</p>
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
						<a href="/quick-learn/content/roadmap">
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
						<a href="/quick-learn/content/roadmap">
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
						<a href="/quick-learn/content/roadmap">
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
						<a href="/quick-learn/content/roadmap">
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
						<a href="/quick-learn/content/roadmap">
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
						<a href="/quick-learn/content/roadmap">
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
