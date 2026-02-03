<script>
	import Header from '$quick-certify/common/navbar/header.svelte';
	import Footer from '$quick-certify/common/navbar/footer.svelte';
</script>

<Header />
<div class="flex min-h-full flex-col bg-gray-50 ">
	<!-- 3 column wrapper -->
	<div class="mx-auto w-full max-w-7xl grow lg:flex xl:px-2">
		<!-- Left sidebar & main wrapper -->
		<div class="flex-1 xl:flex">
			<div class="px-4 py-6 sm:px-6 lg:pl-8 lg:w-60 xl:shrink-0 xl:pl-6">
				<!-- Left column area -->
			</div>

			<div class="py-8 :flex-1">
				<!-- Main area -->
				<img
					src="/quick-certify/rashi.png"
					class="rounded-sm
"
					alt="Illustration" />
				<div class="w-full flex items-center justify-between">
					<p class="mt-1 text-xs font-normal text-gray-500 dark:text-gray-300" id="file_input_help">
						Credential ID: <span
							class="text-green-700 hover:underline cursor-pointer dark:text-white"
							>019c617e-58c1-4de1-a975-73c20737580e</span>
					</p>
					<p class="mt-1 text-xs font-normal text-gray-500 dark:text-gray-300" id="file_input_help">
						Distributed By: <span
							class="text-gray-900 hover:underline font-bold cursor-pointer dark:text-white"
							>Quick Certify</span>
					</p>
				</div>
			</div>
		</div>

		<div class="shrink-0 px-4 py-6 sm:px-6 lg:w-60 lg:pr-8 xl:pr-6">
			<!-- Right column area -->
		</div>
	</div>
