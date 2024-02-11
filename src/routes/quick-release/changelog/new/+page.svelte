<script>
	import Fullnavbar from '$quick-release/shared/fullnavbar.svelte';
	let menu = { opened: false, filter: false };

	function toggle() {
		menu.opened = !menu.opened;
	}

	function filter() {
		menu.filter = !menu.filter;
	}
</script>

<Fullnavbar />

<main class="mx-auto max-w-2xl px-4 pt-10 pb-12 lg:pb-16">
	<form>
		<div class="space-y-6">
			<div>
				<h1 class="text-lg font-medium leading-6 text-gray-900">Add New Change Log</h1>
				<p class="mt-1 text-sm text-gray-500">
					Let’s get started by filling in the information below to create your new changelog.
				</p>
			</div>

			<div>
				<label for="project-name" class="block text-sm font-medium leading-6 text-gray-900"
					>Title</label>
				<div class="mt-2">
					<input
						type="text"
						name="project-name"
						id="project-name"
						class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-sky-500 sm:text-sm sm:leading-6"
						value="" />
				</div>
			</div>

			<div class="sm:col-span-2">
				<label for="biography" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
					>Description</label>
				<div
					class="w-full bg-gray-50 rounded-lg border border-gray-200 dark:bg-gray-700 dark:border-gray-600">
					<div class="flex justify-between items-center border-b dark:border-gray-600">
						<div
							class="flex flex-wrap items-center divide-gray-200 sm:divide-x dark:divide-gray-600">
							<div class="flex items-center space-x-1 sm:pr-4">
								<button
									type="button"
									class="p-2 text-gray-500 rounded cursor-pointer hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600">
									<svg
										aria-hidden="true"
										class="w-5 h-5"
										fill="currentColor"
										viewBox="0 0 20 20"
										xmlns="http://www.w3.org/2000/svg"
										><path
											fill-rule="evenodd"
											d="M8 4a3 3 0 00-3 3v4a5 5 0 0010 0V7a1 1 0 112 0v4a7 7 0 11-14 0V7a5 5 0 0110 0v4a3 3 0 11-6 0V7a1 1 0 012 0v4a1 1 0 102 0V7a3 3 0 00-3-3z"
											clip-rule="evenodd"></path
										></svg>
									<span class="sr-only">Attach file</span>
								</button>
								<button
									type="button"
									class="p-2 text-gray-500 rounded cursor-pointer hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600">
									<svg
										aria-hidden="true"
										class="w-5 h-5"
										fill="currentColor"
										viewBox="0 0 20 20"
										xmlns="http://www.w3.org/2000/svg"
										><path
											fill-rule="evenodd"
											d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z"
											clip-rule="evenodd"></path
										></svg>
									<span class="sr-only">Embed map</span>
								</button>
								<button
									type="button"
									class="p-2 text-gray-500 rounded cursor-pointer hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600">
									<svg
										aria-hidden="true"
										class="w-5 h-5"
										fill="currentColor"
										viewBox="0 0 20 20"
										xmlns="http://www.w3.org/2000/svg"
										><path
											fill-rule="evenodd"
											d="M4 3a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V5a2 2 0 00-2-2H4zm12 12H4l4-8 3 6 2-4 3 6z"
											clip-rule="evenodd"></path
										></svg>
									<span class="sr-only">Upload image</span>
								</button>
								<button
									type="button"
									class="p-2 text-gray-500 rounded cursor-pointer hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600">
									<svg
										aria-hidden="true"
										class="w-5 h-5"
										fill="currentColor"
										viewBox="0 0 20 20"
										xmlns="http://www.w3.org/2000/svg"
										><path
											fill-rule="evenodd"
											d="M12.316 3.051a1 1 0 01.633 1.265l-4 12a1 1 0 11-1.898-.632l4-12a1 1 0 011.265-.633zM5.707 6.293a1 1 0 010 1.414L3.414 10l2.293 2.293a1 1 0 11-1.414 1.414l-3-3a1 1 0 010-1.414l3-3a1 1 0 011.414 0zm8.586 0a1 1 0 011.414 0l3 3a1 1 0 010 1.414l-3 3a1 1 0 11-1.414-1.414L16.586 10l-2.293-2.293a1 1 0 010-1.414z"
											clip-rule="evenodd"></path
										></svg>
									<span class="sr-only">Format code</span>
								</button>
								<button
									type="button"
									class="p-2 text-gray-500 rounded cursor-pointer hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600">
									<svg
										aria-hidden="true"
										class="w-5 h-5"
										fill="currentColor"
										viewBox="0 0 20 20"
										xmlns="http://www.w3.org/2000/svg"
										><path
											fill-rule="evenodd"
											d="M10 18a8 8 0 100-16 8 8 0 000 16zM7 9a1 1 0 100-2 1 1 0 000 2zm7-1a1 1 0 11-2 0 1 1 0 012 0zm-.464 5.535a1 1 0 10-1.415-1.414 3 3 0 01-4.242 0 1 1 0 00-1.415 1.414 5 5 0 007.072 0z"
											clip-rule="evenodd"></path
										></svg>
									<span class="sr-only">Add emoji</span>
								</button>
							</div>
							<div class="hidden flex-wrap items-center space-x-1 sm:flex sm:pl-4">
								<button
									type="button"
									class="p-2 text-gray-500 rounded cursor-pointer hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600">
									<svg
										aria-hidden="true"
										class="w-5 h-5"
										fill="currentColor"
										viewBox="0 0 20 20"
										xmlns="http://www.w3.org/2000/svg"
										><path
											fill-rule="evenodd"
											d="M3 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm0 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm0 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm0 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
											clip-rule="evenodd"></path
										></svg>
									<span class="sr-only">Add list</span>
								</button>
								<button
									type="button"
									class="p-2 text-gray-500 rounded cursor-pointer hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600">
									<svg
										aria-hidden="true"
										class="w-5 h-5"
										fill="currentColor"
										viewBox="0 0 20 20"
										xmlns="http://www.w3.org/2000/svg"
										><path
											fill-rule="evenodd"
											d="M11.49 3.17c-.38-1.56-2.6-1.56-2.98 0a1.532 1.532 0 01-2.286.948c-1.372-.836-2.942.734-2.106 2.106.54.886.061 2.042-.947 2.287-1.561.379-1.561 2.6 0 2.978a1.532 1.532 0 01.947 2.287c-.836 1.372.734 2.942 2.106 2.106a1.532 1.532 0 012.287.947c.379 1.561 2.6 1.561 2.978 0a1.533 1.533 0 012.287-.947c1.372.836 2.942-.734 2.106-2.106a1.533 1.533 0 01.947-2.287c1.561-.379 1.561-2.6 0-2.978a1.532 1.532 0 01-.947-2.287c.836-1.372-.734-2.942-2.106-2.106a1.532 1.532 0 01-2.287-.947zM10 13a3 3 0 100-6 3 3 0 000 6z"
											clip-rule="evenodd"></path
										></svg>
									<span class="sr-only">Settings</span>
								</button>
								<button
									type="button"
									class="p-2 text-gray-500 rounded cursor-pointer hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600">
									<svg
										aria-hidden="true"
										class="w-5 h-5"
										fill="currentColor"
										viewBox="0 0 20 20"
										xmlns="http://www.w3.org/2000/svg"
										><path
											fill-rule="evenodd"
											d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z"
											clip-rule="evenodd"></path
										></svg>
									<span class="sr-only">Timeline</span>
								</button>
								<button
									type="button"
									class="p-2 text-gray-500 rounded cursor-pointer hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600">
									<svg
										aria-hidden="true"
										class="w-5 h-5"
										fill="currentColor"
										viewBox="0 0 20 20"
										xmlns="http://www.w3.org/2000/svg"
										><path
											fill-rule="evenodd"
											d="M3 17a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm3.293-7.707a1 1 0 011.414 0L9 10.586V3a1 1 0 112 0v7.586l1.293-1.293a1 1 0 111.414 1.414l-3 3a1 1 0 01-1.414 0l-3-3a1 1 0 010-1.414z"
											clip-rule="evenodd"></path
										></svg>
									<span class="sr-only">Download</span>
								</button>
							</div>
						</div>
						<button
							type="button"
							data-tooltip-target="tooltip-fullscreen"
							class="p-2 text-gray-500 rounded cursor-pointer sm:ml-auto hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600">
							<svg
								aria-hidden="true"
								class="w-5 h-5"
								fill="currentColor"
								viewBox="0 0 20 20"
								xmlns="http://www.w3.org/2000/svg"
								><path
									fill-rule="evenodd"
									d="M3 4a1 1 0 011-1h4a1 1 0 010 2H6.414l2.293 2.293a1 1 0 11-1.414 1.414L5 6.414V8a1 1 0 01-2 0V4zm9 1a1 1 0 010-2h4a1 1 0 011 1v4a1 1 0 01-2 0V6.414l-2.293 2.293a1 1 0 11-1.414-1.414L13.586 5H12zm-9 7a1 1 0 012 0v1.586l2.293-2.293a1 1 0 111.414 1.414L6.414 15H8a1 1 0 010 2H4a1 1 0 01-1-1v-4zm13-1a1 1 0 011 1v4a1 1 0 01-1 1h-4a1 1 0 010-2h1.586l-2.293-2.293a1 1 0 111.414-1.414L15 13.586V12a1 1 0 011-1z"
									clip-rule="evenodd"></path
								></svg>
							<span class="sr-only">Full screen</span>
						</button>
						<div
							id="tooltip-fullscreen"
							role="tooltip"
							class="inline-block absolute invisible z-10 py-2 px-3 text-sm font-medium text-white bg-gray-900 rounded-lg shadow-sm opacity-0 transition-opacity duration-300 tooltip dark:bg-gray-700"
							data-popper-reference-hidden=""
							data-popper-escaped=""
							data-popper-placement="bottom"
							style="position: absolute; inset: 0px auto auto 0px; margin: 0px; transform: translate3d(0px, 335px, 0px);">
							Show full screen
							<div class="tooltip-arrow" data-popper-arrow=""></div>
						</div>
					</div>
					<div class="py-2 px-4 bg-white rounded-b-lg dark:bg-gray-800">
						<textarea
							id="biography"
							rows="8"
							class="block px-0 w-full text-sm text-gray-800 bg-white border-0 dark:bg-gray-800 focus:ring-0 dark:text-white dark:placeholder-gray-400"
							placeholder="Write a message here"
							required=""></textarea>
					</div>
				</div>
			</div>

			<div>
				<label for="project-name" class="block text-sm font-medium leading-6 text-gray-900"
					>Release Version (Optional)</label>
				<div class="mt-2">
					<input
						type="text"
						name="project-name"
						id="project-name"
						class="px-2 block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-sky-500 sm:text-sm sm:leading-6"
						value=""
						placeholder="1.0.0" />
				</div>
			</div>

			<fieldset>
				<label for="project-name" class="block text-sm font-medium leading-6 text-gray-900"
					>Release Categories (Optional)</label>

				<div class="space-y-1 flex items-center space-x-4">
					<div class="relative flex items-start">
						<div class="flex h-6 items-center">
							<input
								id="comments"
								aria-describedby="comments-description"
								name="comments"
								type="checkbox"
								class="h-4 w-4 rounded border-green-300 text-green-600 focus:ring-green-600" />
						</div>
						<div class="ml-1 text-sm leading-6">
							<span
								class="inline-flex items-center rounded bg-green-100 px-2 py-0.5 text-xs font-medium text-green-800">
								New
							</span>
						</div>
					</div>

					<div class="relative flex items-start">
						<div class="flex h-6 items-center">
							<input
								id="comments"
								aria-describedby="comments-description"
								name="comments"
								type="checkbox"
								class="h-4 w-4 rounded border-gray-300 text-gray-600 focus:ring-gray-600" />
						</div>
						<div class="ml-1 text-sm leading-6">
							<span
								class="inline-flex items-center rounded bg-gray-100 px-2 py-0.5 text-xs font-medium text-gray-800">
								Improvements
							</span>
						</div>
					</div>

					<div class="relative flex items-start">
						<div class="flex h-6 items-center">
							<input
								id="comments"
								aria-describedby="comments-description"
								name="comments"
								type="checkbox"
								class="h-4 w-4 rounded border-red-300 text-red-600 focus:ring-red-600" />
						</div>
						<div class="ml-1 text-sm leading-6">
							<span
								class="inline-flex items-center rounded bg-red-100 px-2 py-0.5 text-xs font-medium text-red-800">
								Bug Fixes
							</span>
						</div>
					</div>

					<div class="relative flex items-start">
						<div class="flex h-6 items-center">
							<input
								id="comments"
								aria-describedby="comments-description"
								name="comments"
								type="checkbox"
								class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-600" />
						</div>
						<div class="ml-1 text-sm leading-6">
							<span
								class="inline-flex items-center rounded bg-indigo-100 px-2 py-0.5 text-xs font-medium text-indigo-800">
								Maintainence
							</span>
						</div>
					</div>

					<div class="relative flex items-start">
						<div class="flex h-6 items-center">
							<input
								id="comments"
								aria-describedby="comments-description"
								name="comments"
								type="checkbox"
								class="h-4 w-4 rounded border-yellow-300 text-yellow-600 focus:ring-yellow-600" />
						</div>
						<div class="ml-1 text-sm leading-6">
							<span
								class="inline-flex items-center rounded bg-yellow-100 px-2 py-0.5 text-xs font-medium text-yellow-800">
								Refactor
							</span>
						</div>
					</div>
				</div>
			</fieldset>
			<div>
				<label for="tags" class="block text-sm font-medium leading-6 text-gray-900"
					>Release Tags (Optional)</label>

				<div class="flex mt-2">
					<div class="flex items-center me-4">
						<input
							id="inline-checkbox"
							type="checkbox"
							value=""
							class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />
						<label
							for="inline-checkbox"
							class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300">Inline 1</label>
					</div>
					<div class="flex items-center me-4">
						<input
							id="inline-2-checkbox"
							type="checkbox"
							value=""
							class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />
						<label
							for="inline-2-checkbox"
							class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300">Inline 2</label>
					</div>
					<div class="flex items-center me-4">
						<input
							checked
							id="inline-checked-checkbox"
							type="checkbox"
							value=""
							class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />
						<label
							for="inline-checked-checkbox"
							class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
							>Inline checked</label>
					</div>
					<div class="flex items-center">
						<input
							disabled
							id="inline-disabled-checkbox"
							type="checkbox"
							value=""
							class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />
						<label
							for="inline-checked-checkbox"
							class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300">Inline 4</label>
					</div>
				</div>
			</div>

			<div>
				<label for="project-name" class="mb-2 block text-sm font-medium leading-6 text-gray-900"
					>Release Version (Optional)</label>

				<div class="relative">
					<div class="absolute inset-y-0 start-0 flex items-center ps-3 pointer-events-none">
						<svg
							class="w-4 h-4 text-gray-500 dark:text-gray-400"
							aria-hidden="true"
							xmlns="http://www.w3.org/2000/svg"
							fill="currentColor"
							viewBox="0 0 20 20">
							<path
								d="M20 4a2 2 0 0 0-2-2h-2V1a1 1 0 0 0-2 0v1h-3V1a1 1 0 0 0-2 0v1H6V1a1 1 0 0 0-2 0v1H2a2 2 0 0 0-2 2v2h20V4ZM0 18a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V8H0v10Zm5-8h10a1 1 0 0 1 0 2H5a1 1 0 0 1 0-2Z" />
						</svg>
					</div>
					<input
						datepicker
						datepicker-autohide
						type="text"
						class=" border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full ps-10 p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
						placeholder="Select date" />
				</div>
			</div>
			<div class="flex justify-end gap-x-3">
				<a href="/quick-release/changelog">
					<button
						type="button"
						class="rounded-md bg-white py-2 px-3 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50"
						>Cancel</button>
				</a>
				<div>
					<label id="listbox-label" class="sr-only">Change published status</label>
					<div class="relative">
						<div class="inline-flex divide-x divide-indigo-700 rounded-md shadow-sm">
							<div
								class="inline-flex items-center gap-x-1.5 rounded-l-md bg-indigo-600 py-2 px-3 text-white shadow-sm">
								<svg
									class="-ml-0.5 h-5 w-5"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true">
									<path
										fill-rule="evenodd"
										d="M16.704 4.153a.75.75 0 01.143 1.052l-8 10.5a.75.75 0 01-1.127.075l-4.5-4.5a.75.75 0 011.06-1.06l3.894 3.893 7.48-9.817a.75.75 0 011.05-.143z"
										clip-rule="evenodd" />
								</svg>
								<p class="text-sm font-semibold">Publish Changelog Now</p>
							</div>
							<button
								type="button"
								class="inline-flex items-center rounded-l-none rounded-r-md bg-indigo-600 p-2 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-600 focus:ring-offset-2 focus:ring-offset-gray-50"
								aria-haspopup="listbox"
								aria-expanded="true"
								aria-labelledby="listbox-label">
								<span class="sr-only">Change published status</span>
								<svg
									class="h-5 w-5 text-white"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true">
									<path
										fill-rule="evenodd"
										d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z"
										clip-rule="evenodd" />
								</svg>
							</button>
						</div>

						<!--
                Select popover, show/hide based on select state.
          
                Entering: ""
                  From: ""
                  To: ""
                Leaving: "transition ease-in duration-100"
                  From: "opacity-100"
                  To: "opacity-0"
              -->
						<ul
							class="absolute right-0 z-10 mt-2 w-72 origin-top-right divide-y divide-gray-200 overflow-hidden rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
							tabindex="-1"
							role="listbox"
							aria-labelledby="listbox-label"
							aria-activedescendant="listbox-option-0">
							<!--
                  Select option, manage highlight styles based on mouseenter/mouseleave and keyboard navigation.
          
                  Highlighted: "bg-indigo-600 text-white", Not Highlighted: "text-gray-900"
                -->
							<li
								class="text-gray-900 cursor-default select-none p-4 text-sm"
								id="listbox-option-0"
								role="option">
								<div class="flex flex-col">
									<div class="flex justify-between">
										<!-- Selected: "font-semibold", Not Selected: "font-normal" -->
										<p class="font-normal">Publish Now</p>
										<!--
                        Checkmark, only display for selected option.
          
                        Highlighted: "text-white", Not Highlighted: "text-indigo-600"
                      -->
										<span class="text-indigo-600">
											<svg
												class="h-5 w-5"
												viewBox="0 0 20 20"
												fill="currentColor"
												aria-hidden="true">
												<path
													fill-rule="evenodd"
													d="M16.704 4.153a.75.75 0 01.143 1.052l-8 10.5a.75.75 0 01-1.127.075l-4.5-4.5a.75.75 0 011.06-1.06l3.894 3.893 7.48-9.817a.75.75 0 011.05-.143z"
													clip-rule="evenodd" />
											</svg>
										</span>
									</div>
									<!-- Highlighted: "text-indigo-200", Not Highlighted: "text-gray-500" -->
									<p class="text-gray-500 mt-2">Publish your change log now</p>
								</div>
							</li>

							<!-- More items... -->

							<li
								class="text-gray-900 cursor-default select-none p-4 text-sm"
								id="listbox-option-0"
								role="option">
								<div class="flex flex-col">
									<div class="flex justify-between">
										<!-- Selected: "font-semibold", Not Selected: "font-normal" -->
										<p class="font-normal">Save as Draft</p>
										<!--
                          Checkmark, only display for selected option.
            
                          Highlighted: "text-white", Not Highlighted: "text-indigo-600"
                        -->
									</div>
									<!-- Highlighted: "text-indigo-200", Not Highlighted: "text-gray-500" -->
									<p class="text-gray-500 mt-2">Save as draft and edit in future</p>
								</div>
							</li>

							<!-- More items... -->

							<li
								class="text-gray-900 cursor-default select-none p-4 text-sm"
								id="listbox-option-0"
								role="option">
								<div class="flex flex-col">
									<div class="flex justify-between">
										<!-- Selected: "font-semibold", Not Selected: "font-normal" -->
										<p class="font-normal">Schedule</p>
										<!--
                          Checkmark, only display for selected option.
            
                          Highlighted: "text-white", Not Highlighted: "text-indigo-600"
                        -->
									</div>
									<!-- Highlighted: "text-indigo-200", Not Highlighted: "text-gray-500" -->
									<p class="text-gray-500 mt-2">
										Schedule your release to publish automatically on specified date
									</p>
								</div>
							</li>
						</ul>
					</div>
				</div>
			</div>
		</div>
	</form>
</main>
