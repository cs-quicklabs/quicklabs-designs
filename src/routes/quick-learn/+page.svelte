<script>
	let login = [
		{ title: 'Login', link: '/quick-learn/login' },
		{ title: 'Forgot Password', link: '/quick-learn/forgot-password' },
		{ title: 'Reset Password', link: '/quick-learn/reset-password' },
		{ title: 'Navbars', link: '/quick-learn/navbars' }
	];

	let team = [
		{ title: 'Team', link: '/quick-learn/team' },
		{ title: 'Add Member', link: '/quick-learn/team/add' },
		{ title: 'Edit Member', link: '/quick-learn/team/edit' },
		{ title: 'Member Details', link: '/quick-learn/team/1' },
		{ title: 'Member Roadmap Details', link: '/quick-learn/team/1/roadmaps' },
		{ title: 'Member Courses Details', link: '/quick-learn/team/1/courses' }
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
		{ title: 'Roadmap Detail', link: '/quick-learn/member/roadmap' },
		{ title: 'Course Detail', link: '/quick-learn/member/course' }
	];

	let contentRepository = [
		{ title: 'Content', link: '/quick-learn/content' },
		{ title: 'Content Roadmap', link: '/quick-learn/content/roadmap' },
		{ title: 'Content Course', link: '/quick-learn/content/roadmap/course' }
	];

	let archive = [
		{ title: 'Archived Roadmaps', link: '/quick-learn/archive/roadmaps' },
		{ title: 'Archived Courses', link: '/quick-learn/archive/courses' },
		{ title: 'Archived Lessons', link: '/quick-learn/archive/lessons' },
		{ title: 'Archived Users', link: '/quick-learn/archive/users' }
	];

	let lesssons = [
		{ title: 'From Email', link: '/quick-learn/content/lesson/email' },
		{ title: 'From My Learing Path', link: '/quick-learn/content/lesson/mine' },
		{ title: 'Viewing Others Profile', link: '/quick-learn/content/lesson/other' },
		{ title: 'Editor View', link: '/quick-learn/content/lesson/editor' },
		{ title: 'Edit Lesson', link: '/quick-learn/content/lesson/edit' },
		{ title: 'Normal Lesson view', link: '/quick-learn/content/lesson/normal' }
	];

	let workflows2 = [
		{ title: 'Member', screens: memberScreens },
		{ title: 'Content Repository', screens: contentRepository },
		{ title: 'Lesson', screens: lesssons },
		{ title: 'Archive', screens: archive }
	];

	let community = [
		{ title: 'Community Courses List', link: '/quick-learn/community' },
		{ title: 'Community Course', link: '/quick-learn/community/course' },
		{ title: 'Community Course Lesson', link: '/quick-learn/content/lesson/normal' }
	];

	let workflows3 = [{ title: 'Community', screens: community }];
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
							class="sticky top-0 z-10 border-t border-b border-gray-200 bg-gray-200 px-6 py-1 text-sm font-medium text-gray-500">
							<h3>{workflow.title}</h3>
						</div>
						<ul role="list" class="relative z-0 divide-y divide-gray-200">
							{#each workflow.screens as screen}
								<li class="bg-white">
									<div
										class="relative flex items-center space-x-3 px-6 py-2 focus-within:ring-2 focus-within:ring-inset
								focus-within:ring-indigo-500 hover:bg-gray-50">
										<div class="min-w-0 flex-1">
											<a href={screen.link} target="_blank" class="focus:outline-none">
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
							class="sticky top-0 z-10 border-t border-b border-gray-200 bg-gray-200 px-6 py-1 text-sm font-medium text-gray-500">
							<h3>{workflow.title}</h3>
						</div>
						<ul role="list" class="relative z-0 divide-y divide-gray-200">
							{#each workflow.screens as screen}
								<li class="bg-white">
									<div
										class="relative flex items-center space-x-3 px-6 py-2 focus-within:ring-2 focus-within:ring-inset
							focus-within:ring-indigo-500 hover:bg-gray-50">
										<div class="min-w-0 flex-1">
											<a href={screen.link} target="_blank" class="focus:outline-none">
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
					{#each workflows3 as workflow}
						<div
							class="sticky top-0 z-10 border-t border-b border-gray-200 bg-gray-200 px-6 py-1 text-sm font-medium text-gray-500">
							<h3>{workflow.title}</h3>
						</div>
						<ul role="list" class="relative z-0 divide-y divide-gray-200">
							{#each workflow.screens as screen}
								<li class="bg-white">
									<div
										class="relative flex items-center space-x-3 px-6 py-2 focus-within:ring-2 focus-within:ring-inset
						focus-within:ring-indigo-500 hover:bg-gray-50">
										<div class="min-w-0 flex-1">
											<a href={screen.link} target="_blank" class="focus:outline-none">
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
