<template>
  <div class="container is-fullhd">
    <b-carousel-list v-model="currentPage" :data="items" :items-to-show="perList">
        <template slot="item" slot-scope="list">
            <div class="card">
                <div class="card-image">
                    <figure class="image is-5by4">
                        <a @click="info(list.index)"><img :src="list.image"></a>
                    </figure>
                    <b-tag type="is-danger" rounded style="position: absolute; top: 0;"><b>50%</b></b-tag>
                </div>
                <div class="card-content">
                    <div class="content">
                        <p class="title is-6">{{ list.title }}</p>
                        <p class="subtitle is-7">@johnsmith</p>
                        <div class="field is-grouped" >
                            <p class="control is-6" v-if="list.rating">
                                <b-rate :value="list.rating" show-score disabled/>
                            </p>
                        </div>
                        <div class="field is-grouped" >
                            <p class="control is-6" style="margin-left: auto">
                                <div class="buttons">
                                    <b-button type="is-primary" expanded>Expanded</b-button>
                                </div>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </template>
    </b-carousel-list>
  </div>
</template>

<script>
import Card from '~/components/Card'

export default {
  name: 'HomePage',

  components: {
    Card
  },
  data() {
        return {
            currentPage: 0,
            perList:2,
            items: [
                {
                    title: 'Slide 1',
                    image: 'https://buefy.org/static/img/placeholder-1280x960.png',
                    rating: 4.4
                },
                {
                    title: 'Slide 2',
                    image: 'https://buefy.org/static/img/placeholder-1280x960.png',
                    rating: 3.5
                },
                {
                    title: 'Slide 3',
                    image: 'https://buefy.org/static/img/placeholder-1280x960.png',
                    rating: 5
                },
                {
                    title: 'Slide 4',
                    image: 'https://buefy.org/static/img/placeholder-1280x960.png'
                },
                {
                    title: 'Slide 5',
                    image: 'https://buefy.org/static/img/placeholder-1280x960.png',
                    rating: 5
                },
                {
                    title: 'Slide 6',
                    image: 'https://buefy.org/static/img/placeholder-1280x960.png',
                    rating: 4
                },
                {
                    title: 'Slide 7',
                    image: 'https://buefy.org/static/img/placeholder-1280x960.png',
                    rating: 2.7
                },
                {
                    title: 'Slide 8',
                    image: 'https://buefy.org/static/img/placeholder-1280x960.png',
                    rating: 1.5
                }
            ]
        }
    },
    methods: {
        info(value) {
            this.currentPage = value
        }
    }
}
</script>
