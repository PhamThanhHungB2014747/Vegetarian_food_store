<template>
   <div class="slider-box">
      <div class="slider-content">
         <Splide :options="options" aria-label="My Favorite Images">
            <SplideSlide>
               <img src="https://aulac-vegan.com/wp-content/uploads/2020/09/z1988755942116_a85a77a464956e77f7599cf6bad4144a-300x169.jpg" alt="Sample 2"/>
            </SplideSlide>
            <SplideSlide>
               <img src="https://aulac-vegan.com/wp-content/uploads/2020/09/z1988756249747_5d48480ca2c42ce35c3f9069f9d2a706-300x169.jpg" alt="Sample 1" />
            </SplideSlide>
            <SplideSlide>
               <img src="https://aulac-vegan.com/wp-content/uploads/2020/09/z1988757897895_0052d6f69639bf3baf0cbc90a51eb55c-300x169.jpg" alt="Sample 2" />
            </SplideSlide>
         </Splide>
      </div>
   </div>
</template>

<script>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import { defineComponent } from "vue";

export default defineComponent({
   components: {
      Splide,
      SplideSlide,
   },

   setup() {
      const options = {
         rewind: true,
         gap: "1rem",
         autoplay: true,
      };

      return { options };
   },
});
</script>

<style scoped>
.splide__slide img {
   width: 100%;
   /* height: 50%; */
   /* object-fit: cover; */
   /* Bao phủ toàn bộ khung hình */
   /* display: block; */
}
</style>
