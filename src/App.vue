<template>
  <div id="app" class="pt-12">
    <!-- Header -->
    <header class="fixed top-0 left-0 right-0 bg-white shadow-md z-50 bg-header-color">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
        <h1 class="text-2xl font-bold text-center text-white">Journal pour ma princesse</h1>
      </div>
    </header>

    <!-- Content -->
    <div class="pt-16 p-6">
      <JournalEntry v-for="entry in journalEntries" :key="entry.number" :title="entry.title" :content="entry.content"
        :entryNumber="entry.number" />
    </div>
  </div>
</template>

<script>
import JournalEntry from './components/JournalEntry.vue'

export default {
  name: 'App',
  components: {
    JournalEntry
  },
  data() {
    return {
      journalEntries: [
        { number: 1, title: '02 Juillet, 14h', content: "Ça fait bien 2/3 semaines que j'ai reçu la figurine qu'il manquait pour compléter ton Noël. Enfin pour être plus exacte la nouvelle figurine, l'autre a disparu pour d'obscures raisons à cause du marchand.<br/>Quoiqu'il en soit, tu commences à avoir l'habitude, faire les choses de manière basique, c'est à dire, faire un colis avec la figurine, avec un petit mot disant « tiens voilà le cadeau qu'il te manque, bisous », c'est pas mon truc, c'est trop simple...<br/>J'ai un certain niveau de qualité pour continuer à te draguer. Pour être honnête, aujourd'hui l'objectif c'est plus de simplement te draguer même ça c'est devenu mineur (comme toi au début quand tu mentais), l'objectif aujourd'hui, c'est de gagner ma place définitivement dans ton cœur. Je veux être ta première et dernière pensée de chaque journée.<br/>Alors comment faire ça quand l'énergumène qu'on souhaite est une petite conne, égocentrique, égoïste, qui passe son temps à râler et qui doute même dans notre existence ? Tout simplement en innovant.<br/>Alors voilà, j'ai déjà l'idée d'un colis, qui comportera au moins la figurine. <br/>Ah merde j'allais oublié, la partie sur le mariage. Euh Axelle, veux-tu m'épouser ? (Là t'es censée avoir la boîte en main et l'ouvrir).<br/>Blague à part (oui parce que hors de question de t'épouser sans avoir vérifié si t'as des cuisses VRAIMENT confortables), l'idée du cadeau, c'était de réunir mes deux passions, te draguer en étant romantique et te faire chier parce que c'est niais. Mais vu que t'aurais râlé si j'avais acheté quoique ce soit de vrai, j'ai été obligé de la faire en 3d... <br/>D'façon, si t'en veux une vraie un jour, drague moi à ton tour.<br/>Quoiqu'il en soit, il va être temps de clôturer cette première entrée à ce journal. Vu que j'ai que des idées galères, j'vais sûrement essayer de mettre ça en ligne sur un site que j'aurais fait, histoire que tu puisses tout consulter sans avoir 45 lettres chez toi...<br/>Y aura une entrée à chaque fois que je penserai à toi, jusqu'au jour de la réception je dirais ? Oh puis j'trouverai bien un moyen de rajouter des cadeaux aussi... Faut que je vois la taille du colis, et que j'équilibre par rapport à ton futur niveau de « Oh c'est trop et en plus y a pas de raison »." },
        { number: 2, title: 'Entrée 2', content: "" },
        { number: 2, title: 'Entrée 2', content: 'Contenu de la deuxième entrée du journal.' },
        { number: 2, title: 'Entrée 2', content: 'Contenu de la deuxième entrée du journal.' },
        { number: 2, title: 'Entrée 2', content: 'Contenu de la deuxième entrée du journal.' },
        { number: 2, title: 'Entrée 2', content: 'Contenu de la deuxième entrée du journal.' },
        { number: 2, title: 'Entrée 2', content: 'Contenu de la deuxième entrée du journal.' },
        { number: 2, title: 'Entrée 2', content: 'Contenu de la deuxième entrée du journal.' },
        { number: 2, title: 'Entrée 2', content: 'Contenu de la deuxième entrée du journal.' },
        { number: 2, title: 'Entrée 2', content: 'Contenu de la deuxième entrée du journal.' },
        { number: 2, title: 'Entrée 2', content: 'Contenu de la deuxième entrée du journal.' },
        { number: 2, title: 'Entrée 2', content: 'Contenu de la deuxième entrée du journal.' },
      ]
    }
  }
}
</script>

<style scoped>
.bg-header-color {
  background-color: rgba(124, 118, 206, 1);
}
</style>