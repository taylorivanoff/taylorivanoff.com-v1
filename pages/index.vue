<template>
  <div class="container mx-auto">
    <div class="flex flex-wrap" data-aos="fade-up">
      <div class="w-full py-12 ">
        <h1 class="font-bold text-xl mb-2">Taylor Ivanoff</h1>
        <h2 class="mb-2">Projects</h2>
      </div>

      <section v-for="(card, index) in cards" :key="index">
        <div class="max-w-sm rounded overflow-hidden mr-2 shadow-lg">
          <img class="w-full" :src="card.image">
          <div class="px-6 py-4">
            <div class="font-bold text-xl mt-4 mb-2">{{ card.title }} <span v-if="card.demo" class="inline-block px-4 text-sm rounded ml-2 leading-loose float-right text-orange-500">Demo</span></div>
            <p class="text-gray-700 text-base">{{ card.desc }}</p>
          </div>
          <div class="px-6 py-1">
            <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2" v-for="tag in card.tags">#{{tag}}</span>
          </div>
          <div class="px-6 py-4">
            <a class="inline-block bg-blue-500 hover:bg-blue-700 text-white py-3 px-6 rounded shadow-lg mr-2 mb-2"  target="_blank" :href="card.url">View Project</a>
          </div>
        </div>
      </section>
  </div>
</div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          'title': 'SaaS Template',
          'demo': true,
          'image': '/img/stepmate.png',
          'desc': 'SaaS template that features administrator permissions, subscription and billing functions, profile management and more.',
          'url': 'https://stepmate.taylorivanoff.com/',
          'tags': [
            'saas',
            'stripe',
            'laravel'
          ]
        },    
        {
          'title': 'Stock Scanner',
          'demo': false,
          'image': '/img/scanner.png',
          'desc': 'ASX stock scanner that provides realtime data about stocks that are opening at higher price and have news for the day.',
          'url': 'https://asx-scanner.taylorivanoff.com/',
          'tags': [
            'markets',
            'realtime',
            'laravel'
          ]
        },      
        {
          'title': 'Bug Tracker',
          'demo': true,
          'image': '/img/bug-tracker.png',
          'desc': 'Card-based issue tracker that manages bug and task workflows for small web development projects.',
          'url': 'https://bug-tracker.taylorivanoff.com/',
          'tags': [
            'workflows',
            'teams',
            'laravel'
          ]
        },
        {
          'title': 'Appointment Booking',
          'demo': true,
          'image': '/img/consulting.png',
          'desc': 'Short-term booking system that would allow a client to book a time that is also convenient for a service provider.',
          'url': 'https://consulting.taylorivanoff.com/',
          'tags': [
            'booking',
            'timezones',
            'laravel'
          ]
        },
        {
          'title': 'G-code Splicer',
          'demo': false,
          'image': '/img/gcode.png',
          'desc': 'Tool that splices .gcode files in order to potentially automate a 3D additive printing production line.',
          'url': 'https://gcode-batch-tool.taylorivanoff.com/',
          'tags': [
            'gcode',
            'automation',
            'laravel'
          ]
        },
        {
          'title': 'Beard Tracker',
          'demo': false,
          'image': '/img/beard-tracker.png',
          'desc': 'iOS app that locally stores pictures of your beard growth and allows you to create timelapses of progress.',
          'url': 'https://beard-tracker.taylorivanoff.com/',
          'tags': [
            'camera',
            'movember',
            'swift'
          ]
        }
      ]
    }
  }
}

</script>
