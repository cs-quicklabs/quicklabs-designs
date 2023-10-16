<script>
    import Fullnavbar from '$lib/quick-test/fullnavbar.svelte';
    import ProfileSidebar from '$lib/quick-test/profilesidebar.svelte';
</script>
<Fullnavbar/>
<div class="mx-auto max-w-7xl pt-16 lg:flex lg:gap-x-16 lg:px-8">
    <ProfileSidebar/>
    <div class="">
        <h2 class="text-base font-semibold leading-7 text-gray-900">Change Password</h2>
        <p class="mt-1 text-sm leading-6 text-gray-600">Change your old password and set a new one.</p>
        <div class="mt-4 grid grid-cols-1 gap-x-6 gap-y-6 sm:grid-cols-6">
            <div class="col-span-full   ">
                <label for="email" class="block text-sm font-medium leading-6 text-gray-900">Old Password</label>
                <div class="mt-2">
                    <input
                        id="email"
                        name="email"
                        type="email"
                        autocomplete="email"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-1 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                    >
                </div>
            </div>
            <div class="col-span-full   ">
                <label for="email" class="block text-sm font-medium leading-6 text-gray-900">New Password</label>
                <div class="mt-2">
                    <input
                        id="email"
                        name="email"
                        type="email"
                        autocomplete="email"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-1 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                    >
                </div>
            </div>
            <div class="col-span-full   ">
                <label for="email" class="block text-sm font-medium leading-6 text-gray-900">Confirm Password</label>
                <div class="mt-2">
                    <input
                        id="email"
                        name="email"
                        type="email"
                        autocomplete="email"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-1 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                    >
                </div>
            </div>
            <div class="sm:col-span-2 invisible">
                <label for="postal-code" class="block text-sm font-medium leading-6 text-gray-900">ZIP / Postal code</label>
                <div class="mt-2">
                    <input
                        type="text"
                        name="postal-code"
                        id="postal-code"
                        autocomplete="postal-code"
                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-1 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                    >
                </div>
            </div>
        </div>
        <div class="-mt-14 flex items-center justify-end gap-x-6">
            <button type="submit" class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Save</button>
        </div>
    </div>
</div>
