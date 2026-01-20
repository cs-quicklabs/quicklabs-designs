<script>
	const onboarding = [
		{
			title: 'Login',
			link: '/quick-certify/login'
		},
		{
			title: 'Forgot Password',
			link: '/quick-certify/forgot-password'
		},
		{
			title: 'Reset Password',
			link: '/quick-certify/reset-password'
		},
		{
			title: 'Signup',
			link: '/quick-certify/signup'
		},
		{
			title: 'Google Signup',
			link: '/quick-certify/signup/complete'
		}
	];

	let profileSettings = [
		{ title: 'General', link: '/quick-certify/settings/profile/general' },
		{ title: 'Change Password', link: '/quick-certify/settings/profile/password' },
		{ title: 'Change Password (Google)', link: '/quick-certify/settings/profile/password-google' },
		{ title: 'Preferences', link: '/quick-certify/settings/profile/preferences' }
	];
	let accountSettings = [
		{ title: 'General Information', link: '/quick-certify/settings/account/general-information' },
		{ title: 'Social Links', link: '/quick-certify/settings/account/social-links' },
		{ title: 'Branding', link: '/quick-certify/settings/account/branding' },
		{ title: 'Issuer Portal', link: '/quick-certify/settings/account/issuer-portal' },
		{ title: 'Billing Information', link: '/quick-certify/settings/account/billing-information' },
		{ title:'Skills', link: '/quick-certify/settings/account/skill'}

	];
	let teamSettings = [
		{ title: 'Team', link: '/quick-certify/settings/account/team' },
		{ title: 'Add Member', link: '/quick-certify/settings/account/team/add' },
		{ title: 'Edit Member', link: '/quick-certify/settings/account/team/edit' }
	];

	let eventSettings = [
		{ title: 'Event Types', link: '/quick-certify/settings/event/type' },
		{ title: 'Event Levels', link: '/quick-certify/settings/event/level' },
		{ title: 'Event Formats', link: '/quick-certify/settings/event/format' }
	];

	let Designs = [
		{ title: 'Design List', link: '/quick-certify/designs'},
		{ title: 'Add Design', link: '/quick-certify/designs/add-design' },
		{ title: 'Edit Design', link: '/quick-certify/designs/edit-design' }
	];

	let Archived = [
		{title:'Archived Member', link:'/quick-certify/settings/archived/archived-member'}
	]


	

	let settingWorkflows = [
		{ title: 'Onboarding', screens: onboarding },
		{ title: 'Personal Settings', screens: profileSettings },
		{ title: 'Account Settings', screens: accountSettings },
		{ title: 'Team', screens: teamSettings },
		{title:'Archived',screens:Archived}
	];

	let publicPages = [
		{ title: 'Certificate Detail', link: '/quick-certify/public/credential' },
		{ title: 'Event Detail', link: '/quick-certify/public/event/1' },
		{ title: 'Event Participants List', link: '/quick-certify/public/event/1/participants' },
		{ title: 'Issuer Profile', link: '/quick-certify/public/company' },
		{ title: 'Issuer Recipients List', link: '/quick-certify/public/recipients' },
		{ title: 'Issuer Events List', link: '/quick-certify/public/event' },
		{ title: 'Issuer Participant Detail', link: '/quick-certify/public/event/1/person' },
		{ title: 'Person Detail', link: '/quick-certify/public/person' }
	];

	let publicWorkflows = [
		{ title: 'Public', screens: publicPages },
		{ title: 'Event Settings', screens: eventSettings },
				{ title: 'Designs', screens: Designs },

	];
</script>

<!-- 3 column wrapper -->
<div class="mx-auto w-full flex-grow lg:flex">
	<!-- Left sidebar & main wrapper -->
	<div class="min-w-0 flex-1 bg-white xl:flex">
		<div class="border-b border-gray-200 bg-white xl:w-64 xl:flex-shrink-0 xl:border-b-0 border-r">
			<div class="h-full sm:pl-6 lg:pl-8 xl:pl-0">
				<!-- Start left column area -->
				<div class="relative">
					{#each settingWorkflows as workflow}
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
		<div class="border-b border-gray-200 bg-white xl:w-64 xl:flex-shrink-0 xl:border-b-0 border-r">
			<div class="h-full sm:pl-6 lg:pl-8 xl:pl-0">
				<!-- Start left column area -->
				<div class="relative">
					{#each publicWorkflows as workflow}
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
