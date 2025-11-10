<template>
  <UCard variant="soft" class="group hover:scale-105 transition duration-300 hover:shadow-lg shadow-primary/20">
    <div class="h-52 rounded-t-xl overflow-hidden">
      <img
        src="/projects/thumbnail_kesanakemari.png"
        alt=""
        class="object-cover h-full w-full group-hover:scale-110 transition duration-300"
      />
    </div>
    <div class="p-3">
      <h2 class="font-bold text-lg text-primary">
        Kesana Kemari Travel Agency
      </h2>
      <USeparator class="my-2" type="dashed" />
      <div class="space-y-3">
        <div class="flex items-center justify-between">
          <p class="text-sm">Role:</p>
          <UBadge class="" variant="soft">Full-stack Developer</UBadge>
        </div>
        <div class="flex items-center justify-between">
          <p class="text-sm">Tech Stack:</p>
          <div class="flex items-center gap-1">
            <UBadge variant="outline">Laravel</UBadge>
            <UBadge variant="outline">React.js</UBadge>
            <UBadge variant="outline">MySQL</UBadge>
          </div>
        </div>
      </div>
    </div>
  </UCard>
</template>
