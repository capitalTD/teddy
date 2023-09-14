<template>
  <div>
    <v-carousel
      cycle
      height="500"
      hide-delimiter-background
      show-arrows-on-hover
    >
      <v-carousel-item
        v-for="(slide, i) in slides"
        :key="i"
      >
        <v-sheet
          :color="colors[i]"
          height="100%"
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <div class="text-h2">
              {{ slide }} Slide
            </div>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>

<template>
  <v-row>
    <v-col>
      <h1 align="center" justify="center">{{arr.title}}</h1>
    </v-col>
  </v-row>
</template>




    <template >
        <v-row >
          <v-col  v-for="(item, index) in items" :key="index">
            <v-col :style="{'background-color':item.colors}">
            <v-card
            style="background-color:maroon"
              max-width="344"
              class="mx-auto"
            >
              <v-img
                :src="item.img"
                height="200px"
              ></v-img>
              <v-card-title>
                {{item.title}}
              </v-card-title>

              <v-card-subtitle>
                {{item.subtitle}}
              </v-card-subtitle>

              <v-card-actions>
                <v-btn
                  color="orange lighten-2"
                  text
                >
                  Explore
                </v-btn>

                <v-spacer></v-spacer>

                <v-btn
                  icon
                  @click="show = !show"
                >
                  <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                </v-btn>
              </v-card-actions>

              <v-expand-transition>
                <div v-show="show">
                  <v-divider></v-divider>

                  <v-card-text>
                    I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
                  </v-card-text>
                </div>
              </v-expand-transition>
            </v-card>
            </v-col>

          </v-col>
         
        
        </v-row>

    </template>
  </div>
</template>

<script>
import coffee from '../../public/img/icons/coffee.jpg'
import img from '../../public/img/icons/mstile-150x150.png'
export default {
    data () {
      return {
        colors: [
          'indigo',
          'warning',
          'pink darken-2',
          'red lighten-1',
          'deep-purple accent-4',
        ],
        slides: [
          'First',
          'Second',
          'Third',
          'Fourth',
          'Fifth',
        ],
        show:false,

        // test: '../../public/img/icons/coffee.jpg',
        items:[
          {
            img: coffee,
            title: "title",
            subtitle:"subtitle1",
            colors:"red"
          },
          {
            img: img,
            title: "title2",
            subtitle:"subtitle2",
            colors:"green"
          },
          {
            img: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
            title: "title3",
            subtitle:"subtitle3",
            colors:"yellow"
          },
          {
            img: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
            title: "title3",
            subtitle:"subtitle3",
            colors:"blue"
          },
          {
            img: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
            title: "title3",
            subtitle:"subtitle3",
            colors:"violet"
          },
          {
            img: "https://shottbeverages.com/wp-content/uploads/2020/07/tahitian_lime_mint_soda.jpg",
            title: "title3",
            subtitle:"subtitle3",
            colors:"lime"
          },
          {
            img: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
            title: "title3",
            subtitle:"subtitle3",
            colors:"red"
          },
          {
            img: "https://media.istockphoto.com/id/1358132613/photo/refreshing-hot-cup-of-coffee-at-a-cafe.jpg?s=612x612&w=0&k=20&c=ObwIF28Vt3k93Nch9U4QYUdOwMA_eiMwVVCvKbypnNc=",
            title: "title3",
            subtitle:"subtitle3",
            colors:"#8c4f0d"
          },
          {
            img: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
            title: "title3",
            subtitle:"subtitle3",
            colors:"indigo"
          },
          {
            img: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
            title: "title3",
            subtitle:"subtitle3",
            colors:"pink"
          },
          {
            img: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
            title: "title3",
            subtitle:"subtitle3",
            colors:"black"
          }
        ],
        arr: []
      }
    },
    created(){
      this.filterArray()
    },
    methods:{
      filterArray(){

        const map1 = this.slides.map(x => {
          
          return x
        })
        map1.push("sfsdf")
        console.log("map",map1)

        // for(let i=0;i<this.slides.length;i++){
        //   console.log("loop",this.slides[i])
        // }
      }
    }
  }
</script>
