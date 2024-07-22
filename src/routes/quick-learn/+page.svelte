<script>
	let login = [
		{ title: 'Login', link: '/quick-learn/login' },
		{ title: 'Forgot Password', link: '/quick-learn/forgot-password' },
		{ title: 'Reset Password', link: '/quick-learn/reset-password' }
	];

	let team = [
		{ title: 'Team', link: '/quick-learn/team' },
		{ title: 'Add Member', link: '/quick-learn/team/add' },
		{ title: 'Edit Member', link: '/quick-learn/team/edit' }
	];

	let profileSettings = [
		{ title: 'General', link: '/quick-learn/settings/profile/general' },
		{ title: 'Change Password', link: '/quick-learn/settings/profile/password' },
		{ title: 'Preferences', link: '/quick-learn/settings/profile/preferences' }
	];

	let accountSettings = [
		{ title: 'General', link: '/quick-learn/settings/team/general' },
		{ title: 'Primary Skills', link: '/quick-learn/settings/team/skills' },
		{ title: 'Skill Delete Error', link: '/quick-learn/settings/team/error' },
		{ title: 'Roadmap Categories', link: '/quick-learn/settings/team/roadmap-categories' },
		{ title: 'Courses Categories', link: '/quick-learn/settings/team/courses-categories' }
	];

	let workflows = [
		{ title: 'Login', screens: login },
		{ title: 'Team', screens: team },
		{ title: 'Profile Settings', screens: profileSettings },
		{ title: 'Account Settings', screens: accountSettings }
	];

	let memberScreens = [
		{ title: 'My Learning Paths', link: '/quick-learn/member/my-learning-paths' },
		{ title: 'Roadmap Detail', link: '/quick-learn/member/roadmap' }
	];

	let workflows2 = [{ title: 'Member', screens: memberScreens }];
</script>

<!-- 3 column wrapper -->
<div class="mx-auto w-full flex-grow lg:flex">
	<!-- Left sidebar & main wrapper -->
	<div class="min-w-0 flex-1 bg-white xl:flex">
		<div
			class="border-b border-gray-200 bg-white xl:w-64 xl:flex-shrink-0 xl:border-b-0 xl:border-r xl:border-gray-200">
			<div class="h-full sm:pl-6 lg:pl-8 xl:pl-0">
				<!-- Start left column area -->
				<div class="relative">
					{#each workflows as workflow}
						<div
							class="sticky top-0 z-10 border-t border-b border-gray-200 bg-gray-50 px-6 py-1 text-sm font-medium text-gray-500">
							<h3>{workflow.title}</h3>
						</div>
						<ul role="list" class="relative z-0 divide-y divide-gray-200">
							{#each workflow.screens as screen}
								<li class="bg-white">
									<div
										class="relative flex items-center space-x-3 px-6 py-2 focus-within:ring-2 focus-within:ring-inset
								focus-within:ring-indigo-500 hover:bg-gray-50">
										<div class="min-w-0 flex-1">
											<a href={screen.link} class="focus:outline-none">
												<p class="text-sm font-medium text-gray-900">{screen.title}</p>
											</a>
										</div>
									</div>
								</li>
							{/each}
						</ul>
					{/each}
				</div>
				<!-- End left column area -->
			</div>
		</div>

		<div
			class="border-b border-gray-200 bg-white xl:w-64 xl:flex-shrink-0 xl:border-b-0 xl:border-r xl:border-gray-200">
			<div class="h-full sm:pl-6 lg:pl-8 xl:pl-0">
				<!-- Start left column area -->
				<div class="relative">
					{#each workflows2 as workflow}
						<div
							class="sticky top-0 z-10 border-t border-b border-gray-200 bg-gray-50 px-6 py-1 text-sm font-medium text-gray-500">
							<h3>{workflow.title}</h3>
						</div>
						<ul role="list" class="relative z-0 divide-y divide-gray-200">
							{#each workflow.screens as screen}
								<li class="bg-white">
									<div
										class="relative flex items-center space-x-3 px-6 py-2 focus-within:ring-2 focus-within:ring-inset
							focus-within:ring-indigo-500 hover:bg-gray-50">
										<div class="min-w-0 flex-1">
											<a href={screen.link} class="focus:outline-none">
												<p class="text-sm font-medium text-gray-900">{screen.title}</p>
											</a>
										</div>
									</div>
								</li>
							{/each}
						</ul>
					{/each}
				</div>
				<!-- End left column area -->
			</div>
		</div>
	</div>
</div>
