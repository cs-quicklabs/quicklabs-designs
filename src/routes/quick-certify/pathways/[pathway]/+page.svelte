<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';
	import Pagination from '$quick-certify/common/navbar/pagination.svelte';

	let activeTab = $state('credentials');
	let showModal = $state(false);
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

<svelte:window
	onclick={(e) => {
		if (showModal && e.target.closest('.modal-backdrop') && !e.target.closest('.modal-content')) {
			showModal = false;
		}
	}} />

<NavBar />

<main>
	<!-- Banner Section (company-style) -->
	<div class="bg-gray-50 dark:bg-gray-900">
		<div class="px-4 mx-auto max-w-screen-2xl lg:px-8 pt-4">
			<div class="rounded-sm border border-gray-200 bg-white overflow-hidden">
				<div class="relative">
					<img
						class="h-32 w-full object-cover lg:h-48"
						src="https://images.unsplash.com/photo-1444628838545-ac4016a5418a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80"
						alt="Pathway Banner" />
				</div>

				<!-- Title block -->
				<div class="px-4 sm:px-6 py-4">
					<div class="flex flex-col sm:flex-row sm:items-start sm:justify-between gap-3">
						<div>
							<h1 class="text-2xl font-bold text-gray-900 sm:text-3xl sm:tracking-tight">
								{pathway.name}
							</h1>
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
						<a href="/quick-certify/pathways/edit" class="btn-secondary shrink-0">
							<svg
								class="w-4 h-4 mr-1.5"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
								stroke-width="2">
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									d="M16.862 4.487l1.687-1.688a1.875 1.875 0 112.652 2.652L10.582 16.07a4.5 4.5 0 01-1.897 1.13L6 18l.8-2.685a4.5 4.5 0 011.13-1.897l8.932-8.931z" />
							</svg>
							Edit
						</a>
					</div>
				</div>
			</div>
		</div>
	</div>

	<!-- Final Credential Card -->
	<div class="px-4 mx-auto max-w-screen-2xl lg:px-8 mt-4 mb-6">
		<div class="bg-white rounded-sm shadow-md border border-gray-200 overflow-hidden">
			<div class="flex flex-col sm:flex-row">
				<!-- Left: Certificate Image -->
				<div
					class="sm:w-64 lg:w-80 shrink-0 bg-gray-50 p-4 sm:p-6 flex items-center justify-center">
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
					<div class="flex flex-wrap gap-2">
						<button class="btn-primary text-sm">
							<span class="flex items-center gap-1.5">
								<svg
									class="w-4 h-4"
									fill="none"
									viewBox="0 0 24 24"
									stroke="currentColor"
									stroke-width="2">
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										d="M2.036 12.322a1.012 1.012 0 010-.639C3.423 7.51 7.36 4.5 12 4.5c4.638 0 8.573 3.007 9.963 7.178.07.207.07.431 0 .639C20.577 16.49 16.64 19.5 12 19.5c-4.638 0-8.573-3.007-9.963-7.178z" />
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
								</svg>
								View Credential
							</span>
						</button>
					</div>
				</div>
			</div>
		</div>
	</div>

	<!-- Tabs Section -->
	<div class="px-4 mx-auto max-w-screen-2xl lg:px-8 mb-8">
		<div class="bg-white shadow-md rounded-sm border border-gray-200 overflow-hidden">
			<!-- Tab Headers -->
			<div class="border-b border-gray-200">
				<ul class="flex -mb-px">
					<li>
						<button
							class="cursor-pointer {activeTab === 'credentials'
								? 'selected-tab'
								: 'unselected-tab'}"
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
													<div class="mt-3">
														<a
															href="/quick-certify/credential/{credential.id}"
															class="btn-inline-blue text-xs">
															View credential details →
														</a>
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
					<!-- Header & Search -->
					<div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-3 mb-4">
						<div>
							<h3 class="form-title">Participants</h3>
							<p class="form-subtitle">{participants.length} total participants</p>
						</div>
						<div class="flex items-center gap-3">
							<input
								type="text"
								placeholder="Search by name or email..."
								class="form-input-field w-full sm:w-56"
								bind:value={searchQuery} />
							<!-- Sort dropdown -->
							<details class="relative">
								<summary
									class="cursor-pointer flex items-center gap-2 px-3 py-1.5 text-sm border border-gray-200 rounded-sm bg-gray-50 hover:bg-gray-100 list-none">
									<svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
										<path
											stroke-width="2"
											stroke-linecap="round"
											stroke-linejoin="round"
											d="M3 7.5L7.5 3m0 0L12 7.5M7.5 3v13.5m13.5-3L16.5 18m0 0L12 13.5m4.5 4.5V4.5" />
									</svg>
									<span class="hidden sm:inline">Sort</span>
								</summary>
								<div
									class="absolute right-0 z-10 mt-2 w-40 bg-white border border-gray-200 rounded-sm shadow p-1">
									<button
										class="w-full text-left px-3 py-1.5 text-sm text-gray-700 hover:bg-gray-100 rounded-sm cursor-pointer"
										>A - Z</button>
									<button
										class="w-full text-left px-3 py-1.5 text-sm text-gray-700 hover:bg-gray-100 rounded-sm cursor-pointer"
										>Z - A</button>
									<button
										class="w-full text-left px-3 py-1.5 text-sm text-gray-700 hover:bg-gray-100 rounded-sm cursor-pointer"
										>Newest</button>
									<button
										class="w-full text-left px-3 py-1.5 text-sm text-gray-700 hover:bg-gray-100 rounded-sm cursor-pointer"
										>Oldest</button>
								</div>
							</details>
							<!-- Add Participant button -->
							<button class="btn-primary whitespace-nowrap" onclick={() => (showModal = true)}>
								Add Participant
							</button>
						</div>
					</div>

					<!-- Desktop Table -->
					<div class="hidden sm:block border border-gray-200 rounded-sm overflow-hidden">
						<table class="w-full text-sm text-left text-gray-700">
							<thead class="bg-gray-50 border-b border-gray-200">
								<tr>
									<th class="px-4 py-3 font-medium text-xs uppercase text-gray-500">Name</th>
									<th class="px-4 py-3 font-medium text-xs uppercase text-gray-500">Email</th>
									<th class="px-4 py-3 font-medium text-xs uppercase text-gray-500">Status</th>
									<th class="px-4 py-3 font-medium text-xs uppercase text-gray-500">Action</th>
								</tr>
							</thead>
							<tbody class="divide-y divide-gray-200">
								{#each filteredParticipants as participant}
									<tr class="hover:bg-gray-50">
										<td class="px-4 py-2.5">
											<span class="font-medium text-gray-900">{participant.name}</span>
										</td>
										<td class="px-4 py-2.5 text-gray-500">{participant.email}</td>
										<td class="px-4 py-2.5">
											{#if participant.status === 'Completed'}
												<span
													class="inline-flex items-center text-xs font-medium px-2 py-0.5 rounded-sm bg-green-100 text-green-800">
													{participant.status}
												</span>
											{:else if participant.status === 'In Progress'}
												<span
													class="inline-flex items-center text-xs font-medium px-2 py-0.5 rounded-sm bg-blue-100 text-blue-800">
													{participant.status}
												</span>
											{:else}
												<span
													class="inline-flex items-center text-xs font-medium px-2 py-0.5 rounded-sm bg-yellow-100 text-yellow-800">
													{participant.status}
												</span>
											{/if}
										</td>
										<td class="px-4 py-2.5">
											<a href="#" class="btn-inline-blue text-xs">View</a>
										</td>
									</tr>
								{/each}
								{#if filteredParticipants.length === 0}
									<tr>
										<td colspan="4" class="px-4 py-8 text-center text-sm text-gray-500">
											No participants found matching your search.
										</td>
									</tr>
								{/if}
							</tbody>
						</table>
					</div>

					<!-- Mobile Card Layout -->
					<div
						class="sm:hidden divide-y divide-gray-200 border border-gray-200 rounded-sm overflow-hidden">
						{#each filteredParticipants as participant}
							<div class="px-4 py-3 bg-white hover:bg-gray-50">
								<div class="flex items-center justify-between mb-1">
									<span class="font-medium text-sm text-gray-900">{participant.name}</span>
									{#if participant.status === 'Completed'}
										<span
											class="text-xs font-medium px-2 py-0.5 rounded-sm bg-green-100 text-green-800">
											{participant.status}
										</span>
									{:else if participant.status === 'In Progress'}
										<span
											class="text-xs font-medium px-2 py-0.5 rounded-sm bg-blue-100 text-blue-800">
											{participant.status}
										</span>
									{:else}
										<span
											class="text-xs font-medium px-2 py-0.5 rounded-sm bg-yellow-100 text-yellow-800">
											{participant.status}
										</span>
									{/if}
								</div>
								<p class="text-xs text-gray-500">{participant.email}</p>
							</div>
						{/each}
						{#if filteredParticipants.length === 0}
							<div class="px-4 py-8 text-center text-sm text-gray-500">
								No participants found matching your search.
							</div>
						{/if}
					</div>

					<Pagination />
				</div>
			{/if}
		</div>
	</div>
</main>

<!-- Add Participant Modal -->
{#if showModal}
	<div
		class="modal-backdrop fixed inset-0 z-50 flex items-center justify-center bg-black/50 backdrop-blur-sm p-4">
		<div class="modal-content relative w-full max-w-md bg-white rounded-sm shadow-lg">
			<!-- Modal Header -->
			<div class="flex items-center justify-between p-4 border-b border-gray-200">
				<h3 class="text-lg font-semibold text-gray-900">Add Participant</h3>
				<button
					class="cursor-pointer p-1 rounded-sm hover:bg-gray-100"
					onclick={() => (showModal = false)}>
					<svg
						class="w-4 h-4 text-gray-500"
						fill="none"
						viewBox="0 0 14 14"
						stroke="currentColor"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round">
						<path d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6" />
					</svg>
				</button>
			</div>

			<!-- Modal Body -->
			<form class="p-4 space-y-4">
				<div>
					<label for="participant-name" class="form-input-label">
						Name <span class="text-red-500">*</span>
					</label>
					<input
						id="participant-name"
						type="text"
						required
						class="form-input-field w-full"
						placeholder="Enter full name" />
				</div>

				<div>
					<label for="participant-email" class="form-input-label">
						Email <span class="text-red-500">*</span>
					</label>
					<input
						id="participant-email"
						type="email"
						required
						class="form-input-field w-full"
						placeholder="name@company.com" />
					<p class="form-input-description">An invitation will be sent to this email address.</p>
				</div>

				<!-- Modal Actions -->
				<div class="flex items-center justify-between pt-2">
					<button type="submit" class="btn-primary"> Send Invite </button>
					<button type="button" class="btn-secondary" onclick={() => (showModal = false)}>
						Cancel
					</button>
				</div>
			</form>
		</div>
	</div>
{/if}
