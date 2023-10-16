<script>
	import { goto } from '$app/navigation';
	import Fullnavbar from '$lib/quick-test/fullnavbar.svelte';
	let menu = { opened: false, filter: false };

	function toggle() {
		menu.opened = !menu.opened;
	}

	function filter() {
		menu.filter = !menu.filter;
	}
</script>
<Fullnavbar/>
<div class="mx-auto px-4 pt-4 sm:px-6 lg:px-8">
    <div class="flex">
        <h1 class="flex-1 text-2xl font-bold text-gray-900">Projects</h1>
        <div class="flex items-center justify-end gap-x-6">
            <button type="submit" class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">New Project</button>
        </div>
    </div>
</div>
<!-- Projects list (only on smallest breakpoint) -->
<div class="mt-4 sm:hidden">
    <div class="px-4 sm:px-6">
        <h2 class="text-sm font-medium text-gray-900">Projects</h2>
    </div>
    <ul role="list" class="mt-3 divide-y divide-gray-100 border-t border-gray-200">
        <li>
            <a href="#" class="group flex items-center justify-between px-4 py-4 hover:bg-gray-50 sm:px-6">
                <span class="flex items-center space-x-3 truncate">
                    <span class="h-2.5 w-2.5 flex-shrink-0 rounded-full bg-pink-600" aria-hidden="true"></span>
                    <span class="truncate text-sm font-medium leading-6">
                        GraphQL API
                        <span class="truncate font-normal text-gray-500">in Engineering</span>
                    </span>
                </span>
                <svg
                    class="ml-4 h-5 w-5 text-gray-400 group-hover:text-gray-500"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                    aria-hidden="true"
                >
                    <path fill-rule="evenodd" d="M7.21 14.77a.75.75 0 01.02-1.06L11.168 10 7.23 6.29a.75.75 0 111.04-1.08l4.5 4.25a.75.75 0 010 1.08l-4.5 4.25a.75.75 0 01-1.06-.02z" clip-rule="evenodd"/>
                </svg>
            </a>
        </li>
    </ul>
