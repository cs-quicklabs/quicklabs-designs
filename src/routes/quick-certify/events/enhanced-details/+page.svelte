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
        class="block w-full px-2 py-2.5 bg-neutral-secondary-medium border border-default-medium
               text-heading text-sm rounded-lg
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
        class="block w-full px-2 py-2.5 bg-neutral-secondary-medium border border-default-medium
               text-heading text-sm rounded-lg
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
        class="block w-full px-2 py-2.5 bg-neutral-secondary-medium border border-default-medium
               text-heading text-sm rounded-lg
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

    <!-- YOUR badge (unchanged) -->
    <span class="text-center inline-flex items-center bg-brand-softer border border-brand-subtle text-fg-brand-strong text-xs font-medium ps-1.5 pe-0.5 py-0.5 rounded gap-1">
      
      certificates
      <button type="button" class="inline-flex items-center p-0.5 text-sm bg-transparent rounded-xs hover:bg-brand-soft">
        
      </button>
    </span>

    <!-- Another badge -->
    <span class="inline-flex bg-neutral-secondary-medium border border-default-medium text-heading text-xs font-medium ps-1.5 pe-0.5 py-0.5 rounded gap-1">
      Events
      <button type="button" class="inline-flex items-center p-0.5 text-sm bg-transparent rounded-xs hover:bg-neutral-quaternary">
       
      </button>
    </span>

    <!-- Actual input -->
    <input
      type="text"
      placeholder="Name of Events"
      class="flex-1 min-w-[120px] h-full bg-transparent border-0 outline-none focus:ring-0 text-sm"
    />
  </div>

  <p class="form-input-description mt-2">
    Specify the name of the occasion on which you would like to issue credentials
  </p>
</div>

						
				</form>
			</div>

			
			<div class="flex justify-between items-center mt-4">
				<button type="submit" class="btn-primary"> Save Events </button>

				<button type="submit" class="btn-secondary px-3">cancel</button>
			</div>
			
		</main>
	</div>
</main>