</div>
<div class="bg-gray-50">
	<!-- 3 column wrapper -->
	<div class="mx-auto w-full max-w-7xl grow lg:flex xl:px-2 bg-gray-50 ">
		<!-- Left sidebar & main wrapper -->
		<div class="flex-1 xl:flex">
			<div class="py-6 lg:pl-8 lg:w-96 xl:shrink-0 xl:pl-4">
				<!-- Left column area -->
					<div
						class="flex flex-col overflow-hidden rounded-sm border border-stroke-dark border-gray-200 bg-white p-4 md:p-4 gap-3">
						<div class="flex justify-between">
							<div class="flex flex-col gap-2">
								<h4 class="text-xs font-medium uppercase leading-6 text-blue-500">Issued to</h4>
								<h2 class="text-2xl font-medium">Rashi Gupta</h2>
							</div>
						</div>
						<div>
							<button
								type="button"
								class="inline-flex items-center gap-x-1.5 rounded-sm bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-xs hover:bg-indigo-500 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 w-full justify-center">
								<svg
									xmlns="http://www.w3.org/2000/svg"
									fill="none"
									viewBox="0 0 24 24"
									stroke-width="1.5"
									stroke="currentColor"
									class="size-6">
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										d="M7.217 10.907a2.25 2.25 0 1 0 0 2.186m0-2.186c.18.324.283.696.283 1.093s-.103.77-.283 1.093m0-2.186 9.566-5.314m-9.566 7.5 9.566 5.314m0 0a2.25 2.25 0 1 0 3.935 2.186 2.25 2.25 0 0 0-3.935-2.186Zm0-12.814a2.25 2.25 0 1 0 3.933-2.185 2.25 2.25 0 0 0-3.933 2.185Z" />
								</svg>

								Share Your Award
							</button>
						</div>
						<div class="flex flex-col md:flex-row">
							<button
								type="button"
								class="text-gray-900 w-full bg-white hover:bg-gray-100 border border-gray-200 focus:ring-4 focus:outline-none focus:ring-gray-100 font-medium rounded-sm text-sm px-3 py-2 text-center inline-flex justify-center items-center dark:focus:ring-gray-600 dark:bg-gray-800 dark:border-gray-700 dark:text-white dark:hover:bg-gray-700 me-2">
								Add to Linkedin Profile
							</button>
							<div class="flex gap-2">
								<div class="hidden md:block">
									<button
										type="button"
										class=" border border-gray-200 hover:border-blue-700 hover:text-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-sm text-sm text-center p-2.5 inline-flex items-center dark:border-blue-500 dark:text-gray-500 dark:hover:text-blue-800 dark:focus:ring-blue-800 dark:hover:bg-blue-500">
										<svg
											xmlns="http://www.w3.org/2000/svg"
											fill="none"
											viewBox="0 0 24 24"
											stroke-width="2"
											stroke="currentColor"
											class="size-4">
											<path
												stroke-linecap="round"
												stroke-linejoin="round"
												d="M3 16.5v2.25A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75V16.5M16.5 12 12 16.5m0 0L7.5 12m4.5 4.5V3" />
										</svg>

										<span class="sr-only">Icon description</span>
									</button>
								</div>
								<div class="flex-1 md:hidden">
									<button
										type="button"
										class=" border border-gray-200 hover:border-blue-700 hover:text-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-sm text-sm text-center p-2.5 inline-flex items-center dark:border-blue-500 dark:text-gray-500 dark:hover:text-blue-800 dark:focus:ring-blue-800 dark:hover:bg-blue-500">
										<svg
											xmlns="http://www.w3.org/2000/svg"
											fill="none"
											viewBox="0 0 24 24"
											stroke-width="2"
											stroke="currentColor"
											class="size-4">
											<path
												stroke-linecap="round"
												stroke-linejoin="round"
												d="M3 16.5v2.25A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75V16.5M16.5 12 12 16.5m0 0L7.5 12m4.5 4.5V3" />
										</svg>

										<span class="sr-only">Icon description</span>
									</button>
								</div>
								<span
									><button
										type="button"
										class=" border border-gray-200 hover:border-blue-700 hover:text-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-sm text-sm text-center p-2.5 inline-flex items-center dark:border-blue-500 dark:text-gray-500 dark:hover:text-blue-800 dark:focus:ring-blue-800 dark:hover:bg-blue-500">
										<svg
											xmlns="http://www.w3.org/2000/svg"
											fill="none"
											viewBox="0 0 24 24"
											stroke-width="1.5"
											stroke="currentColor"
											class="size-4">
											<path
												stroke-linecap="round"
												stroke-linejoin="round"
												d="M13.19 8.688a4.5 4.5 0 0 1 1.242 7.244l-4.5 4.5a4.5 4.5 0 0 1-6.364-6.364l1.757-1.757m13.35-.622 1.757-1.757a4.5 4.5 0 0 0-6.364-6.364l-4.5 4.5a4.5 4.5 0 0 0 1.242 7.244" />
										</svg>

										<span class="sr-only">Icon description</span>
									</button></span>
							</div>
						</div>
						<div class="flex flex-col gap-2 mt-2">
							<p class="text-sm leading-6">Want to report a typo or a mistake?</p>

							<p class="text-gray-500 dark:text-gray-400">
								<a
									href="#"
									class="inline-flex items-center text-sm text-blue-600 dark:text-blue-500 hover:underline">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										fill="none"
										viewBox="0 0 24 24"
										stroke-width="2"
										stroke="currentColor"
										class="size-4 me-1">
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
									</svg>

									Contact Issuer
								</a>
							</p>
						</div>
					</div>
				</div>
			

			<div class="py-6 lg:pl-8 xl:flex-1 xl:pl-6">
				<!-- Main area -->

				<div
					class="flex flex-col overflow-hidden rounded-sm border border-stroke-dark border-gray-200 bg-white p-4 md:p-4 gap-3">
					<div class="flex w-full justify-between">
						<div class="flex min-h-14 w-full items-center gap-3">
							<div class="flex w-full flex-col gap-1.5">
								<div class="flex items-center justify-between">
									<h4 class="text-xs font-medium uppercase leading-6 text-blue-500">Issued by</h4>
								</div>
								<div class="flex gap-2">
									<h2 class="text-2xl font-medium leading-[26px]">Keka HR</h2>
								</div>
							</div>
						</div>
					</div>
					<p class="text-sm leading-6">
						Keka is a cloud-based HR platform that simplifies and automates various HR processes,
						including payroll, time tracking, employee benefits, and performance management.
					</p>
				</div>
			</div>
		</div>
	</div>
</div>
<Footer />
