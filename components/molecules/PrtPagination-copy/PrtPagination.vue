<script src="./PrtPagination.js"></script>
<template>
  <div class="prt-pagination">
    <!-- PAGINATION -->

    <div class="grid gap-4 grid-cols-4">
      <div v-if="currentPage === 1" :class="disabledStyle">
        <span class="hidden sm:inline">&lt; &lt;</span>
      </div>

      <nuxt-link
        v-else
        :to="{ name: 'articles-page-page', params: { page: 1 } }"
        :class="buttonStyles"
      >
        <span class="hidden sm:inline"> &lt; &lt;</span>
      </nuxt-link>

      <div v-if="currentPage === 1" :class="disabledStyle">
        <span class="hidden sm:inline">&lt;</span>
      </div>

      <nuxt-link
        v-else
        :to="{ name: 'articles-page-page', params: { page: prevPage } }"
        :class="buttonStyles"
      >
        <span class="hidden sm:inline">&lt;</span>
      </nuxt-link>

      <div v-if="currentPage === totalPages" :class="disabledStyle">
        <span class="hidden sm:inline"> &gt;</span>
      </div>

      <nuxt-link
        v-else
        :to="{ name: 'articles-page-page', params: { page: nextPage } }"
        :class="buttonStyles"
      >
        <span class="hidden sm:inline"> &gt;</span>
      </nuxt-link>

      <div v-if="currentPage === totalPages" :class="disabledStyle">
        <span class="hidden sm:inline"> </span>
      </div>

      <nuxt-link
        v-else
        :to="{ name: 'articles-page-page', params: { page: totalPages } }"
        :class="buttonStyles"
      >
        <span class="hidden sm:inline"> &gt; &gt;</span>
      </nuxt-link>
    </div>
    <!-- PAGINATION -->
    <nav
      class="relative z-0 inline-flex shadow-sm -space-x-px"
      aria-label="Pagination"
    >
      <a
        href="#"
        class="relative inline-flex items-center px-2 py-2 rounded-l-md border border-gray-300 bg-white text-sm font-medium text-gray-500 hover:bg-gray-50"
      >
        <span class="sr-only">Previous</span>
        <!-- Heroicon name: chevron-left -->
        <svg
          class="h-5 w-5"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
          fill="currentColor"
          aria-hidden="true"
        >
          <path
            fill-rule="evenodd"
            d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"
            clip-rule="evenodd"
          />
        </svg>
      </a>
      <a
        href="#"
        class="relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50"
      >
        1
      </a>
      <a
        href="#"
        class="relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50"
      >
        2
      </a>
      <a
        href="#"
        class="hidden md:inline-flex relative items-center px-4 py-2 border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50"
      >
        3
      </a>
      <span
        class="relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm font-medium text-gray-700"
      >
        ...
      </span>
      <a
        href="#"
        class="hidden md:inline-flex relative items-center px-4 py-2 border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50"
      >
        8
      </a>
      <a
        href="#"
        class="relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50"
      >
        9
      </a>
      <a
        href="#"
        class="relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50"
      >
        10
      </a>
      <a
        href="#"
        class="relative inline-flex items-center px-2 py-2 rounded-r-md border border-gray-300 bg-white text-sm font-medium text-gray-500 hover:bg-gray-50"
      >
        <span class="sr-only">Next</span>
        <!-- Heroicon name: chevron-right -->
        <svg
          class="h-5 w-5"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
          fill="currentColor"
          aria-hidden="true"
        >
          <path
            fill-rule="evenodd"
            d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
            clip-rule="evenodd"
          />
        </svg>
      </a>
    </nav>
  </div>
</template>
<style lang="scss"></style>
