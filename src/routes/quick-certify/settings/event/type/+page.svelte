<script>
	import NavBar from '$quick-certify/common/navbar/admin.svelte';
	import EventSettingsNavBar from '$quick-certify/common/navbar/event.svelte';
</script>

<NavBar />

<main class="max-w-7xl mx-auto pb-10 lg:py-12 lg:px-8">
	<div class="lg:grid lg:grid-cols-12 lg:gap-x-5">
		<aside class="px-2 py-6 sm:px-6 lg:py-0 lg:px-0 lg:col-span-3">
			<EventSettingsNavBar />
		</aside>

		<main class="max-w-xl pb-12 px-4 lg:col-span-6">
			<div>
				<h1 class="form-title">Event Types</h1>
				<p class="form-subtitle">
					Event types specify the category of the event. For example, a conference, workshop, or
					seminar. You can add new event types, edit existing ones, or delete them.
				</p>

				<form class="w-full mt-6">
					<div class="">
						<label for="email" class="form-input-label">Add New Event Type</label>
						<input
							type="email"
							id="email"
							class="form-input-field"
							placeholder="New Event Type"
							required />
					</div>
					<button type="submit" class="btn-primary mt-4">Save</button>
				</form>

				<div class="relative overflow-x-auto mt-8">
					<table class="w-full text-sm text-left rtl:text-right text-gray-500 dark:text-gray-400">
						<thead
							class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
							<tr>
								<th scope="col" class="px-6 py-3 w-full">Event Type</th>
								<th scope="col" class="px-6 py-3"> Action </th>
							</tr>
						</thead>
						<tbody>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50  even:dark:bg-gray-800 border-b border-gray-200 dark:border-gray-700">
								<th scope="row" class="px-6 py-4 form-text-normal"> Achievent Award </th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 border-gray-200 even:dark:bg-gray-800 border-b  dark:border-gray-700">
								<th scope="row" class="px-6 py-4 form-text-normal"> Certification </th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-b border-gray-200 dark:border-gray-700">
							</tr>
							<tr>
								<th class="p-2">
									<input
										type="text"
										id="last_name"
										class="form-input-field"
										placeholder="Engineering"
										value="Conference"
										required />
								</th>
								<td>
									<button type="submit" class="btn-primary">Save</button>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-b border-gray-200 dark:border-gray-700 border-t">
								<th scope="row" class="px-6 py-4 form-text-normal"> Course </th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-gray-200 border-b dark:border-gray-700 border-t">
								<th scope="row" class="px-6 py-4 form-text-normal"> Memebership </th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-gray-200 border-b dark:border-gray-700 border-t">
								<th scope="row" class="px-6 py-4 form-text-normal"> Licence </th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-gray-200 border-b dark:border-gray-700 border-t">
								<th scope="row" class="px-6 py-4 form-text-normal"> Training </th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800  border-gray-200 border-b dark:border-gray-700 border-t">
								<th scope="row" class="px-6 py-4 form-text-normal"> Webinar </th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-gray-200 border-b dark:border-gray-700 border-t">
								<th scope="row" class="px-6 py-4 form-text-normal"> Seminar </th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800  border-gray-200 border-b dark:border-gray-700 border-t">
								<th scope="row" class="px-6 py-4 form-text-normal"> Workshop </th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>
							<tr
								class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-gray-200 border-b dark:border-gray-700 border-t">
								<th scope="row" class="px-6 py-4 form-text-normal"> Other </th>
								<td class="px-6 py-4 inline-flex">
									<a href="#" class="btn-inline-blue">Edit</a>
									<a href="#" class="ml-2 btn-inline-red">Delete</a>
								</td>
							</tr>
						</tbody>
					</table>
				</div>
			</div>
		</main>
	</div>
</main>