</div>
<!-- Projects table (small breakpoint and up) -->
<div class="mt-4 hidden sm:block">
    <div class="inline-block min-w-full border-b border-gray-200 align-middle">
        <table class="min-w-full">
            <thead>
                <tr class="border-t border-gray-200">
                    <th class="border-b border-gray-200 bg-gray-50 px-6 py-3 text-left text-sm font-semibold text-gray-900" scope="col">
                        <span class="lg:pl-2">Projects</span>
                    </th>
                    <th class="border-b border-gray-200 bg-gray-50 px-6 py-3 text-left text-sm font-semibold text-gray-900" scope="col">Runs</th>
                    <th class="border-b border-gray-200 bg-gray-50 px-6 py-3 text-left text-sm font-semibold text-gray-900" scope="col">
                        Milestones
                    </th>
                    <th class="border-b border-gray-200 bg-gray-50 px-6 py-3 text-left text-sm font-semibold text-gray-900" scope="col">Members</th>
                    <th class="border-b border-gray-200 bg-gray-50 px-6 py-3 text-right text-sm font-semibold text-gray-900" scope="col">
                        Created At
                    </th>
                    <th class="border-b border-gray-200 bg-gray-50 py-3 pr-6 text-right text-sm font-semibold text-gray-900" scope="col">Status</th>
                </tr>
            </thead>
            <tbody class="divide-y divide-gray-100 bg-white">
                <tr>
                    <td class="w-full max-w-0 whitespace-nowrap px-6 py-3 text-sm font-medium text-gray-900">
                        <div class="flex items-center space-x-3 lg:pl-2">
                            <div class="h-2.5 w-2.5 flex-shrink-0 rounded-full bg-pink-600" aria-hidden="true"></div>
                            <a href="/quick-test/projects/1" class="truncate hover:text-gray-600 hover:underline">
                                <span>
                                    GraphQL API
                                    <span class="font-normal text-gray-500">in Engineering</span>
                                </span>
                            </a>
                        </div>
                    </td>
                    <td class="hidden whitespace-nowrap px-6 py-3 text-right text-sm text-gray-500 md:table-cell">3 Test Runs</td>
                    <td class="hidden whitespace-nowrap px-6 py-3 text-right text-sm text-gray-500 md:table-cell">1 Milestone</td>
                    <td class="px-6 py-3 text-sm font-medium text-gray-500">
                        <div class="flex items-center space-x-2">
                            <div class="flex flex-shrink-0 -space-x-1">
                                <img class="h-6 w-6 max-w-none rounded-full ring-2 ring-white" src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="Dries Vincent">
                                <img class="h-6 w-6 max-w-none rounded-full ring-2 ring-white" src="https://images.unsplash.com/photo-1517841905240-472988babdf9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="Lindsay Walton">
                                <img class="h-6 w-6 max-w-none rounded-full ring-2 ring-white" src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="Courtney Henry">
                                <img class="h-6 w-6 max-w-none rounded-full ring-2 ring-white" src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="Tom Cook">
                            </div>
                            <span class="flex-shrink-0 text-xs font-medium leading-5">+8</span>
                        </div>
                    </td>
                    <td class="hidden whitespace-nowrap px-6 py-3 text-right text-sm text-gray-500 md:table-cell">March 17, 2020</td>
                    <td class="whitespace-nowrap px-6 py-3 text-right text-sm font-medium">
                        <span class="inline-flex items-center rounded-md bg-green-50 px-2 py-1 text-xs font-medium text-green-700 ring-1 ring-inset ring-green-600/20">Active</span>
                    </td>
                </tr>
                <tr>
                    <td class="w-full max-w-0 whitespace-nowrap px-6 py-3 text-sm font-medium text-gray-900">
                        <div class="flex items-center space-x-3 lg:pl-2">
                            <div class="h-2.5 w-2.5 flex-shrink-0 rounded-full bg-pink-600" aria-hidden="true"></div>
                            <a href="/quick-test/projects/1" class="truncate hover:text-gray-600 hover:underline">
                                <span>
                                    GraphQL API
                                    <span class="font-normal text-gray-500">in Engineering</span>
                                </span>
                            </a>
                        </div>
                    </td>
                    <td class="hidden whitespace-nowrap px-6 py-3 text-right text-sm text-gray-500 md:table-cell">3 Test Runs</td>
                    <td class="hidden whitespace-nowrap px-6 py-3 text-right text-sm text-gray-500 md:table-cell">1 Milestone</td>
                    <td class="px-6 py-3 text-sm font-medium text-gray-500">
                        <div class="flex items-center space-x-2">
                            <div class="flex flex-shrink-0 -space-x-1">
                                <img class="h-6 w-6 max-w-none rounded-full ring-2 ring-white" src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="Dries Vincent">
                                <img class="h-6 w-6 max-w-none rounded-full ring-2 ring-white" src="https://images.unsplash.com/photo-1517841905240-472988babdf9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="Lindsay Walton">
                                <img class="h-6 w-6 max-w-none rounded-full ring-2 ring-white" src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="Courtney Henry">
                                <img class="h-6 w-6 max-w-none rounded-full ring-2 ring-white" src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="Tom Cook">
                            </div>
                            <span class="flex-shrink-0 text-xs font-medium leading-5">+8</span>
                        </div>
                    </td>
                    <td class="hidden whitespace-nowrap px-6 py-3 text-right text-sm text-gray-500 md:table-cell">March 17, 2020</td>
                    <td class="whitespace-nowrap px-6 py-3 text-right text-sm font-medium">
                        <span class="inline-flex items-center rounded-md bg-green-50 px-2 py-1 text-xs font-medium text-green-700 ring-1 ring-inset ring-green-600/20">Active</span>
                    </td>
                </tr>
                <!-- More projects... -->
            </tbody>
        </table>
    </div>
</div>
