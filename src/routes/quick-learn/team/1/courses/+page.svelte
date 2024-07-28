<script>
	import NavBar from '$quick-learn/common/navbar/admin.svelte';
</script>

<NavBar />
<main>
	<div class="bg-gray-50 relative z-0 flex-1 overflow-x-scroll focus:outline-none h-screen">
		<div class="px-4 py-4 sm:flex sm:items-center sm:justify-center sm:px-6 lg:px-8">
			<nav class="flex" aria-label="Breadcrumb">
				<ol class="inline-flex justify-self-center space-x-1 md:space-x-2 rtl:space-x-reverse">
					<li class="inline-flex items-center">
						<a
							href="/quick-learn/team"
							class="inline-flex items-center text-sm font-medium text-gray-700 hover:text-blue-600 dark:text-gray-400 dark:hover:text-white hover:underline">
							<svg
								class="w-3 h-3 me-2.5"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								fill="currentColor"
								viewBox="0 0 20 20">
								<path
									d="m19.707 9.293-2-2-7-7a1 1 0 0 0-1.414 0l-7 7-2 2a1 1 0 0 0 1.414 1.414L2 10.414V18a2 2 0 0 0 2 2h3a1 1 0 0 0 1-1v-4a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v4a1 1 0 0 0 1 1h3a2 2 0 0 0 2-2v-7.586l.293.293a1 1 0 0 0 1.414-1.414Z" />
							</svg>
							Team
						</a>
					</li>
					<li>
						<div class="flex items-center">
							<svg
								class="rtl:rotate-180 w-3 h-3 text-gray-400 mx-1"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 6 10">
								<path
									stroke="currentColor"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="m1 9 4-4-4-4" />
							</svg>
							<a
								href="1"
								class="ms-1 text-sm font-medium text-gray-700 hover:text-blue-600 md:ms-2 dark:text-gray-400 dark:hover:text-white hover:underline"
								>Aashish Dhawan</a>
						</div>
					</li>
					<li>
						<div class="flex items-center">
							<svg
								class="rtl:rotate-180 w-3 h-3 text-gray-400 mx-1"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 6 10">
								<path
									stroke="currentColor"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="m1 9 4-4-4-4" />
							</svg>
							<a
								href="1"
								class="ms-1 text-sm font-medium text-gray-700 hover:text-blue-600 md:ms-2 dark:text-gray-400 dark:hover:text-white hover:underline"
								>HTML Course</a>
						</div>
					</li>
				</ol>
			</nav>
		</div>
		<div class="px-4 mb-8 sm:flex sm:items-center sm:justify-center sm:px-6 lg:px-8">
			<div class="items-baseline">
				<h1 class="text-5xl font-extrabold leading-tight">Aashish Dhawan</h1>
				<p
					class="mt-1 ml-1 text-sm text-gray-500 truncate sm:flex sm:items-center sm:justify-center">
					(20 lessons)
				</p>
			</div>
		</div>

		<div class="px-8 py-8 sm:flex sm:items-center sm:justify-between sm:px-6 lg:px-8">
			<div class="flex flex-wrap items-baseline -mt-2 -ml-2">
				<h1 class="text-3xl font-bold leading-tight">HTML Course</h1>
				<p class="mt-1 ml-1 text-sm text-gray-500 truncate">(19 lessons)</p>
			</div>
		</div>
		<div class="relative px-6 grid gap-10 pb-16" id="release_notes">
			<div id="created-spaces">
				<ul
					role="list"
					class="grid grid-cols-2 gap-x-2 gap-y-4 sm:grid-cols-3 sm:gap-x-4 lg:grid-cols-6 2xl:grid-cols-8 xl:gap-x-6">
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/mine">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-48">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									First HTML Code
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<div class="items-center space-x-1 py-3 flex font-medium text-green-500">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										viewBox="0 0 20 20"
										fill="currentColor"
										class="w-4 h-4"
										aria-hidden="true">
										<path
											fill-rule="evenodd"
											d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
											clip-rule="evenodd" />
									</svg>
									<p class="flex-wrap text-xs text-gray-400 line-clamp-2">
										Completed on June 12, 2024
									</p>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/mine">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-48">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									First HTML Code
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<div class="items-center space-x-1 py-3 flex font-medium text-green-500">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										viewBox="0 0 20 20"
										fill="currentColor"
										class="w-4 h-4"
										aria-hidden="true">
										<path
											fill-rule="evenodd"
											d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
											clip-rule="evenodd" />
									</svg>
									<p class="text-xs text-gray-400 line-clamp-2">Completed on June 12, 2024</p>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/mine">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-48">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									Exploring the document
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<div class="items-center space-x-1 py-3 flex font-medium text-green-500">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										viewBox="0 0 20 20"
										fill="currentColor"
										class="w-4 h-4"
										aria-hidden="true">
										<path
											fill-rule="evenodd"
											d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
											clip-rule="evenodd" />
									</svg>
									<p class="text-xs text-gray-400 line-clamp-2">Completed on June 12, 2024</p>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/mine">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-48">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									Comments, White Space and line breaks
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<div class="items-center space-x-1 py-3 flex font-medium text-green-500">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										viewBox="0 0 20 20"
										fill="currentColor"
										class="w-4 h-4"
										aria-hidden="true">
										<path
											fill-rule="evenodd"
											d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
											clip-rule="evenodd" />
									</svg>
									<p class="text-xs text-gray-400 line-clamp-2">Completed on June 12, 2024</p>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/mine">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-48">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									The Rest of the HTML tags
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<div class="items-center space-x-1 py-3 flex font-medium text-green-500">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										viewBox="0 0 20 20"
										fill="currentColor"
										class="w-4 h-4"
										aria-hidden="true">
										<path
											fill-rule="evenodd"
											d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
											clip-rule="evenodd" />
									</svg>
									<p class="text-xs text-gray-400 line-clamp-2">Completed on June 12, 2024</p>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg bg-white shadow-sm hover:shadow-lg border-gray-100 group"
						id="space_8">
						<a href="/quick-learn/content/lesson/mine">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-48">
								<h1 id="message-heading" class="font-medium text-gray-900 group-hover:underline">
									Inserting Pictures and Styling
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
								<div class="items-center space-x-1 py-3 flex font-medium text-green-500">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										viewBox="0 0 20 20"
										fill="currentColor"
										class="w-4 h-4"
										aria-hidden="true">
										<path
											fill-rule="evenodd"
											d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
											clip-rule="evenodd" />
									</svg>
									<p class="text-xs text-gray-400 line-clamp-2">Completed on June 12, 2024</p>
								</div>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg shadow-sm border-gray-100 group bg-gray-100 cursor-default"
						id="space_8">
						<a href="/quick-learn/content/lesson/mine">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-48">
								<h1 id="message-heading" class="font-medium text-gray-900">
									Inserting Pictures and Styling
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
							</div>
						</a>
					</li>
					<li
						class="col-span-1 rounded-lg shadow-sm border-gray-100 group bg-gray-100"
						id="space_8">
						<a href="/quick-learn/content/lesson/mine">
							<div class="flex-wrap py-4 px-6 text-gray-900 h-48">
								<h1 id="message-heading" class="font-medium text-gray-900">
									Inserting Pictures Via CSS
								</h1>
								<p class="font-normal text-sm text-gray-500 line-clamp-3 mt-2">
									Learn Git basics in this course. This shows first three lines of the content and
									whatever lesson contains
								</p>
							</div>
						</a>
					</li>
				</ul>
			</div>
		</div>
	</div>
</main>
