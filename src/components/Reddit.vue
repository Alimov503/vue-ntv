<template>
  <Page>
      <ListView class="list-group" for="post in posts"
          @itemTap="onItemTap" style="height:2350px">
          <v-template>
              <FlexboxLayout flexDirection="row" class="list-group-item">
                  <Image :src="post.data.thumbnail" class="thumb img-circle" />
                  <Label :text="post.data.title" class="list-group-item-heading"
                      style="width: 60%" />
              </FlexboxLayout>
          </v-template>
      </ListView>

  </Page>
</template>

<script>
import another from './anoth'
import axios from 'axios'
export default {

  data() {
    return {
      posts: [],
    }
  },
  mounted(){

      axios.get('https://reddit.com/r/aww.json')
  .then(res => {
    this.posts = res.data.data.children
  })

    // fetch('https://reddit.com/r/aww.json')
    // .then(res => res.json())
    // .then(data => {
    //   this.posts =  data.data.children
    //   // console.log( data.data.children[0].data.thumbnail)
    // })
  },
  methods:{
    onItemTap : function (args){
      console.log('Item with index ' + args.item.data.thumbnail + ' was tapped' );
      this.$navigateTo(another, {
        context: {
          propsData:{
            imageSrc: args.item.data.thumbnail,

          }
        }
      })
    },
   
  }
}
</script>

<style>

</style>
