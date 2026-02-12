<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';

	let searchQuery = $state('');
	let dropdownOpen = $state(false);

	const availableCredentials = [
		{ id: 1, name: 'React Basics' },
		{ id: 2, name: 'Node.js Fundamentals' },
		{ id: 3, name: 'MongoDB Essentials' },
		{ id: 4, name: 'Python for Data Science' },
		{ id: 5, name: 'Machine Learning' },
		{ id: 6, name: 'AWS Foundations' },
		{ id: 7, name: 'Azure Basics' },
		{ id: 8, name: 'Docker & Kubernetes' },
		{ id: 9, name: 'CI/CD Pipelines' },
		{ id: 10, name: 'Design Thinking' },
		{ id: 11, name: 'Figma Mastery' },
		{ id: 12, name: 'Network Security' },
		{ id: 13, name: 'Ethical Hacking' },
		{ id: 14, name: 'Incident Response' }
	];

	let selectedCredentials = $state([
		{ id: 1, name: 'React Basics', isFinal: false },
		{ id: 2, name: 'Node.js Fundamentals', isFinal: false },
		{ id: 3, name: 'MongoDB Essentials', isFinal: true }
	]);

	let filteredCredentials = $derived(
		availableCredentials.filter(
			(c) =>
				c.name.toLowerCase().includes(searchQuery.toLowerCase()) &&
				!selectedCredentials.some((s) => s.id === c.id)
		)
	);

	function addCredential(credential) {
		selectedCredentials = [...selectedCredentials, { ...credential, isFinal: false }];
		searchQuery = '';
		dropdownOpen = false;
	}

	function removeCredential(id) {
		selectedCredentials = selectedCredentials.filter((c) => c.id !== id);
	}

	function toggleFinal(index) {
		selectedCredentials = selectedCredentials.map((c, i) =>
			i === index ? { ...c, isFinal: !c.isFinal } : c
		);
	}
</script>

<svelte:window
	onclick={(e) => {
		if (!e.target.closest('.credential-search-wrapper')) {
			dropdownOpen = false;
		}
	}} />

<NavBar />

