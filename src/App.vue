<script setup lang="ts"></script>

<template>
  <div class="min-h-screen flex flex-col">
    <header class="bg-gradient-to-r from-blue-600 to-purple-600 text-white shadow-lg">
      <div class="max-w-5xl mx-auto px-6 py-8">
        <h1 class="text-4xl md:text-5xl font-bold mb-4 tracking-tight">Jose Manuel Córdoba C</h1>
        <nav aria-label="Main navigation">
          <ul class="flex flex-wrap gap-6 text-lg">
            <li>
              <a
                href="#about-title"
                class="hover:text-blue-200 transition-colors duration-200 font-medium"
                >About</a
              >
            </li>
            <li>
              <a
                href="#projects-title"
                class="hover:text-blue-200 transition-colors duration-200 font-medium"
                >Projects</a
              >
            </li>
            <li>
              <a
                href="#writings-title"
                class="hover:text-blue-200 transition-colors duration-200 font-medium"
                >Writings</a
              >
            </li>
            <li>
              <a
                href="#contact-title"
                class="hover:text-blue-200 transition-colors duration-200 font-medium"
                >Contact</a
              >
            </li>
          </ul>
        </nav>
      </div>
    </header>

    <main class="flex-grow max-w-5xl mx-auto px-6 py-12 w-full">
      <div class="space-y-16">
        <section
          aria-labelledby="about-title"
          class="bg-white rounded-xl shadow-md p-8 border border-gray-100 hover:shadow-lg transition-shadow duration-300"
        >
          <h2
            id="about-title"
            class="text-3xl font-bold mb-4 text-gray-800 border-b-4 border-blue-500 inline-block pb-2"
          >
            About Me
          </h2>
          <p class="text-gray-700 text-lg leading-relaxed">
            IT professional since 2006: developer, manager, director, startup founder. Portfolio,
            writings, and contact info below.
          </p>
        </section>

        <section
          aria-labelledby="projects-title"
          class="bg-white rounded-xl shadow-md p-8 border border-gray-100 hover:shadow-lg transition-shadow duration-300"
        >
          <h2
            id="projects-title"
            class="text-3xl font-bold mb-6 text-gray-800 border-b-4 border-purple-500 inline-block pb-2"
          >
            Featured Projects
          </h2>
          <article class="border-t border-gray-200 pt-6 mt-6">
            <p class="text-gray-500 italic text-lg">Coming soon...</p>
          </article>
        </section>

        <section
          aria-labelledby="writings-title"
          class="bg-white rounded-xl shadow-md p-8 border border-gray-100 hover:shadow-lg transition-shadow duration-300"
        >
          <h2
            id="writings-title"
            class="text-3xl font-bold mb-6 text-gray-800 border-b-4 border-green-500 inline-block pb-2"
          >
            Writings
          </h2>
          <article class="border-t border-gray-200 pt-6 mt-6">
            <p class="text-gray-500 italic text-lg">Coming soon...</p>
          </article>
        </section>

        <aside
          class="bg-gradient-to-br from-blue-50 to-purple-50 rounded-xl shadow-md p-8 border border-blue-100"
        >
          <h3 class="text-xl font-semibold mb-3 text-gray-800">Quick Connect</h3>
          <p class="text-gray-700 text-lg">
            <a
              href="mailto:jose@example.com"
              class="text-blue-600 hover:text-blue-800 font-medium underline decoration-2 underline-offset-2 transition-colors duration-200"
              >jose@example.com</a
            >
          </p>
        </aside>

        <section
          aria-labelledby="contact-title"
          class="bg-white rounded-xl shadow-md p-8 border border-gray-100 hover:shadow-lg transition-shadow duration-300"
        >
          <h2
            id="contact-title"
            class="text-3xl font-bold mb-4 text-gray-800 border-b-4 border-orange-500 inline-block pb-2"
          >
            Contact
          </h2>
          <p class="text-gray-700 text-lg leading-relaxed">Ways to get in touch.</p>
        </section>
      </div>
    </main>

    <footer class="bg-gradient-to-r from-gray-800 to-gray-900 text-white text-center py-8 mt-12">
      <small class="text-base">&copy; 2026 Jose Manuel Córdoba C</small>
    </footer>
  </div>
</template>

<style scoped></style>
