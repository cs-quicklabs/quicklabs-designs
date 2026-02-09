<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';
	import Pagination from '$quick-certify/common/navbar/pagination.svelte';

	const maxVisibleCredentials = 2;

	const pathways = [
		{
			id: 1,
			name: 'Full Stack Developer',
			credentials: ['React Basics', 'Node.js Fundamentals', 'MongoDB Essentials'],
			participants: 124,
			duration: '6 months',
			status: 'Active'
		},
		{
			id: 2,
			name: 'Data Science Professional',
			credentials: ['Python for Data Science', 'Machine Learning'],
			participants: 89,
			duration: '4 months',
			status: 'Active'
		},
		{
			id: 3,
			name: 'Cloud Architecture',
			credentials: ['AWS Foundations', 'Azure Basics', 'Docker & K8s', 'CI/CD Pipelines'],
			participants: 0,
			duration: '',
			status: 'Draft'
		},
		{
			id: 4,
			name: 'UI/UX Design',
			credentials: ['Design Thinking', 'Figma Mastery'],
			participants: 210,
			duration: '3 months',
			status: 'Active'
		},
		{
			id: 5,
			name: 'Cybersecurity Analyst',
			credentials: ['Network Security', 'Ethical Hacking', 'Incident Response'],
			participants: 45,
			duration: '5 months',
			status: 'Archived'
		}
	];
</script>

<NavBar />