<main>
	<section class="min-h-screen">
		<div class="py-6 px-4 mx-auto max-w-2xl lg:py-8">
			<!-- Heading -->
			<div class="mb-6">
				<h1 class="form-title">Create New Pathway</h1>
				<p class="form-subtitle">
					Define a learning pathway by adding credentials in the order they should be completed.
				</p>
			</div>

			<form action="/quick-certify/pathways" method="GET">
				<!-- Name -->
				<div class="mb-4">
					<label for="pathway-name" class="form-input-label">Name</label>
					<input
						id="pathway-name"
						type="text"
						class="form-input-field w-full"
						placeholder="e.g. Full Stack Developer" />
					<p class="form-input-description">Give your pathway a clear, descriptive name.</p>
				</div>

				<!-- Description -->
				<div class="mb-6">
					<label for="pathway-description" class="form-input-label">Description</label>
					<textarea
						id="pathway-description"
						rows="3"
						class="form-input-field w-full"
						placeholder="Describe what this pathway covers and who it's for..."></textarea>
					<p class="form-input-description">
						Briefly explain the purpose and goals of this pathway.
					</p>
				</div>

				<!-- Banner Image -->
				<div class="mb-6">
					<label for="banner-upload" class="form-input-label">Banner Image</label>
					<p class="form-input-description -mt-1 mb-2">
						Upload a banner image for this pathway.
					</p>
					<label
						for="banner-upload"
						class="flex flex-col justify-center items-center w-full h-40 bg-gray-50 rounded-sm border-2 border-gray-300 border-dashed cursor-pointer hover:bg-gray-100 dark:bg-gray-700 dark:border-gray-600 dark:hover:border-gray-500 dark:hover:bg-gray-600">
						<div class="flex flex-col justify-center items-center pt-5 pb-6">
							<svg
								aria-hidden="true"
								class="mb-3 w-10 h-10 text-gray-400"
								fill="none"
								stroke="currentColor"
								viewBox="0 0 24 24"
								xmlns="http://www.w3.org/2000/svg">
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12" />
							</svg>
							<p class="mb-2 text-sm text-gray-500 dark:text-gray-400">
								<span class="font-semibold">Click to upload</span> or drag and drop
							</p>
							<p class="text-xs text-gray-500 dark:text-gray-400">PNG, JPG or SVG (1920x300)</p>
						</div>
						<input id="banner-upload" type="file" class="hidden" accept="image/*" />
					</label>
				</div>

				<!-- Credentials Search & Dropdown -->
				<div class="mb-2">
					<label for="credential-search" class="form-input-label">Credentials</label>
					<p class="form-input-description -mt-1 mb-2">
						Search and add credentials to this pathway. Drag to reorder.
					</p>
				</div>

				<div class="relative credential-search-wrapper mb-4">
					<div class="relative">
						<input
							id="credential-search"
							type="text"
							class="form-input-field w-full"
							placeholder="Search credentials to add..."
							bind:value={searchQuery}
							onfocus={() => (dropdownOpen = true)} />
					</div>

					<!-- Dropdown -->
					{#if dropdownOpen && searchQuery.length > 0}
						<div
							class="absolute z-10 mt-1 w-full bg-white border border-gray-200 rounded-sm shadow-lg max-h-60 overflow-y-auto dark:bg-gray-700 dark:border-gray-600">
							{#if filteredCredentials.length > 0}
								<ul class="py-1 text-sm text-gray-700 dark:text-gray-200">
									{#each filteredCredentials as credential}
										<li>
											<button
												type="button"
												class="w-full text-left px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white flex items-center gap-2"
												onclick={() => addCredential(credential)}>
												<svg
													class="w-4 h-4 text-gray-400 shrink-0"
													xmlns="http://www.w3.org/2000/svg"
													fill="none"
													viewBox="0 0 24 24"
													stroke="currentColor"
													stroke-width="2">
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														d="M12 4.5v15m7.5-7.5h-15" />
												</svg>
												{credential.name}
											</button>
										</li>
									{/each}
								</ul>
							{:else}
								<div class="px-4 py-3 text-sm text-gray-500 dark:text-gray-400">
									No matching credentials found.
								</div>
							{/if}
						</div>
					{/if}
				</div>

				<!-- Credentials List -->
				{#if selectedCredentials.length > 0}
					<div class="border border-gray-200 rounded-sm dark:border-gray-600 overflow-hidden mb-6">
						<ul class="divide-y divide-gray-200 dark:divide-gray-600">
							{#each selectedCredentials as credential, index}
								<li
									class="group flex items-center gap-2 sm:gap-3 px-3 sm:px-4 py-2.5 bg-white dark:bg-gray-800 hover:bg-gray-50 dark:hover:bg-gray-700 {credential.isFinal
										? 'ring-1 ring-inset ring-green-200 bg-green-50 hover:bg-green-50 dark:bg-green-900/20'
										: ''}">
									<!-- Drag handle -->
									<span class="shrink-0 cursor-grab text-gray-400 hover:text-gray-600">
										<svg class="w-4 h-4" viewBox="0 0 16 16" fill="currentColor">
											<circle cx="5" cy="3" r="1.5" />
											<circle cx="11" cy="3" r="1.5" />
											<circle cx="5" cy="8" r="1.5" />
											<circle cx="11" cy="8" r="1.5" />
											<circle cx="5" cy="13" r="1.5" />
											<circle cx="11" cy="13" r="1.5" />
										</svg>
									</span>

									<!-- Order number -->
									<span
										class="shrink-0 w-6 h-6 flex items-center justify-center rounded-full bg-gray-100 text-xs font-medium text-gray-600 dark:bg-gray-700 dark:text-gray-300">
										{index + 1}
									</span>

									<!-- Credential name -->
									<div class="flex-1 min-w-0">
										<span class="text-sm font-medium text-gray-900 dark:text-white truncate block">
											{credential.name}
										</span>
									</div>

									<!-- Mark as final (visible on hover or if marked final) -->
									<button
										type="button"
										class="shrink-0 text-xs px-2 py-1 rounded-sm border cursor-pointer transition-opacity {credential.isFinal
											? 'opacity-100 bg-green-100 text-green-800 border-green-300 dark:bg-green-800 dark:text-green-200 dark:border-green-600'
											: 'opacity-0 group-hover:opacity-100 bg-gray-50 text-gray-500 border-gray-200 hover:bg-gray-100 dark:bg-gray-700 dark:text-gray-400 dark:border-gray-600 dark:hover:bg-gray-600'}"
										onclick={() => toggleFinal(index)}>
										{credential.isFinal ? 'Final' : 'Mark Final'}
									</button>

									<!-- Delete -->
									<button
										type="button"
										class="shrink-0 p-1 rounded hover:bg-red-100 dark:hover:bg-red-900/30 cursor-pointer"
										onclick={() => removeCredential(credential.id)}
										aria-label="Remove credential">
										<svg
											class="w-4 h-4 text-red-500"
											xmlns="http://www.w3.org/2000/svg"
											fill="none"
											viewBox="0 0 24 24"
											stroke="currentColor"
											stroke-width="2">
											<path
												stroke-linecap="round"
												stroke-linejoin="round"
												d="M14.74 9l-.346 9m-4.788 0L9.26 9m9.968-3.21c.342.052.682.107 1.022.166m-1.022-.165L18.16 19.673a2.25 2.25 0 01-2.244 2.077H8.084a2.25 2.25 0 01-2.244-2.077L4.772 5.79m14.456 0a48.108 48.108 0 00-3.478-.397m-12 .562c.34-.059.68-.114 1.022-.165m0 0a48.11 48.11 0 013.478-.397m7.5 0v-.916c0-1.18-.91-2.164-2.09-2.201a51.964 51.964 0 00-3.32 0c-1.18.037-2.09 1.022-2.09 2.201v.916m7.5 0a48.667 48.667 0 00-7.5 0" />
										</svg>
									</button>
								</li>
							{/each}
						</ul>
					</div>
				{:else}
					<div
						class="border border-dashed border-gray-300 rounded-sm px-4 py-8 text-center text-sm text-gray-500 dark:border-gray-600 dark:text-gray-400 mb-6">
						No credentials added yet. Search and add credentials above.
					</div>
				{/if}

				<!-- Action Buttons -->
				<div class="flex items-center justify-between pt-2">
					<button type="submit" class="btn-primary"> Save & Activate </button>
					<button type="button" class="cursor-pointer px-4 py-2 text-sm font-medium rounded-sm border border-yellow-400 bg-yellow-50 text-yellow-700 hover:bg-yellow-100"> Save as Draft </button>
				</div>
			</form>
		</div>
	</section>
</main>
