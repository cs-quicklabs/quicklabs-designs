<script>
	let menu = $state({ opened: false });

	function toggle() {
		menu.opened = !menu.opened;
	}
</script>

<nav class="bg-gray-800">
	<div class="mx-auto px-2 sm:px-4 lg:px-8">
		<div class="relative flex h-12 items-center justify-between">
			<div class="flex items-center px-2 lg:px-0">
				<a href="/quick-certify">
					<div class="flex-shrink-0 flex items-center">
						<span
							data-cy="Quick Test-label"
							class="text-white font-extrabold font-mono px-3 hidden lg:block tracking-wider"
							>Quick Certify</span
						><span class="text-white font-medium px-3 block lg:hidden"></span>
					</div>
				</a>
				<div class="hidden lg:ml-4 lg:block">
					<div class="flex space-x-1">
						<!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
						<a href="/quick-certify/team" class="selected-nav">Dashboard</a>
						<a href="/quick-certify/member/my-learning-paths" class="unselected-nav">Events</a>
						<a href="/quick-certify/content" class="unselected-nav">Credentials</a>
						<a href="/quick-certify/designs" class="unselected-nav">Designs</a>
						<a href="/quick-certify/approvals" class="unselected-nav">Emails</a>
						<a href="/quick-certify/approvals" class="unselected-nav">Analytics</a>
						<a href="/quick-certify/approvals" class="unselected-nav">Integrations</a>
					</div>
				</div>
			</div>
			<div class="flex flex-1 justify-center px-2 lg:ml-6 lg:justify-end">
				<div class="w-full max-w-lg lg:max-w-xs">
					<label for="search" class="sr-only">Search</label>
					<div class="relative">
						<div class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-3"></div>
						<input
							id="search"
							name="search"
							class="block w-full form-input-field"
							placeholder="Search Events or Participants"
							type="search" />
					</div>
				</div>
			</div>
			<div class="flex lg:hidden">
				<!-- Mobile menu button -->
				<button
					type="button"
					class="inline-flex items-center justify-center rounded-sm p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
					aria-controls="mobile-menu"
					aria-expanded="false">
					<span class="sr-only">Open main menu</span>
					<!--
              Icon when menu is closed.
  
              Menu open: "hidden", Menu closed: "block"
            -->
					<svg
						class="block h-6 w-6"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						aria-hidden="true">
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
					</svg>
					<!--
              Icon when menu is open.
  
              Menu open: "block", Menu closed: "hidden"
            -->
					<svg
						class="hidden h-6 w-6"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						aria-hidden="true">
						<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
					</svg>
				</button>
			</div>
			<div class="hidden lg:ml-4 lg:block">
				<div class="flex items-center">
					<button
						type="button"
						class="flex-shrink-0 rounded-full bg-gray-800 p-1 text-gray-400 hover:text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800">
						<span class="sr-only">View notifications</span>
						<svg
							class="h-6 w-6"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							aria-hidden="true">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0" />
						</svg>
					</button>
					<!-- Profile dropdown -->
					<div class="relative ml-4 flex-shrink-0">
						<div>
							<button
								onclick={toggle}
								type="button"
								class="flex rounded-full bg-gray-800 text-sm text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800"
								id="user-menu-button"
								aria-expanded="false"
								aria-haspopup="true">
								<span class="sr-only">Open user menu</span>
								<img
									class="h-8 w-8 rounded-full"
									src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
									alt="" />
							</button>
						</div>
						<!--
                Dropdown menu, show/hide based on menu state.
  
                Entering: "transition ease-out duration-100"
                  From: "transform opacity-0 scale-95"
                  To: "transform opacity-100 scale-100"
                Leaving: "transition ease-in duration-75"
                  From: "transform opacity-100 scale-100"
                  To: "transform opacity-0 scale-95"
              -->
						{#if menu.opened}
							<div
								class="absolute right-0 z-10 mt-2 w-56 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg border border-gray-200 focus:outline-none"
								role="menu"
								aria-orientation="vertical"
								aria-labelledby="menu-button"
								tabindex="-1">
								<div class="px-4 py-3" role="none">
									<p class="text-xs" role="none">aashishd-yweir8832khsd@gmail.com</p>
									<p class="text-xs text-gray-700" role="none">Crownstack Technologies</p>
								</div>
								<div class="py-1" role="none">
									<a
										href="/quick-certify/settings/profile/general"
										class="text-gray-700 block px-4 py-2 text-sm hover:bg-gray-50"
										role="menuitem"
										tabindex="-1"
										id="menu-item-0"
										>Profile Settings
									</a>
									<a
										href="/quick-certify/settings/account/general-information"
										class="text-gray-700 block px-4 py-2 text-sm hover:bg-gray-50"
										role="menuitem"
										tabindex="-1"
										id="menu-item-0"
										>Account Settings
									</a>
									<a
										href="/quick-certify/settings/event/type"
										class="text-gray-700 block px-4 py-2 text-sm hover:bg-gray-50"
										role="menuitem"
										tabindex="-1"
										id="menu-item-0"
										>Event Settings
									</a>

									<a
										href="/quick-certify/settings/account/team"
										class="text-gray-700 block px-4 py-2 text-sm hover:bg-gray-50"
										role="menuitem"
										tabindex="-1"
										id="menu-item-0"
										>Team
									</a>
									<a
										href="/quick-certify/settings/archived/archived-member"
										class="text-gray-700 block px-4 py-2 text-sm hover:bg-gray-50"
										role="menuitem"
										tabindex="-1"
										id="menu-item-0"
										>Archived
									</a>
								</div>
								<div class="py-1" role="none">
									<a href="/quick-certify/login">
										<button
											type="submit"
											class=" hover:bg-gray-50 text-gray-700 block w-full px-4 py-2 text-left text-sm"
											role="menuitem"
											tabindex="-1"
											id="menu-item-3">Sign out</button>
									</a>
								</div>
							</div>
						{/if}
					</div>
				</div>
			</div>
		</div>
	</div>
</nav>
