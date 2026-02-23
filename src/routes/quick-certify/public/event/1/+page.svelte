<script>
	import Header from '$quick-certify/common/navbar/header.svelte';
	import Footer from '$quick-certify/common/navbar/footer.svelte';
</script>

<Header />
<div class="bg-gray-50 min-h-screen p-4">
	<!-- Breadcrumb & Title -->
	<div
		class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 p-4 rounded-sm border border-gray-200 bg-white">
		<div>
			<nav class="sm:hidden" aria-label="Back">
				<a href="#" class="flex items-center text-sm font-medium text-gray-500 hover:text-gray-700">
					<svg
						class="mr-1 -ml-1 size-5 shrink-0 text-gray-400"
						viewBox="0 0 20 20"
						fill="currentColor"
						aria-hidden="true">
						<path
							fill-rule="evenodd"
							d="M11.78 5.22a.75.75 0 0 1 0 1.06L8.06 10l3.72 3.72a.75.75 0 1 1-1.06 1.06l-4.25-4.25a.75.75 0 0 1 0-1.06l4.25-4.25a.75.75 0 0 1 1.06 0Z"
							clip-rule="evenodd" />
					</svg>
					Back
				</a>
			</nav>
			<nav class="hidden sm:flex" aria-label="Breadcrumb">
				<ol role="list" class="flex items-center space-x-4">
					<li>
						<div class="flex">
							<a
								href="/quick-certify/public/company"
								class="text-sm font-medium text-gray-500 hover:text-gray-700 hover:underline"
								>Issuer Profile</a>
						</div>
					</li>
					<li>
						<div class="flex items-center">
							<svg
								class="size-5 shrink-0 text-gray-400"
								viewBox="0 0 20 20"
								fill="currentColor"
								aria-hidden="true">
								<path
									fill-rule="evenodd"
									d="M8.22 5.22a.75.75 0 0 1 1.06 0l4.25 4.25a.75.75 0 0 1 0 1.06l-4.25 4.25a.75.75 0 0 1-1.06-1.06L11.94 10 8.22 6.28a.75.75 0 0 1 0-1.06Z"
									clip-rule="evenodd" />
							</svg>
							<a
								href="/quick-certify/public/event"
								class="ml-4 text-sm font-medium text-gray-500 hover:text-gray-700 hover:underline"
								>Events</a>
						</div>
					</li>
					<li>
						<div class="flex items-center">
							<svg
								class="size-5 shrink-0 text-gray-400"
								viewBox="0 0 20 20"
								fill="currentColor"
								aria-hidden="true">
								<path
									fill-rule="evenodd"
									d="M8.22 5.22a.75.75 0 0 1 1.06 0l4.25 4.25a.75.75 0 0 1 0 1.06l-4.25 4.25a.75.75 0 0 1-1.06-1.06L11.94 10 8.22 6.28a.75.75 0 0 1 0-1.06Z"
									clip-rule="evenodd" />
							</svg>
							<span class="ml-4 text-sm font-medium text-gray-500">Understanding Clean Coding Practices</span>
						</div>
					</li>
				</ol>
			</nav>
		</div>
		<div class="mt-2 md:flex md:items-center md:justify-between">
			<div class="min-w-0 flex-1">
				<h2 class="text-2xl/7 font-bold text-gray-900 sm:truncate sm:text-3xl sm:tracking-tight">
					Understanding Clean Coding Practices
				</h2>
				<p class="mt-1 text-sm text-gray-500">Created on June 12, 2024</p>
			</div>
		</div>
	</div>

	<!-- Banner / Appearance Section -->
	<div class="max-w-7xl mx-auto rounded-sm border border-gray-200 bg-white overflow-hidden mt-4">
		<div class="relative">
			<img
				class="w-full h-64 sm:h-80 lg:h-112 object-cover"
				src="/quick-certify/rashi.png"
				alt="Event Certificate" />
		</div>
	</div>

	<!-- Event Details Section -->
	<div class="max-w-7xl mx-auto mt-4 flex flex-col lg:flex-row gap-4">
		<!-- Left: Description & Learning Resources -->
		<div class="flex-1 flex flex-col gap-4">
			<!-- Description -->
			<div class="bg-white rounded-sm border border-gray-200 p-6">
				<h3 class="text-lg font-semibold text-gray-900 mb-3">Description</h3>
				<p class="text-sm text-gray-600 leading-relaxed">
					This event focuses on teaching developers the principles of clean code, including readable naming conventions, modular design, effective commenting, and SOLID principles. Participants will engage in hands-on exercises and code reviews to apply best practices in real-world scenarios. By the end of the session, attendees will be equipped with practical techniques to write maintainable, scalable, and efficient code.
				</p>
			</div>

			<!-- Learning Resources -->
			<div class="bg-white rounded-sm border border-gray-200 p-6">
				<h3 class="text-lg font-semibold text-gray-900 mb-3">Learning Resources</h3>
				<a
					href="#"
					class="inline-flex items-center gap-2 text-sm text-blue-600 hover:underline"
					target="_blank"
					rel="noopener noreferrer">
					<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1" />
					</svg>
					https://resources.cleancode.dev/clean-coding-practices
				</a>
			</div>
		</div>

		<!-- Right: Event Metadata -->
		<div class="lg:w-80 flex flex-col gap-4">
			<div class="bg-white rounded-sm border border-gray-200 p-6">
				<h3 class="text-lg font-semibold text-gray-900 mb-4">Event Information</h3>
				<dl class="space-y-4">
					<div>
						<dt class="text-xs font-medium text-gray-500 uppercase tracking-wide">Event Type</dt>
						<dd class="mt-1 text-sm text-gray-900">Workshop</dd>
					</div>
					<div>
						<dt class="text-xs font-medium text-gray-500 uppercase tracking-wide">Event Level</dt>
						<dd class="mt-1 text-sm text-gray-900">Intermediate</dd>
					</div>
					<div>
						<dt class="text-xs font-medium text-gray-500 uppercase tracking-wide">Event Format</dt>
						<dd class="mt-1 text-sm text-gray-900">Virtual</dd>
					</div>
					<div>
						<dt class="text-xs font-medium text-gray-500 uppercase tracking-wide">Duration</dt>
						<dd class="mt-1 text-sm text-gray-900">2 Hours 30 Minutes</dd>
					</div>
				</dl>
			</div>

			<!-- Skills -->
			<div class="bg-white rounded-sm border border-gray-200 p-6">
				<h3 class="text-lg font-semibold text-gray-900 mb-3">Skills</h3>
				<div class="flex flex-wrap gap-2">
					<span class="inline-flex items-center rounded-full bg-primary-50 px-3 py-1 text-xs font-medium text-primary-700">Clean Code</span>
					<span class="inline-flex items-center rounded-full bg-primary-50 px-3 py-1 text-xs font-medium text-primary-700">SOLID Principles</span>
					<span class="inline-flex items-center rounded-full bg-primary-50 px-3 py-1 text-xs font-medium text-primary-700">Code Review</span>
					<span class="inline-flex items-center rounded-full bg-primary-50 px-3 py-1 text-xs font-medium text-primary-700">Refactoring</span>
					<span class="inline-flex items-center rounded-full bg-primary-50 px-3 py-1 text-xs font-medium text-primary-700">Design Patterns</span>
					<span class="inline-flex items-center rounded-full bg-primary-50 px-3 py-1 text-xs font-medium text-primary-700">JavaScript</span>
				</div>
			</div>
		</div>
	</div>

	<!-- Participants Section -->
	<div
		class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 p-4 rounded-sm border border-gray-200 bg-white mt-4">
		<div class="flex items-center justify-between mb-2">
			<h3 class="text-lg font-semibold text-gray-900">Participants</h3>
			<span class="text-sm text-gray-500">16 participants</span>
		</div>

		<!-- Search & Sort -->
		<div class="relative bg-white sm:rounded-sm">
			<div class="flex flex-col items-center justify-between md:flex-row md:space-y-0">
				<div class="w-full me-4">
					<form class="flex items-center">
						<label for="participant-search" class="sr-only">Search</label>
						<div class="relative w-full">
							<div class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
								<svg
									aria-hidden="true"
									class="w-5 h-5 text-gray-500"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg">
									<path
										fill-rule="evenodd"
										d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
										clip-rule="evenodd" />
								</svg>
							</div>
							<input
								type="text"
								id="participant-search"
								class="block w-full p-1.5 pl-10 text-sm text-gray-900 border border-gray-300 rounded-sm bg-gray-50 focus:ring-primary-500 focus:border-primary-500"
								placeholder="Search participant by name"
								required="" />
						</div>
					</form>
				</div>
				<div
					class="flex flex-col items-stretch justify-end flex-shrink-0 w-full space-y-2 md:w-auto md:flex-row md:space-y-0 md:items-center md:space-x-3">
					<div class="flex items-center w-full space-x-3 md:w-auto">
						<button
							id="participantSortButton"
							data-dropdown-toggle="participantSortDropdown"
							class="flex items-center justify-center w-full px-4 py-1.5 text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-sm md:w-auto focus:outline-none hover:bg-gray-100 hover:text-primary-700 focus:z-10 focus:ring-4 focus:ring-gray-200"
							type="button">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								aria-hidden="true"
								class="w-4 h-4 mr-2 text-gray-400"
								viewBox="0 0 20 20"
								fill="currentColor">
								<path
									fill-rule="evenodd"
									d="M3 3a1 1 0 011-1h12a1 1 0 011 1v3a1 1 0 01-.293.707L12 11.414V15a1 1 0 01-.293.707l-2 2A1 1 0 018 17v-5.586L3.293 6.707A1 1 0 013 6V3z"
									clip-rule="evenodd" />
							</svg>
							Sort By
							<svg
								class="-mr-1 ml-1.5 w-5 h-5"
								fill="currentColor"
								viewBox="0 0 20 20"
								xmlns="http://www.w3.org/2000/svg"
								aria-hidden="true">
								<path
									clip-rule="evenodd"
									fill-rule="evenodd"
									d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" />
							</svg>
						</button>
						<!-- Dropdown menu -->
						<div
							id="participantSortDropdown"
							class="z-10 hidden w-48 p-3 bg-white rounded-sm shadow">
							<ul class="space-y-2 text-sm cursor-pointer" aria-labelledby="participantSortButton">
								<li class="flex items-center hover:underline cursor-pointer">
									<label class="ml-2 text-sm font-medium text-gray-900 cursor-pointer">
										Newest First
									</label>
								</li>
								<li class="flex items-center hover:underline cursor-pointer">
									<label class="ml-2 text-sm font-medium text-gray-900 cursor-pointer">
										Oldest First
									</label>
								</li>
							</ul>
						</div>
					</div>
				</div>
			</div>
		</div>

		<!-- Participant Grid -->
		<div class="grid grid-cols-1 gap-4 sm:grid-cols-2 lg:grid-cols-3 mt-6">
			<div
				class="relative flex items-center space-x-3 rounded-sm border border-gray-300 bg-white px-4 py-3 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 hover:border-gray-400">
				<div class="shrink-0">
					<img
						class="size-10 rounded-full"
						src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt="" />
				</div>
				<div class="min-w-0 flex-1">
					<a href="/quick-certify/public/event/1/person" class="focus:outline-hidden">
						<span class="absolute inset-0" aria-hidden="true"></span>
						<p class="text-sm font-medium text-gray-900">Leslie Alexander</p>
						<p class="truncate text-sm text-gray-500">Co-Founder / CEO</p>
					</a>
				</div>
			</div>

			<div
				class="relative flex items-center space-x-3 rounded-sm border border-gray-300 bg-white px-4 py-3 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 hover:border-gray-400">
				<div class="shrink-0">
					<img
						class="size-10 rounded-full"
						src="https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt="" />
				</div>
				<div class="min-w-0 flex-1">
					<a href="/quick-certify/public/event/1/person" class="focus:outline-hidden">
						<span class="absolute inset-0" aria-hidden="true"></span>
						<p class="text-sm font-medium text-gray-900">Michael Foster</p>
						<p class="truncate text-sm text-gray-500">Software Engineer</p>
					</a>
				</div>
			</div>

			<div
				class="relative flex items-center space-x-3 rounded-sm border border-gray-300 bg-white px-4 py-3 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 hover:border-gray-400">
				<div class="shrink-0">
					<img
						class="size-10 rounded-full"
						src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt="" />
				</div>
				<div class="min-w-0 flex-1">
					<a href="/quick-certify/public/event/1/person" class="focus:outline-hidden">
						<span class="absolute inset-0" aria-hidden="true"></span>
						<p class="text-sm font-medium text-gray-900">Dries Vincent</p>
						<p class="truncate text-sm text-gray-500">Frontend Developer</p>
					</a>
				</div>
			</div>

			<div
				class="relative flex items-center space-x-3 rounded-sm border border-gray-300 bg-white px-4 py-3 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 hover:border-gray-400">
				<div class="shrink-0">
					<img
						class="size-10 rounded-full"
						src="https://images.unsplash.com/photo-1517841905240-472988babdf9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt="" />
				</div>
				<div class="min-w-0 flex-1">
					<a href="/quick-certify/public/event/1/person" class="focus:outline-hidden">
						<span class="absolute inset-0" aria-hidden="true"></span>
						<p class="text-sm font-medium text-gray-900">Lindsay Walton</p>
						<p class="truncate text-sm text-gray-500">Backend Developer</p>
					</a>
				</div>
			</div>

			<div
				class="relative flex items-center space-x-3 rounded-sm border border-gray-300 bg-white px-4 py-3 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 hover:border-gray-400">
				<div class="shrink-0">
					<img
						class="size-10 rounded-full"
						src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt="" />
				</div>
				<div class="min-w-0 flex-1">
					<a href="/quick-certify/public/event/1/person" class="focus:outline-hidden">
						<span class="absolute inset-0" aria-hidden="true"></span>
						<p class="text-sm font-medium text-gray-900">Courtney Henry</p>
						<p class="truncate text-sm text-gray-500">Product Manager</p>
					</a>
				</div>
			</div>

			<div
				class="relative flex items-center space-x-3 rounded-sm border border-gray-300 bg-white px-4 py-3 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 hover:border-gray-400">
				<div class="shrink-0">
					<img
						class="size-10 rounded-full"
						src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt="" />
				</div>
				<div class="min-w-0 flex-1">
					<a href="/quick-certify/public/event/1/person" class="focus:outline-hidden">
						<span class="absolute inset-0" aria-hidden="true"></span>
						<p class="text-sm font-medium text-gray-900">Tom Cook</p>
						<p class="truncate text-sm text-gray-500">DevOps Engineer</p>
					</a>
				</div>
			</div>

			<div
				class="relative flex items-center space-x-3 rounded-sm border border-gray-300 bg-white px-4 py-3 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 hover:border-gray-400">
				<div class="shrink-0">
					<img
						class="size-10 rounded-full"
						src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt="" />
				</div>
				<div class="min-w-0 flex-1">
					<a href="/quick-certify/public/event/1/person" class="focus:outline-hidden">
						<span class="absolute inset-0" aria-hidden="true"></span>
						<p class="text-sm font-medium text-gray-900">Whitney Francis</p>
						<p class="truncate text-sm text-gray-500">QA Engineer</p>
					</a>
				</div>
			</div>

			<div
				class="relative flex items-center space-x-3 rounded-sm border border-gray-300 bg-white px-4 py-3 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 hover:border-gray-400">
				<div class="shrink-0">
					<img
						class="size-10 rounded-full"
						src="https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt="" />
				</div>
				<div class="min-w-0 flex-1">
					<a href="/quick-certify/public/event/1/person" class="focus:outline-hidden">
						<span class="absolute inset-0" aria-hidden="true"></span>
						<p class="text-sm font-medium text-gray-900">Leonard Krasner</p>
						<p class="truncate text-sm text-gray-500">Tech Lead</p>
					</a>
				</div>
			</div>

			<div
				class="relative flex items-center space-x-3 rounded-sm border border-gray-300 bg-white px-4 py-3 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 hover:border-gray-400">
				<div class="shrink-0">
					<img
						class="size-10 rounded-full"
						src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt="" />
				</div>
				<div class="min-w-0 flex-1">
					<a href="/quick-certify/public/event/1/person" class="focus:outline-hidden">
						<span class="absolute inset-0" aria-hidden="true"></span>
						<p class="text-sm font-medium text-gray-900">Floyd Miles</p>
						<p class="truncate text-sm text-gray-500">Data Analyst</p>
					</a>
				</div>
			</div>
		</div>

		<!-- Pagination -->
		<div class="relative overflow-hidden bg-white mt-8">
			<nav
				class="flex flex-col items-start justify-end p-4 space-y-3 md:flex-row md:items-center md:space-y-0"
				aria-label="Table navigation">
				<span class="text-sm font-normal text-gray-500"
					>Showing <span class="font-semibold text-gray-900">1-10</span> of
					<span class="font-semibold text-gray-900 me-8">16</span></span>
				<ul class="inline-flex items-stretch -space-x-px">
					<li>
						<a
							href="#"
							class="flex items-center justify-center h-full py-1.5 px-3 ml-0 text-gray-500 bg-white rounded-l-lg border border-gray-300 hover:bg-gray-100 hover:text-gray-700">
							<span class="sr-only">Previous</span>
							<svg
								class="w-5 h-5"
								aria-hidden="true"
								fill="currentColor"
								viewBox="0 0 20 20"
								xmlns="http://www.w3.org/2000/svg">
								<path
									fill-rule="evenodd"
									d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"
									clip-rule="evenodd"></path>
							</svg>
						</a>
					</li>
					<li>
						<a
							href="#"
							aria-current="page"
							class="z-10 flex items-center justify-center px-3 py-2 text-sm leading-tight border text-primary-600 bg-primary-50 border-primary-300 hover:bg-primary-100 hover:text-primary-700"
							>1</a>
					</li>
					<li>
						<a
							href="#"
							class="flex items-center justify-center px-3 py-2 text-sm leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700"
							>2</a>
					</li>
					<li>
						<a
							href="#"
							class="flex items-center justify-center h-full py-1.5 px-3 leading-tight text-gray-500 bg-white rounded-r-lg border border-gray-300 hover:bg-gray-100 hover:text-gray-700">
							<span class="sr-only">Next</span>
							<svg
								class="w-5 h-5"
								aria-hidden="true"
								fill="currentColor"
								viewBox="0 0 20 20"
								xmlns="http://www.w3.org/2000/svg">
								<path
									fill-rule="evenodd"
									d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
									clip-rule="evenodd"></path>
							</svg>
						</a>
					</li>
				</ul>
			</nav>
		</div>
	</div>
</div>
<Footer />
