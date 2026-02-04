<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';
	import SideBar from '$quick-certify/common/navbar/events-group.svelte';
	import InfoButton from '$lib/tooltip.svelte';
</script>

<NavBar />
<main class="max-w-7xl mx-auto pb-10 lg:py-12 lg:px-8">
	<div class="lg:grid lg:grid-cols-12 lg:gap-x-5">
		<SideBar />

		<main class="max-w-xl pb-12 px-4 lg:col-span-6">
		<div>
				<h1 class="form-title">About</h1>
				<p class="form-subtitle">
					Add a detailed description of your event and a link to its website.
				</p>

				<form class="w-full mt-4 space-y-4">
					

					<div class="mb-4">
						<div class="flex items-center space-x-1 mb-2">
							<label for="password" class="block text-sm font-medium text-gray-900 dark:text-white"
								>Description</label>
							<InfoButton
								tooltipText="Provide a detailed description of your event that will appear on the issuer portal. This helps recipients understand the context and significance of the credentials they receive."
								id="tooltip-hot" />
						</div>
						<textarea
							id="message"
							rows="4"
							class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-sm border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
							placeholder="Write more description here..."></textarea>
					</div>

					<div class="">
						<label for="email" class="form-input-label">Learning Events Link </label>
						<div class="flex">
				
							<input
								type="text"
								id="website-admin"
								class="form-input-field"
							 />
						</div>
					</div>
                  
  <div class="flex flex-col gap-4 sm:flex-row">


    <div class="flex-1">
      <label class="block mb-2.5 text-sm font-medium text-heading">
        Type
      </label>
      <select
        class="block w-full px-2 py-2 bg-neutral-secondary-medium border border-default-medium
               text-heading text-sm rounded-xs
               focus:ring-brand focus:border-brand shadow-xs cursor-pointer"
      >
        <option selected>Event Type</option>
        <option>Type 1</option>
        <option>Type 2</option>
        <option>Type 3</option>
        <option>Type 4</option>
      </select>
    </div>

    <div class="flex-1">
     <label class="block mb-2.5 text-sm font-medium text-heading">
        Events Level
      </label>
      <select
        class="block w-full px-2 py-2 bg-neutral-secondary-medium border border-default-medium
               text-heading text-sm rounded-xs
               focus:ring-brand focus:border-brand shadow-xs cursor-pointer"
      >
        <option selected>Event level</option>
        <option>Level 1</option>
         <option>Level 2</option>
      </select>
    </div>

    <div class="flex-1">
       <label class="block mb-2.5 text-sm font-medium text-heading">
        Events Format
      </label>
      <select
        class="block w-full px-1 py-2 bg-neutral-secondary-medium border border-default-medium
               text-heading text-sm rounded-xs
               focus:ring-brand focus:border-brand shadow-xs cursor-pointer"
      >
        <option selected>Format</option>
        <option>Format 1</option>
        <option>Format 2</option>
      </select>
    </div>
    </div>
    
    
<div class="w-full">
  <label class="form-input-label">Skills</label>

  <!-- Fake input field -->
  <div class="form-input-field flex flex-wrap items-center gap-2 min-h-[52px]">

   
      
      <span id="badge-avatar-dismiss-gray" class="inline-flex items-center bg-neutral-secondary-medium border border-default-medium text-heading text-xs font-medium ps-1.5 pe-0.5 py-0.5 rounded gap-1">
      JS
      <button type="button" class="inline-flex items-center p-0.5 text-sm bg-transparent rounded-xs hover:bg-neutral-quaternary" data-dismiss-target="#badge-avatar-dismiss-gray" aria-label="Remove">
        <svg class="w-3 h-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24"><path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18 17.94 6M18 18 6.06 6"/></svg>
        <span class="sr-only">Remove badge</span>
      </button>
      </span>
      
      <span id="badge-avatar-dismiss-danger" class="inline-flex items-center bg-danger-soft border border-danger-subtle text-fg-danger-strong text-xs font-medium ps-1.5 pe-0.5 py-0.5 rounded gap-1">
      Python
      <button type="button" class="inline-flex items-center p-0.5 text-sm bg-transparent rounded-xs hover:bg-danger-medium" data-dismiss-target="#badge-avatar-dismiss-danger" aria-label="Remove">
        <svg class="w-3 h-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24"><path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18 17.94 6M18 18 6.06 6"/></svg>
        <span class="sr-only">Remove badge</span>
      </button>
      </span>
      
      
      
  

    <!-- Actual input -->
    <input
      type="text"
      placeholder="Name of Skills"
      class="flex-1 min-w-[120px] h-full bg-transparent border-0 outline-none focus:ring-0 text-sm"
    />
  </div>
</div>

						
				</form>
			</div>

			
			<div class="flex justify-between items-center mt-4">
				<button type="submit" class="btn-primary"> Save Events </button>

				<button type="submit" class="btn-secondary px-3">Cancel</button>
			</div>
			
		</main>
	</div>
</main>
