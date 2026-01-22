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

<section class="bg-gray-50 py-2 min-h-screen">
  <div class="px-4 mx-auto max-w-screen-2xl lg:px-8">
    <div class="bg-white border border-gray-200 rounded-md shadow-sm overflow-hidden">

      <!-- Header -->
      <div class="flex items-center justify-between px-4 py-2 border-b border-gray-200">
        <div>
          <h1 class="text-lg font-semibold text-gray-900">Credential</h1>
          <p class="text-sm text-gray-500">4 credentials</p>
        </div>

        <button
          class="btn-primary">
          Issuer Credential
        </button>
      </div>

      <!-- Filters -->
      <div class="flex flex-wrap items-center gap-4 px-4 py-2 border-b border-gray-200">

        <!-- Filter dropdown -->
        <details class="relative">
          <summary
            class="cursor-pointer flex items-center gap-2 px-3 py-2 text-sm
                   border border-gray-200 rounded-md bg-gray-50 hover:bg-gray-100 list-none">
            <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                d="M3 4h18M6 10h12M10 16h4" />
            </svg>
            Filter by Events
          </summary>

          <div
            class="absolute z-10 mt-2 w-48 bg-white border border-gray-200 rounded-md shadow p-3">
            <p class="text-xs font-medium text-gray-500 mb-2">Select Events</p>

            {#each ['Events 1','Events-2','Events-3','Events-4'] as event}
              <label class="flex items-center gap-2 py-1 text-sm text-gray-700">
                <input type="checkbox" class="rounded border-gray-300" />
                {event}
              </label>
            {/each}
          </div>
        </details>

        <!-- Search -->
        <div class="ml-auto">
          <input
            type="text"
            placeholder="Search by name..."
            class="w-48 px-3 py-2 text-sm border border-gray-200 rounded-md
                   bg-gray-50 focus:ring-1 focus:ring-gray-300 focus:outline-none" />
        </div>
      </div>

      <!-- Table -->
      <table class="w-full text-sm text-left text-gray-700">
        <thead class="bg-gray-50 border-b border-gray-200">
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
            <tr class="border-b border-gray-200 hover:bg-gray-50">
              <td class="px-6 py-2">{user.name}</td>
              <td class="px-6 py-2">{user.email}</td>
              <td class="px-6 py-2">{user.event}</td>
              <td class="px-6 py-2">{user.issueDate}</td>
              <td class="px-6 py-2 text-gray-500">{user.status}</td>
              <td class="px-6 py-2">
                <a href="#" class="text-blue-600 hover:underline">View</a>
              </td>
            </tr>
          {/each}
        </tbody>
      </table>

      <!-- Pagination -->
      <div class="flex justify-end px-4 py-3 border-t border-gray-200">
        <ul class="flex text-sm">
          {#each ['Previous',1,2,3,4,5,'Next'] as page}
            <li>
              <a
                href="#"
                class="flex items-center justify-center px-3 h-9 border border-gray-200
                       hover:bg-gray-100 text-gray-700">
                {page}
              </a>
            </li>
          {/each}
        </ul>
      </div>

    </div>
  </div>
</section>


