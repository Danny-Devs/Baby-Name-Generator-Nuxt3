<script setup lang="ts">
import { names } from '@/data/names'

interface Options {
  gender: 'Girl' | 'Boy' | 'Unisex' | ''
  popularity: 'Unique' | 'Trendy' | ''
  length: 'Long' | 'All' | 'Short' | ''
}

const options = reactive<Options>({
  gender: '',
  popularity: '',
  length: '',
})

const selectedNames = ref<string[]>([])
</script>

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
      class="bg-gray-300 dark:bg-gray-700 mt-8 pt-4 pb-6 rounded-lg w-[60%] mx-auto"
    >
      <div>
        <h4 text-lg mb-4>1) Choose a gender</h4>
        <div mb-4>
          <button
            @click="options.gender = 'Boy'"
            rounded-l-lg
            outline-2
            dark-outline-1
            outline-red-500
            dark:outline-white
            outline
            bg-white
            dark:bg-red-600
            px-6
            py-2
            shadow-md
            :class="options.gender === 'Boy' && 'option-active'"
          >
            Boy
          </button>
          <button
            @click="options.gender = 'Unisex'"
            outline-2
            dark-outline-1
            outline-red-500
            dark:outline-white
            outline
            bg-white
            dark:bg-red-600
            px-6
            py-2
            shadow-md
            :class="options.gender === 'Unisex' && 'option-active'"
          >
            Unisex
          </button>
          <button
            @click="options.gender = 'Girl'"
            outline-2
            dark-outline-1
            outline-red-500
            dark:outline-white
            outline
            bg-white
            dark:bg-red-600
            px-6
            py-2
            rounded-r-lg
            shadow-md
            :class="options.gender === 'Girl' && 'option-active'"
          >
            Girl
          </button>
        </div>
      </div>
      <div mb-4>
        <h4 text-lg mb-4>2) Choose the name's popularity</h4>
        <div>
          <button
            @click="options.popularity = 'Trendy'"
            outline-2
            dark-outline-1
            outline-red-500
            dark:outline-white
            outline
            rounded-l-lg
            bg-white
            dark:bg-red-600
            px-6
            py-2
            shadow-md
            :class="options.popularity === 'Trendy' && 'option-active'"
          >
            Trendy
          </button>
          <button
            @click="options.popularity = 'Unique'"
            outline-2
            dark-outline-1
            outline-red-500
            dark:outline-white
            outline
            bg-white
            dark:bg-red-600
            px-6
            py-2
            rounded-r-lg
            shadow-md
            :class="options.popularity === 'Unique' && 'option-active'"
          >
            Unique
          </button>
        </div>
      </div>
      <div mb-8>
        <h4 text-lg mb-4>3) Choose name's length</h4>
        <div>
          <button
            @click="options.length = 'Long'"
            outline-2
            dark-outline-1
            outline-red-500
            dark:outline-white
            outline
            bg-white
            dark:bg-red-600
            px-6
            py-2
            rounded-l-lg
            shadow-md
            :class="options.length === 'Long' && 'option-active'"
          >
            Long
          </button>
          <button
            @click="options.length = 'All'"
            outline-2
            dark-outline-1
            outline-red-500
            dark:outline-white
            outline
            bg-white
            dark:bg-red-600
            px-6
            py-2
            shadow-md
            :class="options.length === 'All' && 'option-active'"
          >
            All
          </button>
          <button
            @click="options.length = 'Short'"
            outline-2
            dark-outline-1
            outline-red-500
            dark:outline-white
            outline
            bg-white
            dark:bg-red-600
            px-6
            py-2
            rounded-r-lg
            shadow-md
            :class="options.length === 'Short' && 'option-active'"
          >
            Short
          </button>
        </div>
      </div>
      <button
        bg-red-500
        text-white
        font-semibold
        dark:bg-red-600
        text-lg
        px-8
        py-3
        rounded-md
        shadow-lg
        hover:bg-red-400
        class="dark:hover:bg-red-500"
        active:shadow-none
      >
        Find Names
      </button>
    </div>
    {{ selectedNames }}
  </div>
</template>

<style scoped>
.option-active {
  background-color: #ef4444;
  color: #fff;
  font-weight: 500;
}

.dark .option-active {
  background-color: #fff;
  color: #ef4444;
  font-weight: 500;
}
</style>
