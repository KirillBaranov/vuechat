<template>
  <div class="dialog-list">

    <v-list two-line>
      <template v-for="dialog in dialogs">
        <Dialog class="dialog-list__dialog" :dialog="dialog"></Dialog>
      </template>
    </v-list>

    <v-list two-line>

    </v-list>

  </div>
</template>

<script>
    import Dialog from './templates/Dialog.vue';

    export default {
        name: "DialogList",
        components: {
            Dialog
        },
        data() {
            return {
                dialogs: [
                    {
                        avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
                        title: 'Brunch this weekend?',
                        subtitle: "<span class='text--primary'>Ali Connors</span> &mdash; I'll be in your neighborhood doing errands this weekend. Do you want to hang out?"
                    },
                    { divider: true, inset: true },
                    {
                        avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
                        title: 'Summer BBQ <span class="grey--text text--lighten-1">4</span>',
                        subtitle: "<span class='text--primary'>to Alex, Scott, Jennifer</span> &mdash; Wish I could come, but I'm out of town this weekend."
                    },
                    { divider: true, inset: true },
                    {
                        avatar: 'https://cdn.vuetifyjs.com/images/lists/3.jpg',
                        title: 'Oui oui',
                        subtitle: "<span class='text--primary'>Sandra Adams</span> &mdash; Do you have Paris recommendations? Have you ever been?"
                    }
                ]
            }
        }
    }
</script>

<style scoped>
  .dialog-list {
    width: 100%;
    margin: 60px 15px 0 15px;
  }
</style>