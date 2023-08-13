<script>
let menu = { opened: false, filter: false };

function toggle() {
    menu.opened = !menu.opened;
}

function filter() {
    menu.filter = !menu.filter;
}

export let selection;

let tabs = [
    { name: 'Overview', href: '#', current: selection === 'Overview' },    
    { name: 'Test Runs', href: '#', current: selection === 'Test Runs' },
    { name: 'Test Cases', href: '#', current: selection === 'Test Cases' },
    { name: 'Test Groups', href: '#', current: selection === 'Test Groups' },
    { name: 'Todos', href: '#', current: selection === 'Todos' },
    { name: 'Milestones', href: '#', current: selection === 'Milestones' },
    { name: 'Members', href: '#', current: selection === 'Members' }
    ];


</script>
<div class="bg-gray-50/50">
    <div class="mx-auto px-4 pt-4 sm:px-6 lg:px-8">
        <div class="sm:flex sm:items-baseline sm:justify-between">
            <div class="sm:w-0 sm:flex-1">
                <h1 class="flex-1 text-2xl font-bold text-gray-900">GraphQL API</h1>
                <p class="mt-1 truncate text-sm text-gray-500">This is project description which should not go beyond one line</p>
            </div>
            <div class="mt-4 flex items-center justify-between sm:ml-6 sm:mt-0 sm:flex-shrink-0 sm:justify-start">
                <span class="inline-flex items-center rounded-md bg-green-50 px-2 py-1 text-xs font-medium text-green-700 ring-1 ring-inset ring-green-600/20">Active</span>

                <div class="relative ml-3 inline-block text-left">
                    <div>
                        <button
                        on:click={toggle}
                            type="button"
                            class="-my-2 flex items-center rounded-full bg-white p-2 text-gray-400 hover:text-gray-600 focus:outline-none focus:ring-2 focus:ring-indigo-500"
                            id="menu-0-button"
                            aria-expanded="false"
                            aria-haspopup="true"
                        >
                            <span class="sr-only">Open options</span>
                            <svg
                                class="h-5 w-5"
                                viewBox="0 0 20 20"
                                fill="currentColor"
                                aria-hidden="true"
                            >
                                <path d="M10 3a1.5 1.5 0 110 3 1.5 1.5 0 010-3zM10 8.5a1.5 1.5 0 110 3 1.5 1.5 0 010-3zM11.5 15.5a1.5 1.5 0 10-3 0 1.5 1.5 0 003 0z"/>
                            </svg>
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
                        class="absolute right-0 z-10 mt-2 w-56 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
                        role="menu"
                        aria-orientation="vertical"
                        aria-labelledby="menu-0-button"
                        tabindex="-1"
                    >
                        <div class="py-1" role="none">
                            <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
                            <a
                                href="#"
                                class="text-gray-700 flex justify-between px-4 py-2 text-sm hover:bg-gray-50"
                                role="menuitem"
                                tabindex="-1"
                                id="menu-0-item-0"
                            >
                                <span>Edit</span>
                            </a>
                            <button
                                type="button"
                                class="text-gray-700 flex w-full justify-between px-4 py-2 text-sm hover:bg-gray-50"
                                role="menuitem"
                                tabindex="-1"
                                id="menu-0-item-2"
                            >
                                <span>Archive</span>
                            </button>
                        </div>
                    </div>
                    {/if}
                </div>
            </div>
        </div>
    </div>
    <div>
        <div class="sm:hidden">
            <label for="tabs" class="sr-only">Select a tab</label>
            <!-- Use an "onChange" listener to redirect the user to the selected tab URL. -->
            <select id="tabs" name="tabs" class="block w-full rounded-md border-gray-300 py-2 pl-3 pr-10 text-base focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm">
                <option>Overview</option>
                <option>Todos</option>
                <option selected>Milestones</option>
                <option>Test Cases</option>
                <option>Test Runs</option>
                <option>Team</option>
            </select>
        </div>
        <div class="hidden sm:block">
            <div class="border-b border-gray-200 mt-2">
                <nav class="-mb-px flex space-x-8 px-8" aria-label="Tabs">
                    {#each tabs as tab}
                    <a
                        href="#"
                        class={tab.current ? 'border-indigo-500 text-indigo-600 whitespace-nowrap border-b-2 py-2 px-1 text-sm font-medium' : 'border-transparent text-gray-500 hover:border-gray-300 hover:text-gray-700 whitespace-nowrap border-b-2 py-2 px-1 text-sm font-medium'}
                    >
                        {tab.name}
                    </a>
                    {/each}
                    
                </nav>
            </div>
        </div>
    </div>
</div>
