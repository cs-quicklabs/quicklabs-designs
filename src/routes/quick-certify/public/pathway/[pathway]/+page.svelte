<script>
	import Header from '$quick-certify/common/navbar/header.svelte';
	import Footer from '$quick-certify/common/navbar/footer.svelte';

	let activeTab = $state('credentials');
	let searchQuery = $state('');

	// Expanded accordion state: track which credential index is open
	let expandedIndex = $state(-1);

	function toggleAccordion(index) {
		expandedIndex = expandedIndex === index ? -1 : index;
	}

	// Pathway data
	const pathway = {
		name: 'Full Stack Developer',
		description:
			'Master the fundamentals of full-stack web development from front-end frameworks to back-end databases and deployment pipelines.',
		status: 'Active',
		duration: '6 months',
		participantCount: 124,
		credentialCount: 5
	};

	// Final credential (the overlapping hero card)
	const finalCredential = {
		name: 'Full Stack Developer Certification',
		description:
			'This certification validates mastery in front-end, back-end, and DevOps skills. Holders have demonstrated proficiency across the entire modern web development stack.',
		image: '/quick-certify/rashi.png'
	};

	// Credentials list for the timeline
	const credentials = [
		{
			id: 1,
			name: 'React Basics',
			summary: 'Learn the fundamentals of React including components, state, and props.',
			description:
				'This credential covers React core concepts including JSX, component lifecycle, hooks, state management with useState and useReducer, and building reusable UI components. Candidates will build a complete single-page application as part of the assessment.',
			duration: '4 weeks',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 2,
			name: 'Node.js Fundamentals',
			summary: 'Build server-side applications with Node.js and Express.',
			description:
				'Covers Node.js runtime, event loop, modules, file system operations, building RESTful APIs with Express, middleware patterns, authentication, and error handling. Includes a capstone project building a production-ready API.',
			duration: '4 weeks',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 3,
			name: 'MongoDB Essentials',
			summary: 'Master NoSQL database design and operations with MongoDB.',
			description:
				'Learn MongoDB fundamentals including document modeling, CRUD operations, aggregation pipelines, indexing strategies, and integration with Node.js using Mongoose. Covers schema design patterns for real-world applications.',
			duration: '3 weeks',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 4,
			name: 'Docker & Kubernetes',
			summary: 'Containerize and orchestrate applications for modern deployment.',
			description:
				'Covers Docker containers, Dockerfiles, multi-stage builds, Docker Compose, Kubernetes pods, deployments, services, and ingress. Candidates will containerize a full-stack app and deploy it to a Kubernetes cluster.',
			duration: '5 weeks',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 5,
			name: 'CI/CD Pipelines',
			summary: 'Automate testing and deployment with continuous integration workflows.',
			description:
				'Learn to set up CI/CD pipelines using GitHub Actions, automated testing strategies, deployment automation, environment management, and monitoring. Covers best practices for reliable software delivery.',
			duration: '3 weeks',
			image: '/quick-certify/rashi.png'
		}
	];

	// Participants data
	const participants = [
		{
			id: 1,
			name: 'Divanshu Sharma',
			email: 'divanshu@example.com',
			status: 'Completed'
		},
		{
			id: 2,
			name: 'Rashi Gupta',
			email: 'rashi@example.com',
			status: 'In Progress'
		},
		{
			id: 3,
			name: 'Amit Verma',
			email: 'amit.verma@example.com',
			status: 'Invited'
		},
		{
			id: 4,
			name: 'Priya Singh',
			email: 'priya.singh@example.com',
			status: 'Completed'
		},
		{
			id: 5,
			name: 'Rahul Kumar',
			email: 'rahul.k@example.com',
			status: 'In Progress'
		},
		{
			id: 6,
			name: 'Sneha Patel',
			email: 'sneha.patel@example.com',
			status: 'Invited'
		}
	];

	let filteredParticipants = $derived(
		participants.filter(
			(p) =>
				p.name.toLowerCase().includes(searchQuery.toLowerCase()) ||
				p.email.toLowerCase().includes(searchQuery.toLowerCase())
		)
	);
</script>

