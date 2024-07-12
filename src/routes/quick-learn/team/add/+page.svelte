<script>
	import NavBar from '$quick-learn/common/navbar/admin.svelte';
</script>

<NavBar />
<main>
	<section class="bg-white dark:bg-gray-900">
		<div class="py-8 px-4 mx-auto max-w-2xl lg:py-8">
			<div>
				<h1 class="text-lg font-semibold dark:text-white">Add New Team Member</h1>
				<p class="text-gray-500 dark:text-gray-400 text-sm">
					Please fill in details of new team member.
				</p>
			</div>

			<form id="new_user" action="/members" accept-charset="UTF-8" method="post">
				<div class="mt-4 grid gap-4 sm:grid-cols-2 sm:gap-6">
					<div>
						<div>
							<label
								class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
								for="user_first_name">First Name</label>
							<div class="mt-1">
								<input
									class="appearance-none block bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-sm focus:ring-primary-600 focus:border-primary-600 block w-full p-1.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
									required="required"
									type="text"
									name="user[first_name]"
									id="user_first_name" />
							</div>
						</div>
					</div>
					<div>
						<div>
							<label
								class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
								for="user_last_name">Last Name</label>
							<div class="mt-1">
								<input
									class="appearance-none block bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-sm focus:ring-primary-600 focus:border-primary-600 block w-full p-1.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
									required="required"
									type="text"
									name="user[last_name]"
									id="user_last_name" />
							</div>
						</div>
					</div>
					<div>
						<div>
							<label
								class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
								for="user_email">Email</label>
							<div class="mt-1">
								<input
									class="appearance-none block bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-sm focus:ring-primary-600 focus:border-primary-600 block w-full p-1.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
									required="required"
									type="text"
									name="user[email]"
									id="user_email" />
							</div>
						</div>
					</div>
					<div>
						<label
							for="user-role"
							class="inline-flex items-center mb-2 text-sm font-medium text-gray-900 dark:text-white">
							User Role
							<button
								type="button"
								data-tooltip-target="tooltip-user-role"
								data-tooltip-style="dark"
								class="ml-1">
								<svg
									aria-hidden="true"
									class="w-4 h-4 text-gray-400 hover:text-gray-900 dark:hover:text-white dark:text-gray-500"
									fill="currentColor"
									viewBox="0 0 20 20"
									xmlns="http://www.w3.org/2000/svg"
									><path
										fill-rule="evenodd"
										d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-8-3a1 1 0 00-.867.5 1 1 0 11-1.731-1A3 3 0 0113 8a3.001 3.001 0 01-2 2.83V11a1 1 0 11-2 0v-1a1 1 0 011-1 1 1 0 100-2zm0 8a1 1 0 100-2 1 1 0 000 2z"
										clip-rule="evenodd"></path
									></svg>
								<span class="sr-only">Show information</span>
							</button>
							<div
								id="tooltip-user-role"
								role="tooltip"
								class="inline-block absolute invisible z-10 py-1 px-2 max-w-sm text-xs font-normal text-white bg-gray-900 rounded-sm shadow-sm opacity-0 tooltip dark:bg-gray-700"
								data-popper-placement="top"
								style="position: absolute; inset: auto auto 0px 0px; margin: 0px; transform: translate3d(606px, -345.5px, 0px);">
								A team member can be either Super Admin, Admin, Editor or Member.
								<div
									class="tooltip-arrow"
									data-popper-arrow=""
									style="position: absolute; left: 0px; transform: translate3d(192px, 0px, 0px);">
								</div>
							</div>
						</label>
						<select
							name="user[role]"
							id="bucket"
							class="appearance-none block bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-sm focus:ring-primary-600 focus:border-primary-600 block w-full p-1.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
							><option value="data">Admin</option>
							<option value="recruiter">Editor</option>
							<option value="interviewer">Member</option>
						</select>
					</div>
					<div>
						<div>
							<label
								class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
								for="user_password">New Password</label>
							<div class="mt-1">
								<input
									class="appearance-none block bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-sm focus:ring-primary-600 focus:border-primary-600 block w-full p-1.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
									required="required"
									type="password"
									name="user[password]"
									id="user_password" />
							</div>
						</div>
					</div>
					<div>
						<div>
							<label
								class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
								for="user_password_confirmation">Confirm New Password</label>
							<div class="mt-1">
								<input
									class="appearance-none block bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-sm focus:ring-primary-600 focus:border-primary-600 block w-full p-1.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
									required="required"
									type="password"
									name="user[password_confirmation]"
									id="user_password_confirmation" />
							</div>
						</div>
					</div>
					<div>
						<label
							for="user-role"
							class="inline-flex items-center mb-2 text-sm font-medium text-gray-900 dark:text-white">
							Primary Skill
						</label>
						<select
							name="user[role]"
							id="bucket"
							class="appearance-none block bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-sm focus:ring-primary-600 focus:border-primary-600 block w-full p-1.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
							><option value="data">iOS Developer</option>
							<option value="recruiter">Android Developer</option>
							<option value="interviewer">React Developer</option>
						</select>
					</div>
				</div>

				<button type="submit" class="btn-primary mt-6"> Add Member </button>
				<a class="btn-secondary" href="/quick-learn">Cancel</a>
			</form>
		</div>
	</section>
</main>
