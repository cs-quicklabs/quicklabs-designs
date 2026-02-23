<script>
	import Header from '$quick-certify/common/navbar/header.svelte';
	import Footer from '$quick-certify/common/navbar/footer.svelte';

	// Pathway data
	const pathway = {
		name: 'Full Stack Developer',
		credentialCount: 5
	};

	// Participant data
	const participant = {
		name: 'Rashi Gupta',
		email: 'rashi@example.com',
		joinedDate: 'Jan 15, 2025',
		status: 'In Progress'
	};

	// Credentials with earned/not earned status for this participant
	const credentials = [
		{
			id: 1,
			name: 'React Basics',
			summary: 'Learn the fundamentals of React including components, state, and props.',
			duration: '4 weeks',
			status: 'earned',
			earnedDate: 'Feb 10, 2025',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 2,
			name: 'Node.js Fundamentals',
			summary: 'Build server-side applications with Node.js and Express.',
			duration: '4 weeks',
			status: 'earned',
			earnedDate: 'Mar 8, 2025',
			image: '/quick-certify/rashi.png'
		},
		{
			id: 3,
			name: 'MongoDB Essentials',
			summary: 'Master NoSQL database design and operations with MongoDB.',
			duration: '3 weeks',
			status: 'not_earned',
			earnedDate: null,
			image: '/quick-certify/rashi.png'
		},
		{
			id: 4,
			name: 'Docker & Kubernetes',
			summary: 'Containerize and orchestrate applications for modern deployment.',
			duration: '5 weeks',
			status: 'not_earned',
			earnedDate: null,
			image: '/quick-certify/rashi.png'
		},
		{
			id: 5,
			name: 'CI/CD Pipelines',
			summary: 'Automate testing and deployment with continuous integration workflows.',
			duration: '3 weeks',
			status: 'not_earned',
			earnedDate: null,
			image: '/quick-certify/rashi.png'
		}
	];

	// Calculate stats
	const earnedCount = credentials.filter((c) => c.status === 'earned').length;
	const notEarnedCount = credentials.filter((c) => c.status === 'not_earned').length;
	const totalCount = credentials.length;
	const completionPercentage = Math.round((earnedCount / totalCount) * 100);

	// SVG Pie chart calculations
	const radius = 50;
	const circumference = 2 * Math.PI * radius;

	const earnedAngle = (earnedCount / totalCount) * circumference;
	const notEarnedAngle = (notEarnedCount / totalCount) * circumference;

	function getStatusBadge(status) {
		if (status === 'earned')
			return {
				text: 'Earned',
				classes: 'bg-green-100 text-green-800 border-green-200',
				dotClass: 'bg-green-500'
			};
		return {
			text: 'Not Earned',
			classes: 'bg-gray-100 text-gray-600 border-gray-200',
			dotClass: 'bg-gray-400'
		};
	}
</script>