<Header />
<div class="bg-gray-50 p-4">
	<!-- Breadcrumb Section -->
	<div
		class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 p-4 rounded-sm border border-stroke-dark bg-white border-gray-200">
		<div>
			<nav class="sm:hidden" aria-label="Back">
				<a
					href="/quick-certify/public/pathway"
					class="flex items-center text-sm font-medium text-gray-500 hover:text-gray-700">
					<svg
						class="mr-1 -ml-1 size-5 shrink-0 text-gray-400"
						viewBox="0 0 20 20"
						fill="currentColor"
						aria-hidden="true"
						data-slot="icon">
						<path
							fill-rule="evenodd"
							d="M11.78 5.22a.75.75 0 0 1 0 1.06L8.06 10l3.72 3.72a.75.75 0 1 1-1.06 1.06l-4.25-4.25a.75.75 0 0 1 0-1.06l4.25-4.25a.75.75 0 0 1 1.06 0Z"
							clip-rule="evenodd" />
					</svg>
					Back
				</a>
			</nav>
			<nav class="hidden sm:flex" aria-label="Breadcrumb">
				<ol role="list" class="flex items-center space-x-2">
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
								aria-hidden="true"
								data-slot="icon">
								<path
									fill-rule="evenodd"
									d="M8.22 5.22a.75.75 0 0 1 1.06 0l4.25 4.25a.75.75 0 0 1 0 1.06l-4.25 4.25a.75.75 0 0 1-1.06-1.06L11.94 10 8.22 6.28a.75.75 0 0 1 0-1.06Z"
									clip-rule="evenodd" />
							</svg>
							<a
								href="/quick-certify/public/pathway"
								class="ml-2 text-sm font-medium text-gray-500 hover:text-gray-700 hover:underline"
								>Pathways</a>
						</div>
					</li>
					<li>
						<div class="flex items-center">
							<svg
								class="size-5 shrink-0 text-gray-400"
								viewBox="0 0 20 20"
								fill="currentColor"
								aria-hidden="true"
								data-slot="icon">
								<path
									fill-rule="evenodd"
									d="M8.22 5.22a.75.75 0 0 1 1.06 0l4.25 4.25a.75.75 0 0 1 0 1.06l-4.25 4.25a.75.75 0 0 1-1.06-1.06L11.94 10 8.22 6.28a.75.75 0 0 1 0-1.06Z"
									clip-rule="evenodd" />
							</svg>
							<span class="ml-2 text-sm font-medium text-gray-500">{pathway.name}</span>
						</div>
					</li>
				</ol>
			</nav>
		</div>
		<div class="mt-2 md:flex md:items-center md:justify-between">
			<div class="min-w-0 flex-1">
				<h2 class="text-2xl/7 font-bold text-gray-900 sm:truncate sm:text-3xl sm:tracking-tight">
					{pathway.name}
				</h2>
				<p class="text-gray-500 text-sm mt-1">{pathway.description}</p>
				<div class="flex flex-wrap items-center gap-3 mt-3">
					<span
						class="inline-flex items-center text-xs font-medium px-2 py-0.5 rounded-sm bg-green-100 text-green-800 border border-green-200">
						<div class="w-2 h-2 mr-1.5 bg-green-500 rounded-full"></div>
						{pathway.status}
					</span>
					<span class="text-gray-500 text-sm flex items-center gap-1.5">
						<svg
							class="w-4 h-4"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							stroke-width="2">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M12 6v6h4.5m4.5 0a9 9 0 11-18 0 9 9 0 0118 0z" />
						</svg>
						{pathway.duration}
					</span>
					<span class="text-gray-500 text-sm flex items-center gap-1.5">
						<svg
							class="w-4 h-4"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							stroke-width="2">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M15 19.128a9.38 9.38 0 002.625.372 9.337 9.337 0 004.121-.952 4.125 4.125 0 00-7.533-2.493M15 19.128v-.003c0-1.113-.285-2.16-.786-3.07M15 19.128v.106A12.318 12.318 0 018.624 21c-2.331 0-4.512-.645-6.374-1.766l-.001-.109a6.375 6.375 0 0111.964-3.07M12 6.375a3.375 3.375 0 11-6.75 0 3.375 3.375 0 016.75 0zm8.25 2.25a2.625 2.625 0 11-5.25 0 2.625 2.625 0 015.25 0z" />
						</svg>
						{pathway.participantCount} participants
					</span>
					<span class="text-gray-500 text-sm flex items-center gap-1.5">
						<svg
							class="w-4 h-4"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							stroke-width="2">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5a3.375 3.375 0 00-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12M10.5 2.25H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 00-9-9z" />
						</svg>
						{pathway.credentialCount} credentials
					</span>
				</div>
			</div>
		</div>
	</div>

	<!-- Final Credential Card -->
	<div
		class="max-w-7xl mx-auto p-2 rounded-sm border border-stroke-dark bg-white mt-4 border-gray-200">
		<div class="flex flex-col sm:flex-row">
			<!-- Left: Certificate Image -->
			<div class="sm:w-64 lg:w-80 shrink-0 bg-gray-50 p-4 sm:p-6 flex items-center justify-center">
				<img
					src={finalCredential.image}
					alt="Final Credential Certificate"
					class="rounded-sm w-full max-w-60 object-cover" />
			</div>
			<!-- Right: Details -->
			<div class="flex-1 p-4 sm:p-6 flex flex-col justify-center">
				<div class="flex items-center gap-2 mb-2">
					<span
						class="inline-flex items-center text-xs font-medium px-2 py-0.5 rounded-sm bg-green-100 text-green-800 border border-green-200">
						Final Credential
					</span>
				</div>
				<h2 class="text-lg sm:text-xl font-semibold text-gray-900 mb-2">
					{finalCredential.name}
				</h2>
				<p class="text-sm text-gray-600 mb-4 leading-relaxed">
					{finalCredential.description}
				</p>
			</div>
		</div>
	</div>

	<!-- Tabs Section -->
	<div
		class="max-w-7xl mx-auto px-4 pb-6 rounded-sm border border-stroke-dark bg-white mt-4 border-gray-200 overflow-hidden">
		<!-- Tab Headers -->
		<div class="border-b border-gray-200">
			<ul class="flex -mb-px">
				<li>
					<button
						class="cursor-pointer {activeTab === 'credentials' ? 'selected-tab' : 'unselected-tab'}"
						onclick={() => (activeTab = 'credentials')}>
						Credentials
						<span
							class="ml-1.5 text-xs px-1.5 py-0.5 rounded-sm {activeTab === 'credentials'
								? 'bg-primary-100 text-primary-700'
								: 'bg-gray-100 text-gray-500'}">
							{credentials.length}
						</span>
					</button>
				</li>
				<li>
					<button
						class="cursor-pointer {activeTab === 'participants'
							? 'selected-tab'
							: 'unselected-tab'}"
						onclick={() => (activeTab = 'participants')}>
						Participants
						<span
							class="ml-1.5 text-xs px-1.5 py-0.5 rounded-sm {activeTab === 'participants'
								? 'bg-primary-100 text-primary-700'
								: 'bg-gray-100 text-gray-500'}">
							{participants.length}
						</span>
					</button>
				</li>
			</ul>
		</div>

		<!-- Credentials Tab Content -->
		{#if activeTab === 'credentials'}
			<div class="p-4 sm:p-6">
				<div class="mb-4">
					<h3 class="form-title">Pathway Credentials</h3>
					<p class="form-subtitle">
						Complete these credentials in order to earn the final certification.
					</p>
				</div>

				<!-- Timeline / Stepper -->
				<ol class="relative border-l-2 border-gray-200 ml-4 sm:ml-6">
					{#each credentials as credential, index}
						<li class="mb-0 ml-6 sm:ml-8 {index === credentials.length - 1 ? '' : 'pb-8'}">
							<!-- Step number circle -->
							<span
								class="absolute -left-4 flex items-center justify-center w-7 h-7 rounded-full ring-4 ring-white {expandedIndex ===
								index
									? 'bg-primary-600 text-white'
									: 'bg-gray-100 text-gray-600'}">
								<span class="text-xs font-semibold">{index + 1}</span>
							</span>

							<!-- Credential Card (Accordion) -->
							<div
								class="border border-gray-200 rounded-sm overflow-hidden bg-white hover:shadow-sm transition-shadow">
								<!-- Accordion Header -->
								<button
									type="button"
									class="cursor-pointer w-full text-left px-4 py-3 flex items-center gap-3 sm:gap-4 hover:bg-gray-50"
									onclick={() => toggleAccordion(index)}>
									<!-- Thumbnail -->
									<img
										src={credential.image}
										alt={credential.name}
										class="w-10 h-10 sm:w-12 sm:h-12 rounded-sm object-cover shrink-0 border border-gray-100" />

									<!-- Name & Summary -->
									<div class="flex-1 min-w-0">
										<h4 class="text-sm font-semibold text-gray-900 truncate">
											{credential.name}
										</h4>
										<p class="text-xs text-gray-500 truncate">{credential.summary}</p>
									</div>

									<!-- Duration badge -->
									<span
										class="hidden sm:inline-flex items-center text-xs font-medium px-2 py-0.5 rounded-sm bg-gray-100 text-gray-600 shrink-0">
										{credential.duration}
									</span>

									<!-- Chevron -->
									<svg
										class="w-5 h-5 text-gray-400 shrink-0 transition-transform {expandedIndex ===
										index
											? 'rotate-180'
											: ''}"
										fill="none"
										viewBox="0 0 24 24"
										stroke="currentColor"
										stroke-width="2">
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											d="M19.5 8.25l-7.5 7.5-7.5-7.5" />
									</svg>
								</button>

								<!-- Accordion Body (expanded) -->
								{#if expandedIndex === index}
									<div class="border-t border-gray-200 px-4 py-4 bg-gray-50/50">
										<div class="flex flex-col sm:flex-row gap-4">
											<img
												src={credential.image}
												alt={credential.name}
												class="w-full sm:w-32 h-auto rounded-sm object-cover border border-gray-100" />
											<div class="flex-1">
												<p class="text-sm text-gray-700 leading-relaxed mb-3">
													{credential.description}
												</p>
												<div class="flex flex-wrap items-center gap-3 text-xs text-gray-500">
													<span class="flex items-center gap-1">
														<svg
															class="w-3.5 h-3.5"
															fill="none"
															viewBox="0 0 24 24"
															stroke="currentColor"
															stroke-width="2">
															<path
																stroke-linecap="round"
																stroke-linejoin="round"
																d="M12 6v6h4.5m4.5 0a9 9 0 11-18 0 9 9 0 0118 0z" />
														</svg>
														Duration: {credential.duration}
													</span>
													<span class="flex items-center gap-1">
														<svg
															class="w-3.5 h-3.5"
															fill="none"
															viewBox="0 0 24 24"
															stroke="currentColor"
															stroke-width="2">
															<path
																stroke-linecap="round"
																stroke-linejoin="round"
																d="M9 12h3.75M9 15h3.75M9 18h3.75m3 .75H18a2.25 2.25 0 002.25-2.25V6.108c0-1.135-.845-2.098-1.976-2.192a48.424 48.424 0 00-1.123-.08m-5.801 0c-.065.21-.1.433-.1.664 0 .414.336.75.75.75h4.5a.75.75 0 00.75-.75 2.25 2.25 0 00-.1-.664m-5.8 0A2.251 2.251 0 0113.5 2.25H15c1.012 0 1.867.668 2.15 1.586m-5.8 0c-.376.023-.75.05-1.124.08C9.095 4.01 8.25 4.973 8.25 6.108V8.25m0 0H4.875c-.621 0-1.125.504-1.125 1.125v11.25c0 .621.504 1.125 1.125 1.125h9.75c.621 0 1.125-.504 1.125-1.125V9.375c0-.621-.504-1.125-1.125-1.125H8.25z" />
														</svg>
														Step {index + 1} of {credentials.length}
													</span>
												</div>
											</div>
										</div>
									</div>
								{/if}
							</div>
						</li>
					{/each}
				</ol>
			</div>
		{/if}

		<!-- Participants Tab Content -->
		{#if activeTab === 'participants'}
			<div class="p-4 sm:p-6">
				<!-- Search & Sort -->
				<div class="flex flex-col items-center justify-between md:flex-row md:space-y-0">
					<div class="w-full me-4">
						<form class="flex items-center">
							<label for="participant-search" class="sr-only">Search</label>
							<div class="relative w-full">
								<div class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
									<svg
										aria-hidden="true"
										class="w-5 h-5 text-gray-500 dark:text-gray-400"
										fill="currentColor"
										viewbox="0 0 20 20"
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
									class="block w-full p-1.5 pl-10 text-sm text-gray-900 border border-gray-300 rounded-sm bg-gray-50 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
									placeholder="Search participant by name"
									bind:value={searchQuery} />
							</div>
						</form>
					</div>
					<div
						class="flex flex-col items-stretch justify-end shrink-0 w-full space-y-2 md:w-auto md:flex-row md:space-y-0 md:items-center md:space-x-3">
						<div class="flex items-center w-full space-x-3 md:w-auto">
							<button
								id="participantFilterDropdownButton"
								data-dropdown-toggle="participantFilterDropdown"
								class="flex items-center justify-center w-full px-4 py-1.5 text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-sm md:w-auto focus:outline-none hover:bg-gray-100 hover:text-primary-700 focus:z-10 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700"
								type="button">
								<svg
									xmlns="http://www.w3.org/2000/svg"
									aria-hidden="true"
									class="w-4 h-4 mr-2 text-gray-400"
									viewbox="0 0 20 20"
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
									viewbox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
									aria-hidden="true">
									<path
										clip-rule="evenodd"
										fill-rule="evenodd"
										d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" />
								</svg>
							</button>
							<div
								id="participantFilterDropdown"
								class="z-10 hidden w-48 p-3 bg-white rounded-sm shadow dark:bg-gray-700">
								<ul class="space-y-2 text-sm cursor-pointer" aria-labelledby="dropdownDefault">
									<li class="flex items-center hover:underline cursor-pointer">
										<label class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-100 cursor-pointer">
											Newest First
										</label>
									</li>
									<li class="flex items-center hover:underline cursor-pointer">
										<label class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-100 cursor-pointer">
											Oldest First
										</label>
									</li>
								</ul>
							</div>
						</div>
					</div>
				</div>

				<!-- Participants Grid -->
				<div class="grid grid-cols-1 gap-4 sm:grid-cols-2 lg:grid-cols-3 mt-8">
					{#each filteredParticipants as participant}
						<div
							class="relative flex items-center space-x-3 rounded-sm border border-gray-300 bg-white px-4 py-3 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 hover:border-gray-400">
							<div class="shrink-0">
								<div class="flex items-center justify-center size-10 rounded-full bg-primary-100 text-primary-700 font-semibold text-sm">
									{participant.name.charAt(0)}
								</div>
							</div>
							<div class="min-w-0 flex-1">
								<a href="/quick-certify/public/pathway/1/{participant.id}" class="focus:outline-hidden">
									<span class="absolute inset-0" aria-hidden="true"></span>
									<p class="text-sm font-medium text-gray-900">{participant.name}</p>
									<p class="truncate text-sm text-gray-500">{participant.email}</p>
								</a>
							</div>
						</div>
					{/each}
				</div>

				{#if filteredParticipants.length === 0}
					<div class="px-4 py-8 text-center text-sm text-gray-500">
						No participants found matching your search.
					</div>
				{/if}

				<!-- Pagination -->
				<div class="relative overflow-hidden bg-white mt-8">
					<nav
						class="flex flex-col items-start justify-end p-4 space-y-3 md:flex-row md:items-center md:space-y-0"
						aria-label="Table navigation">
						<span class="text-sm font-normal text-gray-500 dark:text-gray-400"
							>Showing <span class="font-semibold text-gray-900 dark:text-white">1-6</span> of
							<span class="font-semibold text-gray-900 dark:text-white me-8">6</span></span>
						<ul class="inline-flex items-stretch -space-x-px">
							<li>
								<a
									href="#"
									class="flex items-center justify-center h-full py-1.5 px-3 ml-0 text-gray-500 bg-white rounded-l-lg border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white">
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
									class="z-10 flex items-center justify-center px-3 py-2 text-sm leading-tight border text-primary-600 bg-primary-50 border-primary-300 hover:bg-primary-100 hover:text-primary-700 dark:border-gray-700 dark:bg-gray-700 dark:text-white"
									>1</a>
							</li>
							<li>
								<a
									href="#"
									class="flex items-center justify-center h-full py-1.5 px-3 leading-tight text-gray-500 bg-white rounded-r-lg border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white">
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
		{/if}
	</div>
</div>
<Footer />
