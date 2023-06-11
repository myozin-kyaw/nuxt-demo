<template>
  <DefaultWidth>
    <div
      class="w-full overflow-hidden m-5 flex flex-col justify-center w-[500px] mx-auto"
    >
      <div v-if="pending" class="loader loader--style8 flex items-center justify-center h-[50vh]" title="7">
        <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
          width="24px" height="30px" viewBox="0 0 24 30" style="enable-background:new 0 0 50 50;" xml:space="preserve">
          <rect x="0" y="10" width="4" height="10" fill="#00DC82" opacity="0.2">
            <animate attributeName="opacity" attributeType="XML" values="0.2; 1; .2" begin="0s" dur="0.6s" repeatCount="indefinite" />
            <animate attributeName="height" attributeType="XML" values="10; 20; 10" begin="0s" dur="0.6s" repeatCount="indefinite" />
            <animate attributeName="y" attributeType="XML" values="10; 5; 10" begin="0s" dur="0.6s" repeatCount="indefinite" />
          </rect>
          <rect x="8" y="10" width="4" height="10" fill="#00DC82"  opacity="0.2">
            <animate attributeName="opacity" attributeType="XML" values="0.2; 1; .2" begin="0.15s" dur="0.6s" repeatCount="indefinite" />
            <animate attributeName="height" attributeType="XML" values="10; 20; 10" begin="0.15s" dur="0.6s" repeatCount="indefinite" />
            <animate attributeName="y" attributeType="XML" values="10; 5; 10" begin="0.15s" dur="0.6s" repeatCount="indefinite" />
          </rect>
          <rect x="16" y="10" width="4" height="10" fill="#00DC82"  opacity="0.2">
            <animate attributeName="opacity" attributeType="XML" values="0.2; 1; .2" begin="0.3s" dur="0.6s" repeatCount="indefinite" />
            <animate attributeName="height" attributeType="XML" values="10; 20; 10" begin="0.3s" dur="0.6s" repeatCount="indefinite" />
            <animate attributeName="y" attributeType="XML" values="10; 5; 10" begin="0.3s" dur="0.6s" repeatCount="indefinite" />
          </rect>
        </svg>
      </div>
      <ul v-else role="list" class="divide-y divide-gray-100">
        <li
          v-for="product in products"
          :key="product.id"
          class="py-4 hover:bg-gray-200 px-3 cursor-pointer"
        >
          <NuxtLink :to="`/products/${product.id}`">
            <div class="flex items-center gap-x-3">
              <img
                :src="product.image"
                alt=""
                class="h-8 w-8 flex-none rounded-full bg-gray-800"
              />
              <h3
                class="flex-auto truncate text-sm font-semibold leading-6 text-gray-900"
              >
                {{ product.title }} ({{ product.category }})
              </h3>
            </div>
            <p class="mt-3 truncate text-sm text-gray-500">
              <span class="text-gray-700"
                >Desc : {{ cutText(product.description, 30) }}</span
              >
            </p>
            <p class="mt-3 truncate text-sm text-gray-500">
              <span class="text-gray-700">Price : {{ product.price }}</span>
            </p>
          </NuxtLink>
        </li>
      </ul>
    </div>
  </DefaultWidth>
</template>

<script setup>
const products = ref();
const { pending, data } = await useFetch("https://fakestoreapi.com/products",{
  lazy: true,
  // server: false
});

if (data.value) {
  products.value = data.value;
}

function capitalizeFirstLetter(value) {
  return value.charAt(0).toUpperCase() + value.slice(1);
}

function cutText(text, maxLength) {
  if (text.length > maxLength) {
    return text.substring(0, maxLength) + "...";
  }
  return text;
}
</script>