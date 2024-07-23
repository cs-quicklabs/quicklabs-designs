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
						<a href="1/roadmaps">
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