<Header />
<div class="bg-gray-50 p-4">
	<!-- Breadcrumb Section -->
	<div
		class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 p-4 rounded-sm border border-stroke-dark bg-white border-gray-200">
		<div>
			<nav class="sm:hidden" aria-label="Back">
				<a
					href="/quick-certify/public/pathway/1"
					class="flex items-center text-sm font-medium text-gray-500 hover:text-gray-700">
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
								aria-hidden="true">
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
								aria-hidden="true">
								<path
									fill-rule="evenodd"
									d="M8.22 5.22a.75.75 0 0 1 1.06 0l4.25 4.25a.75.75 0 0 1 0 1.06l-4.25 4.25a.75.75 0 0 1-1.06-1.06L11.94 10 8.22 6.28a.75.75 0 0 1 0-1.06Z"
									clip-rule="evenodd" />
							</svg>
							<a
								href="/quick-certify/public/pathway/1"
								class="ml-2 text-sm font-medium text-gray-500 hover:text-gray-700 hover:underline"
								>{pathway.name}</a>
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
							<span class="ml-2 text-sm font-medium text-gray-500">{participant.name}</span>
						</div>
					</li>
				</ol>
			</nav>
		</div>
		<div class="mt-2 md:flex md:items-center md:justify-between">
			<div class="min-w-0 flex-1">
				<h2 class="text-2xl/7 font-bold text-gray-900 sm:truncate sm:text-3xl sm:tracking-tight">
					{participant.name}
				</h2>
				<p class="text-gray-500 text-sm mt-1">{participant.email}</p>
				<div class="flex flex-wrap items-center gap-3 mt-3">
					<span
						class="inline-flex items-center text-xs font-medium px-2 py-0.5 rounded-sm {participant.status ===
						'Completed'
							? 'bg-green-100 text-green-800 border border-green-200'
							: participant.status === 'In Progress'
								? 'bg-blue-100 text-blue-800 border border-blue-200'
								: 'bg-yellow-100 text-yellow-800 border border-yellow-200'}">
						<div
							class="w-3 h-3 mr-1.5 rounded-full {participant.status === 'Completed'
								? 'bg-green-500'
								: participant.status === 'In Progress'
									? 'bg-blue-500'
									: 'bg-yellow-500'}">
						</div>
						{participant.status}
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
								d="M6.75 3v2.25M17.25 3v2.25M3 18.75V7.5a2.25 2.25 0 012.25-2.25h13.5A2.25 2.25 0 0121 7.5v11.25m-18 0A2.25 2.25 0 005.25 21h13.5A2.25 2.25 0 0021 18.75m-18 0v-7.5A2.25 2.25 0 015.25 9h13.5A2.25 2.25 0 0121 11.25v7.5" />
						</svg>
						Joined {participant.joinedDate}
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
						{pathway.name}
					</span>
				</div>
			</div>
		</div>
	</div>

	<!-- Overview Stats with Pie Chart -->
	<div class="max-w-7xl mx-auto rounded-sm border border-stroke-dark bg-white mt-4 border-gray-200">
		<div class="p-4 sm:p-6">
			<h3 class="form-title mb-4">Pathway Progress</h3>
			<div class="flex flex-col md:flex-row items-center gap-8">
				<!-- Pie Chart -->
				<div class="relative shrink-0">
					<svg width="160" height="160" viewBox="0 0 120 120" class="transform -rotate-90">
						<!-- Not Earned (gray background) -->
						<circle cx="60" cy="60" r={radius} fill="none" stroke="#d1d5db" stroke-width="16" />
						<!-- Earned (green overlay) -->
						<circle
							cx="60"
							cy="60"
							r={radius}
							fill="none"
							stroke="#22c55e"
							stroke-width="16"
							stroke-dasharray="{earnedAngle} {circumference - earnedAngle}"
							stroke-dashoffset="0" />
					</svg>
					<!-- Center text -->
					<div class="absolute inset-0 flex flex-col items-center justify-center">
						<span class="text-2xl font-bold text-gray-900">{completionPercentage}%</span>
						<span class="text-xs text-gray-500">Complete</span>
					</div>
				</div>

				<!-- Stats Grid -->
				<div class="flex-1 grid grid-cols-1 sm:grid-cols-2 gap-4 w-full">
					<div class="bg-green-50 rounded-sm p-4 border border-green-100">
						<div class="flex items-center gap-2 mb-1">
							<div class="w-3 h-3 rounded-full bg-green-500"></div>
							<span class="text-sm font-medium text-green-800">Earned</span>
						</div>
						<p class="text-2xl font-bold text-green-900">{earnedCount}</p>
						<p class="text-xs text-green-600">of {totalCount} credentials</p>
					</div>
					<div class="bg-gray-50 rounded-sm p-4 border border-gray-200">
						<div class="flex items-center gap-2 mb-1">
							<div class="w-3 h-3 rounded-full bg-gray-400"></div>
							<span class="text-sm font-medium text-gray-700">Not Earned</span>
						</div>
						<p class="text-2xl font-bold text-gray-900">{notEarnedCount}</p>
						<p class="text-xs text-gray-500">of {totalCount} credentials</p>
					</div>
				</div>
			</div>

			<!-- Overall progress bar -->
			<div class="mt-6">
				<div class="flex items-center justify-between mb-1.5">
					<span class="text-sm font-medium text-gray-700">Overall Progress</span>
					<span class="text-sm font-medium text-gray-700"
						>{earnedCount}/{totalCount} credentials</span>
				</div>
				<div class="w-full bg-gray-200 rounded-full h-2.5">
					<div
						class="bg-green-500 h-2.5 rounded-full transition-all"
						style="width: {completionPercentage}%">
					</div>
				</div>
			</div>
		</div>
	</div>

	<!-- Credentials Timeline -->
	<div
		class="max-w-7xl mx-auto px-4 pb-6 rounded-sm border border-stroke-dark bg-white mt-4 border-gray-200">
		<div class="p-4 sm:p-6">
			<div class="mb-4">
				<h3 class="form-title">Credential Progress</h3>
				<p class="form-subtitle">Track completion status for each credential in this pathway.</p>
			</div>

			<!-- Timeline -->
			<ol class="relative border-l-2 border-gray-200 ml-4 sm:ml-6">
				{#each credentials as credential, index}
					{@const badge = getStatusBadge(credential.status)}
					<li class="mb-0 ml-6 sm:ml-8 {index === credentials.length - 1 ? '' : 'pb-8'}">
						<!-- Step number circle -->
						<span
							class="absolute -left-4 flex items-center justify-center w-7 h-7 rounded-full ring-4 ring-white {credential.status ===
							'earned'
								? 'bg-green-500 text-white'
								: 'bg-gray-100 text-gray-600'}">
							{#if credential.status === 'earned'}
								<svg
									class="w-3.5 h-3.5"
									fill="none"
									viewBox="0 0 24 24"
									stroke="currentColor"
									stroke-width="3">
									<path stroke-linecap="round" stroke-linejoin="round" d="M4.5 12.75l6 6 9-13.5" />
								</svg>
							{:else}
								<span class="text-xs font-semibold">{index + 1}</span>
							{/if}
						</span>

						<!-- Credential Card -->
						<div
							class="border border-gray-200 rounded-sm overflow-hidden bg-white hover:shadow-sm transition-shadow">
							<div class="w-full text-left px-4 py-3 flex items-center gap-3 sm:gap-4">
								<!-- Thumbnail -->
								<img
									src={credential.image}
									alt={credential.name}
									class="w-10 h-10 sm:w-12 sm:h-12 rounded-sm object-cover shrink-0 border border-gray-100" />

								<!-- Name & Summary -->
								<div class="flex-1 min-w-0">
									<div class="flex items-center gap-2 mb-0.5">
										<h4 class="text-sm font-semibold text-gray-900 truncate">
											{credential.name}
										</h4>
										<span
											class="inline-flex items-center text-xs font-medium px-2 py-0.5 rounded-sm border {badge.classes}">
											<div class="w-2 h-2 mr-1.5 rounded-full {badge.dotClass}"></div>
											{badge.text}
										</span>
									</div>
									<p class="text-xs text-gray-500 truncate">{credential.summary}</p>
									{#if credential.earnedDate}
										<p class="text-xs text-green-600 mt-1 flex items-center gap-1">
											<svg
												class="w-3 h-3"
												fill="none"
												viewBox="0 0 24 24"
												stroke="currentColor"
												stroke-width="2">
												<path
													stroke-linecap="round"
													stroke-linejoin="round"
													d="M9 12.75L11.25 15 15 9.75M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
											</svg>
											Earned on {credential.earnedDate}
										</p>
									{/if}
								</div>

								<!-- Duration badge -->
								<span
									class="hidden sm:inline-flex items-center text-xs font-medium px-2 py-0.5 rounded-sm bg-gray-100 text-gray-600 shrink-0">
									{credential.duration}
								</span>
							</div>
						</div>
					</li>
				{/each}
			</ol>
		</div>
	</div>
</div>
<Footer />
