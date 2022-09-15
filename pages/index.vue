<script setup></script>

<template>
  <div class="text-black dark:text-white container mx-auto text-center mt-8">
    <div flex justify-center items-center>
      <h1 text-3xl mr-8>Baby Name Generator</h1>
      <div
        class="text-2xl i-tabler-moon dark:i-tabler-sun hover:cursor-pointer"
        @click="toggleDark()"
      ></div>
    </div>
    <p mt-6>Choose your options and click the "Find Names" button below</p>
    <div
      class="bg-gray-300 dark:bg-gray-600 mt-8 py-4 rounded-lg w-[60%] mx-auto"
    >
      <div>
        <h4 text-lg mb-4>1) Choose a gender</h4>
        <div mb-4>
          <button
            mr-4
            bg-red-400
            dark:bg-red-600
            px-4
            py-2
            rounded-md
            shadow-md
          >
            Boy
          </button>
          <button
            mr-4
            bg-red-400
            dark:bg-red-600
            px-4
            py-2
            rounded-md
            shadow-md
          >
            Unisex
          </button>
          <button bg-red-400 dark:bg-red-600 px-4 py-2 rounded-md shadow-md>
            Girl
          </button>
        </div>
      </div>
      <div mb-4>
        <h4 text-lg mb-4>2) Choose the name's popularity</h4>
        <div>
          <button
            mr-4
            bg-red-400
            dark:bg-red-600
            px-4
            py-2
            rounded-md
            shadow-md
          >
            Trendy
          </button>
          <button bg-red-400 dark:bg-red-600 px-4 py-2 rounded-md shadow-md>
            Unique
          </button>
        </div>
      </div>
      <div mb-4>
        <h4 text-lg mb-4>3) Choose name's length</h4>
        <div>
          <button
            mr-4
            bg-red-400
            dark:bg-red-600
            px-4
            py-2
            rounded-md
            shadow-md
          >
            Long
          </button>
          <button
            mr-4
            bg-red-400
            dark:bg-red-600
            px-4
            py-2
            rounded-md
            shadow-md
          >
            All
          </button>
          <button bg-red-400 dark:bg-red-600 px-4 py-2 rounded-md shadow-md>
            Short
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
