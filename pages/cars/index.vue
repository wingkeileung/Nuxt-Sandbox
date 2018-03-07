<template>
  <section class="cars">
    <Car 
      v-for="car in cars"
      :key="car.id"
      :thumbnail="car.thumbnail"
      :title="car.title"
      :id="car.id"
      :previewText="car.previewText"
    />
  </section>
</template>

<script>
import Car from '@/components/Car';

export default {
  components: {
    Car
  },
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          cars: [
            {
              id: "1",
              title: "Lightning McQueen",
              previewText: "Red car",
              thumbnail: "https://lumiere-a.akamaihd.net/v1/images/open-uri20150422-20810-1fndzcd_41017374.jpeg"
            },
            {
              id: "2",
              title: "Cruz Ramirez",
              previewText: "Yellow car",
              thumbnail: "https://i.ytimg.com/vi/6JSMAbeUS-4/maxresdefault.jpg"
            },
            {
              id: "3",
              title: "Lamborghini",
              previewText: "Blue Aventador",
              thumbnail: "https://media.wired.com/photos/59b1a378a0df4b47dcf7ccb0/master/w_2400,c_limit/LamborghiniRoadsterTA.jpg"
            },
            {
              id: "4",
              title: "Rusty",
              previewText: "Good old Rusty",
              thumbnail: "https://vignette.wikia.nocookie.net/cars2character/images/2/27/Rusty_rust-eze.png/revision/latest?cb=20120308154140"
            },
            {
              id: "5",
              title: "Fred",
              previewText: "Hi, I am Fred",
              thumbnail: "https://vignette.wikia.nocookie.net/disney/images/7/7b/FredCarsArtwork.png/revision/latest?cb=20150523232203"
            },
                {
              id: "6",
              title: "Guido",
              previewText: "Friendly forklift",
              thumbnail: "https://vignette.wikia.nocookie.net/pixarcars/images/d/d0/Guido_large.jpg/revision/latest?cb=20090416204515"
            },
            {
              id: "7",
              title: "Stanley",
              previewText: "Not an antique",
              thumbnail: "https://vignette.wikia.nocookie.net/disney/images/3/31/Lizzie.png/revision/latest?cb=20151222133758"
            }
          ]
        })
      }, 1500)
    })
  },
};
</script>


<style scoped>
.cars{
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}

</style>
