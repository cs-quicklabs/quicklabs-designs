<script>
	 import NavBar from '$quick-certify/common/navbar/admin.svelte';
     import SideBar from '$quick-certify/common/navbar/account.svelte';
 
</script>

<NavBar />

<main class="max-w-7xl mx-auto pb-10 lg:py-12 lg:px-8">
	<div class="lg:grid lg:grid-cols-12 lg:gap-x-5">
		<!-- Left Sidebar -->
		<aside class="px-2 py-6 sm:px-6 lg:py-0 lg:px-0 lg:col-span-3">
			<SideBar />
		</aside>

		<!-- Main Content -->
		<main class="max-w-xl pb-12 px-4 lg:col-span-6">
			<div>
				<h1 class="form-title">Skills</h1>
				<p class="form-subtitle">
					Skills help categorize participants based on expertise. You can add, edit, or delete
					skills as needed.
				</p>

				<!-- Add Skill -->
				<form class="w-full mt-4">
					<div class="mb-4 mt-4">
						<label for="skill" class="form-input-label">Add New Skill</label>
						<input
							type="text"
							id="skill"
							class="form-input-field"
							placeholder="Enter skill name"
							required />
					</div>
					<button type="submit" class="btn-primary">Save</button>
				</form>

				<!-- Skills Table -->
				<div class="relative overflow-x-auto mt-4">
					<table class="w-full text-sm text-left text-gray-500">
						<thead class="text-xs text-gray-700 uppercase bg-gray-50">
							<tr>
								<th scope="col" class="px-6 py-4 w-full">Skill</th>
								<th scope="col" class="px-6 py-4">Action</th>
							</tr>
						</thead>
						<tbody>
							<tr class="odd:bg-white even:bg-gray-50 border-b border-gray-200">
								<th scope="row" class="px-6 py-4 form-text-normal">
									JavaScript
								</th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>

							<tr class="odd:bg-white even:bg-gray-50 border-b border-gray-200">
								<th scope="row" class="px-6 py-4 form-text-normal">
									Automation Testing
								</th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>

							<!-- Inline Edit Row -->
							<tr>
								<th class="p-2">
									<input
										type="text"
										class="form-input-field"
										value="API Testing"
										required />
								</th>
								<td>
									<button type="submit" class="btn-primary ml-2">Save</button>
								</td>
							</tr>
						</tbody>
					</table>
				</div>
			</div>
		</main>
	</div>
</main>
