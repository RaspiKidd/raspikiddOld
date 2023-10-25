<template>
  <div class="relative bg-gray-50">
    <Header />
    <!-- main -->
    <div class="relative bg-gray-50 pt-16 pb-20 px-4 sm:px-6 lg:pt-24 lg:pb-28 lg:px-8">
      <div class="absolute inset-0">
        <div class="bg-white h-1/3 sm:h-2/3"></div>
      </div>
              
      <div class="relative max-w-7xl mx-auto">
        <div class="text-center">
          <h1 class="text-4xl tracking-tight font-extrabold text-gray-900 sm:text-5xl md:text-6xl lg:text-5xl xl:text-6xl" style="color:#A42530">
            From the Blog
          </h1>
        </div>
      </div>
      <div class="grid max-w-lg gap-5 mx-auto mt-12 lg:grid-cols-3 lg:max-w-none">
        <ArticleCard
          v-for="article in articles"
          :key="article.content.title"
          :title="article.content.title"
          :description="article.content.description"
          :slug="`/${article.slug}`"
          :author="article.content.author"
          :image="article.content.image.filename"
          :date="article.content.date.toLocaleDateString()"
        />
      </div>
    </div>
    <Footer />
  </div>
</template>