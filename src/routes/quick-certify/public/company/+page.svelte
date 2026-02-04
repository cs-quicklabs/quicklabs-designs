<script>
	import Header from '$quick-certify/common/navbar/header.svelte';
	import Footer from '$quick-certify/common/navbar/footer.svelte';
</script>

<Header />
<div class="bg-gray-50 min-h-screen p-8">
	<div class="max-w-7xl mx-auto rounded-sm border border-gray-200 border-stroke-dark bg-white border-gray-200">
		<div>
			<img
				class="h-32 w-full object-cover lg:h-48"
				src="https://images.unsplash.com/photo-1444628838545-ac4016a5418a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80"
				alt="" />
		</div>
		<div class="mt-2 md:flex md:items-center md:justify-between p-4">
			<div class="min-w-0 flex-1">
				<h2 class="text-2xl/7 font-bold text-gray-900 sm:truncate sm:text-3xl sm:tracking-tight">
					Crownstack Technologies
				</h2>
			</div>
		</div>
	</div>
		<div class="p-8 flex flex-col lg:flex-row gap-8 max-w-7xl mx-auto">
			<!-- Left: Company Details -->
			<div class="flex-1 flex flex-col gap-4">
				<!-- Company Logo/Profile -->
				<div class="flex items-center space-x-4">
					<img
						class="h-20 w-20 rounded-full border border-gray-200 object-cover"
				src="https://images.unsplash.com/photo-1444628838545-ac4016a5418a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80"
						
						alt="Crownstack Logo"
					/>
					<div>
						<h3 class="text-xl font-semibold text-gray-800">Crownstack Technologies</h3>
						<p class="text-gray-500 text-sm">IT Services and Consulting</p>
					</div>
				</div>
				<!-- Company Info -->
				<div class="bg-gray-50 rounded border border-gray-200  p-4">
					<h4 class="font-medium text-gray-700 mb-2">About</h4>
					<p class="text-sm text-gray-600">
						Crownstack Technologies is a leading provider of digital solutions, offering expertise in enterprise software, web and mobile app development, and digital transformation for companies worldwide.
					</p>
				</div>
				<div class="grid grid-cols-1 md:grid-cols-2 gap-4">
					
					<div>
						<h5 class="font-medium text-gray-700 mb-1">Website</h5>
						<a href="https://crownstack.com" class="text-blue-600 hover:underline text-sm" target="_blank">crownstack.com</a>
					</div>
					<div>
						<h5 class="font-medium text-gray-700 mb-1">Email</h5>
						<a href="mailto:info@crownstack.com" class="text-sm text-blue-600 hover:underline">info@crownstack.com</a>
					</div>
					<div>
						<h5 class="font-medium text-gray-700 mb-1">Phone</h5>
						<p class="text-sm text-gray-600">+91 12345 67890</p>
					</div>
					<div>
						<h5 class="font-medium text-gray-700 mb-1">LinkedIn</h5>
						<a href="https://linkedin.com/company/crownstack" class="text-sm text-blue-600 hover:underline flex items-center gap-1.5" target="_blank">
							<svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
								<path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
							</svg>
							linkedin.com/company/crownstack
						</a>
					</div>
					<div>
						<h5 class="font-medium text-gray-700 mb-1">Twitter</h5>
						<a href="https://twitter.com/crownstack" class="text-sm text-blue-600 hover:underline flex items-center gap-1.5" target="_blank">
							<svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
								<path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"/>
							</svg>
							twitter.com/crownstack
						</a>
					</div>
				</div>
			</div>

			<!-- Right: Recent Certificates Issued -->
			<div class="flex-1 flex flex-col gap-6">
				<div>
					<h4 class="font-semibold text-gray-800 text-lg mb-3">Recent Certificates Issued</h4>
					<ul class="divide-y divide-gray-100 border border-gray-200 rounded-xs bg-white">
						<li class="flex items-center gap-3 p-4">
							<img src="/quick-certify/rashi.png" class="w-20 h-14 object-cover rounded-sm border shadow-md flex-shrink-0" alt="Certificate Thumbnail">
							<div>
								<div class="font-medium text-gray-900">
									Certificate of Excellence
								</div>
								<div class="text-xs text-gray-500">
									<span>25 Jun 2024</span>
								</div>
								<div class="text-xs text-gray-500 mt-1">
									Issued to Ankit Jain
								</div>
							</div>
						</li>
						<li class="flex items-center gap-3 p-4">
							<img src="/quick-certify/rashi.png" class="w-20 h-14 object-cover rounded-sm border shadow-md flex-shrink-0" alt="Certificate Thumbnail">
							<div>
								<div class="font-medium text-gray-900">
									Top Performer Badge
								</div>
								<div class="text-xs text-gray-500">
									<span>18 Jun 2024</span>
								</div>
								<div class="text-xs text-gray-500 mt-1">
									Issued to Riya Shah
								</div>
							</div>
						</li>
						<li class="flex items-center gap-3 p-4">
							<img src="/quick-certify/rashi.png" class="w-20 h-14 object-cover rounded-sm border shadow-md flex-shrink-0" alt="Certificate Thumbnail">
							<div>
								<div class="font-medium text-gray-900">
									Course Completion Certificate
								</div>
								<div class="text-xs text-gray-500">
									<span>04 Jun 2024</span>
								</div>
								<div class="text-xs text-gray-500 mt-1">
									Issued to Rahul Kumar
								</div>
							</div>
						</li>
					</ul>
				</div>

				<!-- Company Contact/Message Section -->
				<div class="bg-gray-50 rounded border border-gray-200 p-4">
					<h4 class="font-semibold text-gray-800 mb-4">Contact Crownstack</h4>
					<form class="flex flex-col gap-3">
						<input
							type="text"
							placeholder="Your Name"
							class="form-input-field"
							required
						/>
						<input
							type="email"
							placeholder="Your Email"
							class="form-input-field"
							required
						/>
						<textarea
							placeholder="Write your message..."
							rows="4"
							class="form-input-field resize-none"
						></textarea>
						<button type="submit" class="btn-primary w-full mt-1">Send Message</button>
					</form>
				</div>
			</div>
		</div>
	</div>
<Footer />