<script>
	import SuperAdminNavBar from '$quick-learn/common/navbar/superadmin.svelte';
	import AdminNavBar from '$quick-learn/common/navbar/admin.svelte';
	import Editor from '$quick-learn/common/navbar/editor.svelte';
	import Member from '$quick-learn/common/navbar/member.svelte';
</script>

<div class="flex-row items-center justify-between p-4 space-y-3 sm:flex sm:space-y-0 sm:space-x-4">
	<div>
		<h5 class="mr-3 font-semibold dark:text-white">Super Admin Nav Bar</h5>
	</div>
</div>
<SuperAdminNavBar />
<div
	class="flex-row items-center justify-between p-4 space-y-3 sm:flex sm:space-y-0 sm:space-x-4 mt-10">
	<div>
		<h5 class="mr-3 font-semibold dark:text-white">Admin Nav Bar</h5>
	</div>
</div>

<AdminNavBar />
<div
	class="flex-row items-center justify-between p-4 space-y-3 sm:flex sm:space-y-0 sm:space-x-4 mt-10">
	<div>
		<h5 class="mr-3 font-semibold dark:text-white">Editor Nav Bar</h5>
	</div>
</div>

<Editor />
<div
	class="flex-row items-center justify-between p-4 space-y-3 sm:flex sm:space-y-0 sm:space-x-4 mt-10">
	<div>
		<h5 class="mr-3 font-semibold dark:text-white">Member Nav Bar</h5>
	</div>
</div>

<Member />
