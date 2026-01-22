<script>
	import Header from '$quick-certify/common/navbar/header.svelte';
	import Footer from '$quick-certify/common/navbar/footer.svelte';
</script>

<Header />
<div class="bg-gray-50 h-screen p-8">
	<div class="max-w-7xl mx-auto rounded-sm border border-stroke-dark bg-white border-gray-200">
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
</div>
<Footer />
