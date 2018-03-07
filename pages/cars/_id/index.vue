<template>
  <section class="single-car">
    <h1>{{ car.title }}</h1>
    <div>
      <img class="car-image" :src="car.thumbnail" :alt="car.title">
    </div>
    <p>{{ car.descriptionText }}</p>
  </section>
</template>

<script>
export default {
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          car: [
            {
              id: "1",
              title: "Lightning McQueen",
              previewText: "Red car",
              descriptionText: "This is a lightning fast car",
              thumbnail: "https://lumiere-a.akamaihd.net/v1/images/open-uri20150422-20810-1fndzcd_41017374.jpeg"
            },
            {
              id: "2",
              title: "Cruz Ramirez",
              previewText: "Yellow car",
              descriptionText: "This car is good for endurance",
              thumbnail: "https://i.ytimg.com/vi/6JSMAbeUS-4/maxresdefault.jpg"
            },
            {
              id: "3",
              title: "Lamborghini",
              previewText: "Blue Aventador",
              descriptionText: "0-60mph in 2.4seconds!",
              thumbnail: "https://media.wired.com/photos/59b1a378a0df4b47dcf7ccb0/master/w_2400,c_limit/LamborghiniRoadsterTA.jpg"
            },
            {
              id: "4",
              title: "Rusty",
              previewText: "Good old Rusty",
              descriptionText: "0-60mph in 120.4seconds!",
              thumbnail: "https://vignette.wikia.nocookie.net/cars2character/images/2/27/Rusty_rust-eze.png/revision/latest?cb=20120308154140"
            },
            {
              id: "5",
              title: "Fred",
              previewText: "Hi, I am Fred",
              descriptionText: "Good buddy of Lightning McQueen",
              thumbnail: "https://vignette.wikia.nocookie.net/disney/images/7/7b/FredCarsArtwork.png/revision/latest?cb=20150523232203"
            },
            {
              id: "6",
              title: "Guido",
              previewText: "Friendly forklift",
              descriptionText: "Do you even lift, bru?",
              thumbnail: "https://vignette.wikia.nocookie.net/pixarcars/images/d/d0/Guido_large.jpg/revision/latest?cb=20090416204515"
            },
            {
              id: "7",
              title: "Stanley",
              previewText: "Not an antique",
              descriptionText: "I am in much better shape than most of the young peeps",
              thumbnail: "https://vignette.wikia.nocookie.net/disney/images/3/31/Lizzie.png/revision/latest?cb=20151222133758"
            }
          ].find(el => el.id === context.params.id)
        })
      }, 1500)
    })
  },
}
</script>


<style scoped>
.single-car {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}

.car-image {
  width: 100%;
  height: 500px;
}
</style>
