<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';

	const recipients = [
		{
			id: 1,
			name: 'Divanshu',
			email: 'neil.sims@flowbite.com',
			event: 'Award Name',
			issueDate: 'June 12 2025',
			status: '--'
		},
		{
			id: 2,
			name: 'Divanshu',
			email: 'neil.sims@flowbite.com',
			event: 'Award Name',
			issueDate: 'June 12 2025',
			status: '--'
		},
        	{
			id: 3,
			name: 'Raj',
			email: 'raj@flowbite.com',
			event: 'Award Name',
			issueDate: 'June 12 2025',
			status: '--'
		},
        	{
			id: 4,
			name: 'Aashish',
			email: 'Aashish@flowbite.com',
			event: 'Award Name',
			issueDate: 'June 12 2025',
			status: '--'
		}
	];
</script>

<NavBar />

<div class="relative overflow-x-auto bg-neutral-primary-soft border border-default rounded-base shadow-xs">
	<!-- Header -->
	<div class="flex flex-col md:flex-row md:items-center md:justify-between gap-4 p-4">
		
		<!-- Left section -->
		<div>
			<h2 class="text-heading font-medium">Credential</h2>
            <p class=mt-1 text-sm>4 credential</p>
<div class="relative inline-block mt-4">
  <details class="group">
    <summary
      class="inline-flex cursor-pointer items-center gap-2 px-3 py-2 text-sm font-medium
             bg-neutral-secondary-medium border border-default-medium rounded-base
             hover:bg-neutral-tertiary-medium list-none"
    >
      <!-- Filter Icon -->
      <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
          d="M3 4h18M6 10h12M10 16h4" />
      </svg>
      Filter by Events
    </summary>

    <!-- Dropdown -->
    <div
      class="absolute z-10 mt-2 w-48 rounded-base border border-default-medium
             bg-neutral-primary-medium shadow-lg p-3"
    >
      <p class="text-xs text-body mb-2 font-medium">Select Events</p>

      <label class="flex items-center gap-2 py-1 text-sm cursor-pointer">
        <input type="checkbox" class="rounded border-default-medium">
        Course Completion
      </label>

      <label class="flex items-center gap-2 py-1 text-sm cursor-pointer">
        <input type="checkbox" class="rounded border-default-medium">
        Top Performer
      </label>

      <label class="flex items-center gap-2 py-1 text-sm cursor-pointer">
        <input type="checkbox" class="rounded border-default-medium">
        Participation
      </label>

      <label class="flex items-center gap-2 py-1 text-sm cursor-pointer">
        <input type="checkbox" class="rounded border-default-medium">
        Achievement
      </label>
    </div>
  </details>
</div>

		</div>

		<!-- Right section -->
		<div class="flex flex-col items-start md:items-end gap-3">
			<button
				class="inline-flex items-center px-3 py-2 text-sm font-medium rounded-base
				bg-neutral-secondary-medium border border-default-medium hover:bg-neutral-tertiary-medium"
			>
				Issuer Credential
			</button>

			<div class="w-full max-w-96">

				<input
					type="text"
					class="w-full text-sm
					bg-neutral-secondary-medium border border-default-medium
					focus:ring-brand focus:border-brand"
					placeholder="Search recipients by name,email"
				/>
			</div>
		</div>
	</div>

	<!-- Table -->
	<table class="w-full text-sm text-left text-body">
		<thead class="bg-neutral-secondary-medium border-y border-default-medium">
			<tr>
				<th class="px-6 py-3 font-medium">Name</th>
				<th class="px-6 py-3 font-medium">Email</th>
				<th class="px-6 py-3 font-medium">Events</th>
				<th class="px-6 py-3 font-medium">Issue Date</th>
				<th class="px-6 py-3 font-medium">Status</th>
				<th class="px-6 py-3 font-medium">Action</th>
			</tr>
		</thead>

		<tbody>
			{#each recipients as user}
				<tr class="border-b border-default bg-neutral-primary-soft hover:bg-neutral-secondary-medium">
					<td class="px-6 py-4">{user.name}</td>
					<td class="px-6 py-4">{user.email}</td>
					<td class="px-6 py-4">{user.event}</td>
					<td class="px-6 py-4">{user.issueDate}</td>
					<td class="px-6 py-4">
						<div class="flex items-center">
							{user.status}
						</div>
					</td>
					<td class="px-6 py-4">
						<a href="#" class="text-fg-brand font-medium hover:underline">View</a>
					</td>
				</tr>
			{/each}
		</tbody>
	</table>
    
<nav aria-label="Page navigation example" class="flex justify-end p-4">
  <ul class="flex -space-x-px text-sm">
    <li>
      <a href="#"
        class="flex items-center justify-center px-3 h-9 text-sm font-medium
               bg-neutral-secondary-medium border border-default-medium
               rounded-s-base hover:bg-neutral-tertiary-medium">
        Previous
      </a>
    </li>

    <li>
      <a href="#" class="flex items-center justify-center w-9 h-9 text-sm border border-default-medium">
        1
      </a>
    </li>

    <li>
      <a href="#" class="flex items-center justify-center w-9 h-9 text-sm border border-default-medium">
        2
      </a>
    </li>

    <li>
      <a href="#" aria-current="page"
        class="flex items-center justify-center w-9 h-9 text-sm font-medium
               text-fg-brand bg-neutral-tertiary-medium border border-default-medium">
        3
      </a>
    </li>

    <li>
      <a href="#" class="flex items-center justify-center w-9 h-9 text-sm border border-default-medium">
        4
      </a>
    </li>

    <li>
      <a href="#" class="flex items-center justify-center w-9 h-9 text-sm border border-default-medium">
        5
      </a>
    </li>

    <li>
      <a href="#"
        class="flex items-center justify-center px-3 h-9 text-sm font-medium
               bg-neutral-secondary-medium border border-default-medium
               rounded-e-base hover:bg-neutral-tertiary-medium">
        Next
      </a>
    </li>
  </ul>
</nav>



</div>