<section class="bg-gray-50 dark:bg-gray-900 py-3 sm:py-5 min-h-screen">
	<div class="px-4 mx-auto max-w-screen-2xl lg:px-8">
		<div class="relative overflow-hidden bg-white shadow-md dark:bg-gray-800 sm:rounded-sm">
			<div class="divide-y dark:divide-gray-700">
				<!-- Header -->
				<div class="p-4 space-y-3 sm:space-y-0 sm:flex sm:items-center sm:justify-between">
					<div>
						<h1 class="mr-3 form-title">Pathways</h1>
						<p class="form-subtitle">
							Manage all your existing <span class="font-bold">{pathways.length}</span> pathways or create
							a new one.
						</p>
					</div>
					<div class="flex flex-col sm:flex-row gap-3 sm:items-center">
						<input
							type="text"
							placeholder="Search pathways..."
							class="w-full sm:w-2xs px-3 py-2 text-sm border border-gray-200 rounded-md bg-gray-50 focus:ring-1 focus:ring-gray-300 focus:outline-none" />
						<a href="/quick-certify/pathways/add" class="btn-primary whitespace-nowrap text-center">
							Create Pathway
						</a>
					</div>
				</div>
			</div>

			<!-- Filters -->
			<div
				class="flex flex-wrap items-center pt-1 pb-4 border-t border-b border-gray-200 dark:border-gray-200 px-4 gap-x-4 gap-y-3">
				<div
					class="items-center hidden mt-3 mr-0 text-sm font-medium text-gray-900 md:flex dark:text-white">
					Show records only for:
				</div>
				<div class="flex flex-wrap flex-1">
					<a href="">
						<div class="flex items-center mt-3 mr-4">
							<input
								id="filter-all"
								type="radio"
								value=""
								name="show-only"
								class="w-4 h-4 bg-gray-100 border-gray-300 text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600 cursor-pointer"
								checked />
							<label
								for="filter-all"
								class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
								Active
							</label>
						</div>
					</a>
					<a href="">
						<div class="flex items-center mt-3 mr-4">
							<input
								id="filter-draft"
								type="radio"
								value=""
								name="show-only"
								class="w-4 h-4 bg-gray-100 border-gray-300 text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600 cursor-pointer" />
							<label
								for="filter-draft"
								class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
								Draft
							</label>
						</div>
					</a>
					<a href="">
						<div class="flex items-center mt-3 mr-4">
							<input
								id="filter-archived"
								type="radio"
								value=""
								name="show-only"
								class="w-4 h-4 bg-gray-100 border-gray-300 text-primary-600 focus:ring-primary-500 dark:focus:ring-primary-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600 cursor-pointer" />
							<label
								for="filter-archived"
								class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">
								Archived
							</label>
						</div>
					</a>
					<a
						href=""
						class="underline mt-3 mr-4 font-medium text-blue-600 dark:text-blue-500 hover:underline text-sm"
						>Show All</a>
				</div>
			</div>

			<!-- Desktop Table -->
			<div class="hidden sm:block overflow-x-auto">
				<table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
					<thead
						class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
						<tr>
							<th scope="col" class="px-4 py-3">Name</th>
							<th scope="col" class="px-4 py-3">Credentials</th>
							<th scope="col" class="px-4 py-3">Participants</th>
							<th scope="col" class="px-4 py-3">Duration</th>
							<th scope="col" class="px-4 py-3">Status</th>
						</tr>
					</thead>
					<tbody>
						{#each pathways as pathway}
							<tr
								class="border-b border-gray-200 dark:border-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">
								<th scope="row" class="px-4 py-2 form-text-normal">
									<div class="flex items-center">
										<a
											href="/quick-certify/pathways/{pathway.id}"
											class="hover:underline font-semibold text-gray-900">
											{pathway.name}
										</a>
									</div>
								</th>
								<td class="px-4 py-2">
									<div class="flex flex-wrap gap-1">
										{#each pathway.credentials.slice(0, maxVisibleCredentials) as credential}
											<span
												class="inline-flex items-center text-xs font-medium px-1.5 py-0.5 rounded bg-primary-100 text-primary-800 dark:bg-primary-900 dark:text-primary-300">
												{credential}
											</span>
										{/each}
										{#if pathway.credentials.length > maxVisibleCredentials}
											<span
												class="inline-flex items-center text-xs font-medium px-1.5 py-0.5 rounded bg-gray-100 text-gray-600 dark:bg-gray-700 dark:text-gray-300 cursor-default"
												title={pathway.credentials.slice(maxVisibleCredentials).join(', ')}>
												+{pathway.credentials.length - maxVisibleCredentials}
											</span>
										{/if}
									</div>
								</td>
								<td class="px-4 py-2 form-text-normal">{pathway.participants || '-'}</td>
								<td class="px-4 py-2 form-text-normal">{pathway.duration || '-'}</td>
								<td class="px-4 py-2 form-text-normal">
									<div class="flex items-center">
										{#if pathway.status === 'Active'}
											<div class="w-3 h-3 mr-2 bg-green-500 border border-buffer rounded-full">
											</div>
										{:else if pathway.status === 'Draft'}
											<div class="w-3 h-3 mr-2 bg-yellow-400 border border-buffer rounded-full">
											</div>
										{:else}
											<div class="w-3 h-3 mr-2 bg-gray-400 border border-buffer rounded-full"></div>
										{/if}
										{pathway.status}
									</div>
								</td>
							</tr>
						{/each}
					</tbody>
				</table>
			</div>

			<!-- Mobile Card Layout -->
			<div class="sm:hidden divide-y divide-gray-200 dark:divide-gray-700">
				{#each pathways as pathway}
					<a
						href="/quick-certify/pathways/{pathway.id}"
						class="block px-4 py-3 hover:bg-gray-50 dark:hover:bg-gray-700">
						<div class="flex items-center justify-between mb-2">
							<span class="font-semibold text-sm text-gray-900 dark:text-white">
								{pathway.name}
							</span>
							<div class="flex items-center text-xs">
								{#if pathway.status === 'Active'}
									<div class="w-2 h-2 mr-1.5 bg-green-500 rounded-full"></div>
								{:else if pathway.status === 'Draft'}
									<div class="w-2 h-2 mr-1.5 bg-yellow-400 rounded-full"></div>
								{:else}
									<div class="w-2 h-2 mr-1.5 bg-gray-400 rounded-full"></div>
								{/if}
								<span class="text-gray-500">{pathway.status}</span>
							</div>
						</div>
						<div class="flex flex-wrap gap-1 mb-2">
							{#each pathway.credentials.slice(0, maxVisibleCredentials) as credential}
								<span
									class="inline-flex items-center text-xs font-medium px-1.5 py-0.5 rounded bg-primary-100 text-primary-800 dark:bg-primary-900 dark:text-primary-300">
									{credential}
								</span>
							{/each}
							{#if pathway.credentials.length > maxVisibleCredentials}
								<span
									class="inline-flex items-center text-xs font-medium px-1.5 py-0.5 rounded bg-gray-100 text-gray-600 dark:bg-gray-700 dark:text-gray-300">
									+{pathway.credentials.length - maxVisibleCredentials}
								</span>
							{/if}
						</div>
						<div class="flex items-center gap-4 text-xs text-gray-500">
							<span>{pathway.participants || '-'} participants</span>
							<span>{pathway.duration || '- Durations'}</span>
						</div>
					</a>
				{/each}
			</div>

			<Pagination />
		</div>
	</div>
</section>
