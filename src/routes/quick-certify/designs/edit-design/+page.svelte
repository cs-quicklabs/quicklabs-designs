<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';
	import SideBar from '$quick-certify/common/navbar/account.svelte';
</script>

<NavBar />

<main class="flex justify-center max-w-7xl mx-auto pb-10 lg:py-12 lg:px-8">
	<main class="max-w-xl pb-12 px-4 lg:col-span-6">
		<div>
			<h1 class="form-title">Edit Design</h1>
			<p class="form-subtitle">Edit certificate or badge design by updating the name and selecting a new image.</p>
		</div>

		<form class="w-full mt-4 space-y-4">
			<div class="mb-4">
				<label for="email" class="form-input-label">Edit Name </label>
				<input id="name" class="form-input-field" placeholder="" required value= "Crownstack Culture Code"/>
			</div>
			<div class="mb-2">
				<label for="dropzone-file" class="form-input-label">Upload Image</label>
				<p class="form-input-description -mt-2 mb-2">
					Upload A4 (1123x794 px) size image for certificate or (400x400 px) for badge
				</p>
			</div>
			<div class="flex justify-center items-center w-full">
				<label
					for="dropzone-file"
					class="flex flex-col justify-center items-center w-full h-40 bg-gray-50 rounded-sm border-2 border-gray-300 border-dashed cursor-pointer dark:hover:bg-bray-800 dark:bg-gray-700 hover:bg-gray-100 dark:border-gray-600 dark:hover:border-gray-500 dark:hover:bg-gray-600">
					<div class="flex flex-col justify-center items-center pt-5 pb-6">
						<svg
							aria-hidden="true"
							class="mb-3 w-15 h-12 text-gray-400"
							fill="none"
							stroke="currentColor"
							viewBox="0 0 24 24"
							xmlns="http://www.w3.org/2000/svg"
							><path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12"
							></path
							></svg>
						<p class="mb-2 text-sm text-gray-500 dark:text-gray-400">
							<span class="font-semibold">Click to upload</span> or drag and drop
						</p>
						<p class="mb-4 text-xs text-gray-500 dark:text-gray-400">Size:1123x794</p>
					</div>
					<input id="dropzone-file" type="file" class="hidden" />
				</label>
			</div>
			<div class="flex justify-between items-center mt-4">
				<button type="submit" class="btn-primary"> Save Design </button>

				<button type="submit" class="btn-secondary"> Replace Image </button>
			</div>
		</form>
	</main>
</main>
