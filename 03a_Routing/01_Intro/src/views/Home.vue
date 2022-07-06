<template>
 <div>
    <h1 v-show="true" v-text="mytext">Mein Name</h1>
    <h2 v-show="true" v-html="myhtml" />
    <a
        :href="link.url"
        :target="link.target"
        :tabindex="link.tabindex"
        v-text="link.title"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      // v-text
      mytext: 'LB02 Fabian Oberli',
      // v-html
      myhtml: 'Shopping </br>Webseite<br/><b>Bzz</b>',
      // v-bind
      link: {
        url: 'https://www.digitec.ch/',
        target: '_blank',
        tabindex: '0',
        title: 'Hier gehts zum Shop'
      },
    }
  },
}
</script>

