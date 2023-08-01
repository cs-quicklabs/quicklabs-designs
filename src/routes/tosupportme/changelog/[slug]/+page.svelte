<script>
	import UserNavBar from '$lib/tosupportme/usernavbar.svelte';
	let menu = { opened: false, filter: false };

	function toggle() {
		menu.opened = !menu.opened;
	}

	function filter() {
		menu.filter = !menu.filter;
	}
</script>

<UserNavBar />

<main class="max-w-2xl mx-auto">
	<a href="/tosupportme/changelog/public">
		<button
			type="button"
			class="mb-2 inline-flex items-center gap-x-1.5 shadow-sm px-2.5 rounded-md bg-white-600 py-1.5 text-sm font-semibold ring-1 ring-inset ring-gray-300 hover:bg-gray-50">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				stroke-width="1.5"
				stroke="currentColor"
				class="w-6 h-6">
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M19.5 12h-15m0 0l6.75 6.75M4.5 12l6.75-6.75" />
			</svg>
			See All Changelogs
		</button>
	</a>

	<div class="md:flex md:items-center md:justify-between">
		<div class="min-w-0 flex-1">
			<h2
				class="text-2xl font-bold leading-7 text-gray-900 sm:truncate sm:text-3xl sm:tracking-tight mt-4">
				Added Feature One
			</h2>
			<p class="mt-1 truncate text-sm text-gray-500">
				Published on October 12, 2022 as Version 3.0.2
			</p>
			<div class="mt-1">
				<span
					class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800"
					>Improvements</span>
				<span
					class="inline-flex items-center rounded bg-red-100 px-2 py-0.5 text-xs font-medium text-red-800"
					>Bug Fixes</span>
				<span
					class="inline-flex items-center rounded bg-green-100 px-2 py-0.5 text-xs font-medium text-green-800"
					>New</span>
				<span
					class="inline-flex items-center rounded bg-yellow-100 px-2 py-0.5 text-xs font-medium text-yellow-800"
					>Refactor</span>
				<span
					class="inline-flex items-center rounded bg-blue-100 px-2 py-0.5 text-xs font-medium text-blue-800"
					>Maintainence</span>
			</div>
		</div>
	</div>

	<div class=" space-y-6 text-sm text-gray-800 py-12">
		<p>This is rich text description of release notes</p>

		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita, hic? Commodi cumque
			similique id tempora molestiae deserunt at suscipit, dolor voluptatem, numquam, harum
			consequatur laboriosam voluptas tempore aut voluptatum alias?
		</p>
		<ul>
			<li>
				Tempor ultrices proin nunc fames nunc ut auctor vitae sed. Eget massa parturient vulputate
				fermentum id facilisis nam pharetra. Aliquet leo tellus.
			</li>
			<li>Turpis ac nunc adipiscing adipiscing metus tincidunt senectus tellus.</li>
			<li>
				Semper interdum porta sit tincidunt. Dui suspendisse scelerisque amet metus eget sed. Ut
				tellus in sed dignissim.
			</li>
		</ul>
		<div class=" text-sm text-gray-800">
			<span
				class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800"
				>iOS</span>
			<span
				class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800"
				>Android</span>
			<span
				class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800"
				>Web</span>
		</div>
	</div>
</main>
