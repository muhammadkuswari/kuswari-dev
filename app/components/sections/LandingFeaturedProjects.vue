<template>
  <section class="my-8 md:my-16">
    <UContainer>
      <div class="inline-block relative pb-0.5 md:pb-1">
        <h1 class="text-lg md:text-2xl font-bold text-primary">
          Featured Projects
        </h1>
        <span
          class="absolute left-0 bottom-0 w-1/2 h-0.5 md:h-1 bg-primary rounded-full"
        ></span>
      </div>

      <div class="mt-4 md:mt-6">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 md:gap-6">
          <CardProject />
          <CardProject />
          <CardProject />
        </div>
        <div class="mt-4 flex justify-center">
          <UButton variant="link">See all Projects</UButton>
        </div>
      </div>
    </UContainer>
  </section>
</template>
