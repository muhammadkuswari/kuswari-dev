<template>
  <section class="my-8 md:my-16">
    <UContainer class="flex flex-col items-center justify-center">
      <!-- image -->
      <div class="flex justify-center relative">
        <img
          src="~/assets/images/muhammadkuswari.png"
          alt="Muhammad Kuswari"
          class="max-w-3xs md:max-w-2xs z-10"
        />
        <div
          class="w-60 h-60 bg-lime-400/30 absolute rounded-full blur-3xl top-10"
        />
        <div
          class="absolute bottom-0 w-full h-28 bg-linear-to-t from-white dark:from-neutral-900 to-transparent z-10"
        ></div>
      </div>
      <!-- title and description -->
      <div class="text-center">
        <h1 class="text-xl md:text-4xl font-bold leading-relaxed">
          Hi, I'm Muhammad Kuswari <br />
          A Professional <span class="text-primary">Front-end</span> Developer
        </h1>
        <p class="text-sm md:text-base font-light mt-2 md:mt-4 max-w-xl">
          <span class="text-primary font-bold">Front-end Developer</span> with
          5+ years of experiences turn ideas into real, interactive, and
          high-performing web and mobile application products.
        </p>
      </div>
      <!-- action button -->
      <div class="mt-2 md:mt-4 flex gap-2">
        <UButton size="lg" icon="i-lucide-rocket" to="/projects"
          >See my Work</UButton
        >
        <UButton
          size="lg"
          icon="i-lucide-file"
          variant="outline"
          @click="
            handleDownloadResume(
              '/documents/Resume - Muhammad Kuswari - Front-end Developer.pdf',
              'Resume - Muhammad Kuswari.pdf'
            )
          "
          >Get my Resume</UButton
        >
      </div>
    </UContainer>
  </section>
</template>

<script lang="ts" setup>
const handleDownloadResume = (filePath: string, fileName: string) => {
  const link = document.createElement("a");
  link.href = filePath;
  link.download = fileName;

  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
};
</script>
