<template>
  <div>
    <div class="min-h-screen bg-gray-100">
      <header class="pb-24 bg-gradient-to-r from-light-blue-800 to-cyan-600">
        <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:max-w-7xl lg:px-8">
          <div
            class="relative flex flex-wrap items-center justify-center lg:justify-between"
          >
            <!-- Logo -->
            <div class="absolute left-0 py-5 flex-shrink-0 lg:static">
              <a href="#">
                <span class="sr-only">Workflow</span>
                <!-- https://tailwindui.com/img/logos/workflow-mark-cyan-200.svg -->
                <svg
                  class="h-8 w-auto"
                  fill="none"
                  viewBox="0 0 35 32"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    fill="#A5F3FC"
                    d="M15.258 26.865a4.043 4.043 0 01-1.133 2.917A4.006 4.006 0 0111.253 31a3.992 3.992 0 01-2.872-1.218 4.028 4.028 0 01-1.133-2.917c.009-.698.2-1.382.557-1.981.356-.6.863-1.094 1.47-1.433-.024.109.09-.055 0 0l1.86-1.652a8.495 8.495 0 002.304-5.793c0-2.926-1.711-5.901-4.17-7.457.094.055-.036-.094 0 0A3.952 3.952 0 017.8 7.116a3.975 3.975 0 01-.557-1.98 4.042 4.042 0 011.133-2.918A4.006 4.006 0 0111.247 1a3.99 3.99 0 012.872 1.218 4.025 4.025 0 011.133 2.917 8.521 8.521 0 002.347 5.832l.817.8c.326.285.668.551 1.024.798.621.33 1.142.826 1.504 1.431a3.902 3.902 0 01-1.504 5.442c.033-.067-.063.036 0 0a8.968 8.968 0 00-3.024 3.183 9.016 9.016 0 00-1.158 4.244zM19.741 5.123c0 .796.235 1.575.676 2.237a4.01 4.01 0 001.798 1.482 3.99 3.99 0 004.366-.873 4.042 4.042 0 00.869-4.386 4.02 4.02 0 00-1.476-1.806 3.994 3.994 0 00-5.058.501 4.038 4.038 0 00-1.175 2.845zM23.748 22.84c-.792 0-1.567.236-2.226.678a4.021 4.021 0 00-1.476 1.806 4.042 4.042 0 00.869 4.387 3.99 3.99 0 004.366.873A4.01 4.01 0 0027.08 29.1a4.039 4.039 0 00-.5-5.082 4 4 0 00-2.832-1.18zM34 15.994c0-.796-.235-1.574-.675-2.236a4.01 4.01 0 00-1.798-1.483 3.99 3.99 0 00-4.367.873 4.042 4.042 0 00-.869 4.387 4.02 4.02 0 001.476 1.806 3.993 3.993 0 002.226.678 4.003 4.003 0 002.832-1.18A4.04 4.04 0 0034 15.993z M5.007 11.969c-.793 0-1.567.236-2.226.678a4.021 4.021 0 00-1.476 1.807 4.042 4.042 0 00.869 4.386 4.001 4.001 0 004.366.873 4.011 4.011 0 001.798-1.483 4.038 4.038 0 00-.5-5.08 4.004 4.004 0 00-2.831-1.181z"
                  />
                </svg>
              </a>
            </div>

            <!-- Right section on desktop -->
            <div
              class="hidden lg:ml-4 lg:flex lg:items-center lg:py-5 lg:pr-0.5"
            >
              <button
                type="button"
                class="flex-shrink-0 p-1 text-cyan-200 rounded-full hover:text-white hover:bg-white hover:bg-opacity-10 focus:outline-none focus:ring-2 focus:ring-white"
              >
                <span class="sr-only">View notifications</span>
                <!-- Heroicon name: outline/bell -->
                <svg
                  class="h-6 w-6"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                  aria-hidden="true"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"
                  />
                </svg>
              </button>

              <!-- Profile dropdown -->
              <div class="ml-4 relative flex-shrink-0">
                <div>
                  <button
                    type="button"
                    class="bg-white rounded-full flex text-sm ring-2 ring-white ring-opacity-20 focus:outline-none focus:ring-opacity-100"
                    id="user-menu"
                    aria-expanded="false"
                    aria-haspopup="true"
                  >
                    <span class="sr-only">Open user menu</span>
                    <img
                      class="h-8 w-8 rounded-full"
                      src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2&amp;w=256&amp;h=256&amp;q=80"
                      alt=""
                    />
                  </button>
                </div>

                <!--
              Dropdown menu, show/hide based on menu state.

              Entering: ""
                From: ""
                To: ""
              Leaving: "transition ease-in duration-75"
                From: "transform opacity-100 scale-100"
                To: "transform opacity-0 scale-95"
            -->
                <ProfilePopUp />
              </div>
            </div>

            <div
              class="w-full py-5 lg:border-t lg:border-white lg:border-opacity-20"
            >
              <div class="lg:grid lg:grid-cols-3 lg:gap-8 lg:items-center">
                <!-- Left nav -->
                <div class="hidden lg:block lg:col-span-2">
                  <userNav />
                </div>
                <div class="px-12 lg:px-0">
                  <!-- Search -->
                  <div class="max-w-xs mx-auto w-full lg:max-w-md">
                    <label for="search" class="sr-only">Search</label>
                    <div class="relative text-white focus-within:text-gray-600">
                      <div
                        class="pointer-events-none absolute inset-y-0 left-0 pl-3 flex items-center"
                      >
                        <!-- Heroicon name: solid/search -->
                        <svg
                          class="h-5 w-5"
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 20 20"
                          fill="currentColor"
                          aria-hidden="true"
                        >
                          <path
                            fill-rule="evenodd"
                            d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
                            clip-rule="evenodd"
                          />
                        </svg>
                      </div>
                      <input
                        id="search"
                        class="block w-full text-white bg-white bg-opacity-20 py-2 pl-10 pr-3 border border-transparent rounded-md leading-5 focus:text-gray-900 placeholder-white focus:outline-none focus:bg-opacity-100 focus:border-transparent focus:placeholder-gray-500 focus:ring-0 sm:text-sm"
                        placeholder="Search"
                        type="search"
                        name="search"
                      />
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- Menu button -->
            <div class="absolute right-0 flex-shrink-0 lg:hidden">
              <!-- Mobile menu button -->
              <button
                type="button"
                class="bg-transparent p-2 rounded-md inline-flex items-center justify-center text-cyan-200 hover:text-white hover:bg-white hover:bg-opacity-10 focus:outline-none focus:ring-2 focus:ring-white"
                aria-expanded="false"
              >
                <span class="sr-only">Open main menu</span>
                <!--
              Heroicon name: outline/menu

              Menu open: "hidden", Menu closed: "block"
            -->
                <svg
                  class="block h-6 w-6"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                  aria-hidden="true"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M4 6h16M4 12h16M4 18h16"
                  />
                </svg>
                <!--
              Heroicon name: outline/x

              Menu open: "block", Menu closed: "hidden"
            -->
                <svg
                  class="hidden h-6 w-6"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                  aria-hidden="true"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M6 18L18 6M6 6l12 12"
                  />
                </svg>
              </button>
            </div>
          </div>
        </div>

        <!-- Mobile menu, show/hide based on mobile menu state. -->
        <div class="lg:hidden">
          <!--
        Mobile menu overlay, show/hide based on mobile menu state.

        Entering: "duration-150 ease-out"
          From: "opacity-0"
          To: "opacity-100"
        Leaving: "duration-150 ease-in"
          From: "opacity-100"
          To: "opacity-0"
      -->
          <div
            class="z-20 fixed inset-0 bg-black bg-opacity-25"
            aria-hidden="true"
          ></div>

          <!--
        Mobile menu, show/hide based on mobile menu state.

        Entering: "duration-150 ease-out"
          From: "opacity-0 scale-95"
          To: "opacity-100 scale-100"
        Leaving: "duration-150 ease-in"
          From: "opacity-100 scale-100"
          To: "opacity-0 scale-95"
      -->
          <div
            class="z-30 absolute top-0 inset-x-0 max-w-3xl mx-auto w-full p-2 transition transform origin-top"
          >
            <div
              class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 bg-white divide-y divide-gray-200"
            >
              <div class="pt-3 pb-2">
                <div class="flex items-center justify-between px-4">
                  <div>
                    <img
                      class="h-8 w-auto"
                      src="https://tailwindui.com/img/logos/workflow-mark-cyan-600.svg"
                      alt="Workflow"
                    />
                  </div>
                  <div class="-mr-2">
                    <button
                      type="button"
                      class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-cyan-500"
                    >
                      <span class="sr-only">Close menu</span>
                      <!-- Heroicon name: outline/x -->
                      <svg
                        class="h-6 w-6"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                        aria-hidden="true"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="M6 18L18 6M6 6l12 12"
                        />
                      </svg>
                    </button>
                  </div>
                </div>
                <div class="mt-3 px-2 space-y-1">
                  <a
                    href="#"
                    class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
                    >Home</a
                  >
                  <a
                    href="#"
                    class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
                    >Profile</a
                  >
                  <a
                    href="#"
                    class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
                    >Resources</a
                  >
                  <a
                    href="#"
                    class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
                    >Company Directory</a
                  >
                  <a
                    href="#"
                    class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
                    >Openings</a
                  >
                </div>
              </div>
              <div class="pt-4 pb-2">
                <div class="flex items-center px-5">
                  <div class="flex-shrink-0">
                    <img
                      class="h-10 w-10 rounded-full"
                      src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2&amp;w=256&amp;h=256&amp;q=80"
                      alt=""
                    />
                  </div>
                  <div class="ml-3 min-w-0 flex-1">
                    <div class="text-base font-medium text-gray-800 truncate">
                      Rebecca Nicholas
                    </div>
                    <div class="text-sm font-medium text-gray-500 truncate">
                      rebecca.nicholas@example.com
                    </div>
                  </div>
                  <button
                    class="ml-auto flex-shrink-0 bg-white p-1 text-gray-400 rounded-full hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-cyan-500"
                  >
                    <span class="sr-only">View notifications</span>
                    <!-- Heroicon name: outline/bell -->
                    <svg
                      class="h-6 w-6"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                      aria-hidden="true"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"
                      />
                    </svg>
                  </button>
                </div>
                <div class="mt-3 px-2 space-y-1">
                  <a
                    href="#"
                    class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
                    >Your Profile</a
                  >
                  <a
                    href="#"
                    class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
                    >Settings</a
                  >
                  <a
                    href="#"
                    class="block rounded-md px-3 py-2 text-base text-gray-900 font-medium hover:bg-gray-100 hover:text-gray-800"
                    >Sign out</a
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </header>
      <main class="-mt-24 pb-8">
        <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:max-w-7xl lg:px-8">
          <h1 class="sr-only">Profile</h1>
          <!-- Main 3 column grid -->
          <div
            class="grid grid-cols-1 gap-4 items-start lg:grid-cols-3 lg:gap-8"
          >
            <!-- Left column -->
            <div class="grid grid-cols-1 gap-4 lg:col-span-2">
              <!-- Welcome panel -->
              <section aria-labelledby="profile-overview-title">
                <div class="rounded-lg bg-white overflow-hidden shadow">
                  <h2 class="sr-only" id="profile-overview-title">
                    Profile Overview
                  </h2>
                  <div class="bg-white p-6">
                    <div class="sm:flex sm:items-center sm:justify-between">
                      <div class="sm:flex sm:space-x-5">
                        <div class="flex-shrink-0">
                          <img
                            class="mx-auto h-20 w-20 rounded-full"
                            src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2&amp;w=256&amp;h=256&amp;q=80"
                            alt=""
                          />
                        </div>
                        <div
                          class="mt-4 text-center sm:mt-0 sm:pt-1 sm:text-left"
                        >
                          <p class="text-sm font-medium text-gray-600">
                            Welcome back,
                          </p>
                          <p
                            class="text-xl font-bold text-gray-900 sm:text-2xl"
                          >
                            Rebecca Nicholas
                          </p>
                          <p class="text-sm font-medium text-gray-600">
                            Product Designer
                          </p>
                        </div>
                      </div>
                      <div class="mt-5 flex justify-center sm:mt-0">
                        <a
                          href="#"
                          class="flex justify-center items-center px-4 py-2 border border-gray-300 shadow-sm text-sm font-medium rounded-md text-gray-700 bg-white hover:bg-gray-50"
                        >
                          View profile
                        </a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="border-t border-gray-200 bg-gray-50 grid grid-cols-1 divide-y divide-gray-200 sm:grid-cols-3 sm:divide-y-0 sm:divide-x"
                  >
                    <div class="px-6 py-5 text-sm font-medium text-center">
                      <span class="text-gray-900">12</span>
                      <span class="text-gray-600">Vacation days left</span>
                    </div>

                    <div class="px-6 py-5 text-sm font-medium text-center">
                      <span class="text-gray-900">4</span>
                      <span class="text-gray-600">Sick days left</span>
                    </div>

                    <div class="px-6 py-5 text-sm font-medium text-center">
                      <span class="text-gray-900">2</span>
                      <span class="text-gray-600">Personal days left</span>
                    </div>
                  </div>
                </div>
              </section>

              <!-- Actions panel -->
              <section aria-labelledby="quick-links-title">
                <UserCards />
              </section>
            </div>

            <!-- Right column -->
            <div class="grid grid-cols-1 gap-4">
              <!-- Announcements -->
              <Notifications />

              <!-- Recent Hires -->
              <section aria-labelledby="recent-hires-title">
                <div class="rounded-lg bg-white overflow-hidden shadow">
                  <div class="p-6">
                    <h2
                      class="text-base font-medium text-gray-900"
                      id="recent-hires-title"
                    >
                      Recent Hires
                    </h2>
                    <div class="flow-root mt-6">
                      <ul class="-my-5 divide-y divide-gray-200">
                        <li class="py-4">
                          <div class="flex items-center space-x-4">
                            <div class="flex-shrink-0">
                              <img
                                class="h-8 w-8 rounded-full"
                                src="https://images.unsplash.com/photo-1519345182560-3f2917c472ef?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2&amp;w=256&amp;h=256&amp;q=80"
                                alt=""
                              />
                            </div>
                            <div class="flex-1 min-w-0">
                              <p
                                class="text-sm font-medium text-gray-900 truncate"
                              >
                                Leonard Krasner
                              </p>
                              <p class="text-sm text-gray-500 truncate">
                                @leonardkrasner
                              </p>
                            </div>
                            <div>
                              <a
                                href="#"
                                class="inline-flex items-center shadow-sm px-2.5 py-0.5 border border-gray-300 text-sm leading-5 font-medium rounded-full text-gray-700 bg-white hover:bg-gray-50"
                              >
                                View
                              </a>
                            </div>
                          </div>
                        </li>

                        <li class="py-4">
                          <div class="flex items-center space-x-4">
                            <div class="flex-shrink-0">
                              <img
                                class="h-8 w-8 rounded-full"
                                src="https://images.unsplash.com/photo-1463453091185-61582044d556?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2&amp;w=256&amp;h=256&amp;q=80"
                                alt=""
                              />
                            </div>
                            <div class="flex-1 min-w-0">
                              <p
                                class="text-sm font-medium text-gray-900 truncate"
                              >
                                Floyd Miles
                              </p>
                              <p class="text-sm text-gray-500 truncate">
                                @floydmiles
                              </p>
                            </div>
                            <div>
                              <a
                                href="#"
                                class="inline-flex items-center shadow-sm px-2.5 py-0.5 border border-gray-300 text-sm leading-5 font-medium rounded-full text-gray-700 bg-white hover:bg-gray-50"
                              >
                                View
                              </a>
                            </div>
                          </div>
                        </li>

                        <li class="py-4">
                          <div class="flex items-center space-x-4">
                            <div class="flex-shrink-0">
                              <img
                                class="h-8 w-8 rounded-full"
                                src="https://images.unsplash.com/photo-1502685104226-ee32379fefbe?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2&amp;w=256&amp;h=256&amp;q=80"
                                alt=""
                              />
                            </div>
                            <div class="flex-1 min-w-0">
                              <p
                                class="text-sm font-medium text-gray-900 truncate"
                              >
                                Emily Selman
                              </p>
                              <p class="text-sm text-gray-500 truncate">
                                @emilyselman
                              </p>
                            </div>
                            <div>
                              <a
                                href="#"
                                class="inline-flex items-center shadow-sm px-2.5 py-0.5 border border-gray-300 text-sm leading-5 font-medium rounded-full text-gray-700 bg-white hover:bg-gray-50"
                              >
                                View
                              </a>
                            </div>
                          </div>
                        </li>

                        <li class="py-4">
                          <div class="flex items-center space-x-4">
                            <div class="flex-shrink-0">
                              <img
                                class="h-8 w-8 rounded-full"
                                src="https://images.unsplash.com/photo-1500917293891-ef795e70e1f6?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2&amp;w=256&amp;h=256&amp;q=80"
                                alt=""
                              />
                            </div>
                            <div class="flex-1 min-w-0">
                              <p
                                class="text-sm font-medium text-gray-900 truncate"
                              >
                                Kristin Watson
                              </p>
                              <p class="text-sm text-gray-500 truncate">
                                @kristinwatson
                              </p>
                            </div>
                            <div>
                              <a
                                href="#"
                                class="inline-flex items-center shadow-sm px-2.5 py-0.5 border border-gray-300 text-sm leading-5 font-medium rounded-full text-gray-700 bg-white hover:bg-gray-50"
                              >
                                View
                              </a>
                            </div>
                          </div>
                        </li>
                      </ul>
                    </div>
                    <div class="mt-6">
                      <a
                        href="#"
                        class="w-full flex justify-center items-center px-4 py-2 border border-gray-300 shadow-sm text-sm font-medium rounded-md text-gray-700 bg-white hover:bg-gray-50"
                      >
                        View all
                      </a>
                    </div>
                  </div>
                </div>
              </section>
            </div>
          </div>
        </div>
      </main>
      <Footer />
    </div>
  </div>
</template>
<script>
import userNav from '@/components/userLayout/Nav'
import UserCards from '@/components/userLayout/UserCards'
import Footer from '@/components/userLayout/Footer'
import ProfilePopUp from '@/components/userLayout/ProfilePopUp'
import Notifications from '@/components/userLayout/Notifications'

export default {
  components: {
    userNav,
    Footer,
    UserCards,
    ProfilePopUp,
    Notifications,
  },
}
</script>
