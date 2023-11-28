<template>
    <div style="background-color:#C3C1E6;">
        <div class="container">
            <br><br><br>
            <div class="bg-success rounded p-3">
                <h1 class="d-flex justify-content-center align-items-center text-warning">WELCOME TO ÂU LẠC</h1>
                <p class="text-center text-white">
                    Hơn 25 năm hình thành và phát triển , thương hiệu thực phẩm chay “Âu Lạc” đã khẳng định  được uy tính của mình trên thị trường trong nước và quốc tế.Thương hiệu thực phẩm chay Âu Lạc đã tạo được uy tín hàng đầu Việt Nam về dây chuyền sản xuất thực phẩm chay.
                </p>
                <p class="text-center text-white">
                    Với phương châm “chất lượng hàng đầu”, công ty cam kết luôn cung cấp những sản phẩm chất lượng cao nhất. Bên cạnh đó, vệ sinh an toàn thực phẩm cũng là tiêu chí hàng đầu mà Âu Lạc đặt ra trước khi đưa sản phẩm ra thị trường. Công ty luôn quan tâm đến sức khỏe của người tiêu dùng và công nghệ thân thiện với môi trường xanh.
                </p>
            </div>
            <Splide :options="options" aria-label="My Favorite Images">
                <SplideSlide class="d-flex justify-content-between align-items-center">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2020/09/z1988758498799_85c58aa1d7a59e8176be3a7e967f4980-300x169.jpg" alt="Sample 1">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2020/09/z1988758500660_909badb02dc197675c7feca66d87f41b-300x169.jpg" alt="Sample 2">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2020/09/z1988758650433_e773f7433bea200db996b7af79efff91-300x169.jpg" alt="">
                </SplideSlide>
                <SplideSlide class="d-flex justify-content-between align-items-center">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2020/09/z1988758739361_34518e27e6ec573615e674b21e45b43a-300x169.jpg" alt="Sample 2">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2020/09/z1988761945650_99d5cf694395c0faf040714e6004f87a-300x169.jpg" alt="">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2020/09/z1988762096042_2af64c018798b80fd8776f5dba6e7a88-300x169.jpg" alt="">
                </SplideSlide>
            </Splide> 
            <div class="">
                <h1 class="d-flex justify-content-center align-items-center" style="color:#fda80a">Productions</h1>    
            </div>
            <Splide :options="options" aria-label="My Favorite Images">
                <SplideSlide class="d-flex justify-content-between align-items-center">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2021/02/z2298538079975_f154d896e127f0dd5c715cd055b9d5ac.jpg" alt="" width="300">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2021/02/z2298438338160_be2591ba064d18b655ceced1dc7d1abe.jpg" alt="" width="300">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2021/02/z2298438336986_e761c11036ac01a7263c5539d745bdc6.jpg" alt="" width="300">
                </SplideSlide>
                <SplideSlide class="d-flex justify-content-between align-items-center">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2021/02/z2298438338864_c747a4961143e0f2571ddb03d683fdd9.jpg" alt="" width="300">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2022/01/z3127322013372_f4f01c362d3ce7a9947fbf2ae6c61c40-2048x1633.jpg" alt="" width="300">
                    <img src="https://aulac-vegan.com/wp-content/uploads/2022/01/z3127322013372_f4f01c362d3ce7a9947fbf2ae6c61c40-2048x1633.jpg" alt="" width="300">
                </SplideSlide>
            </Splide>            
        </div>
    </div>
</template>
<script>
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import { defineComponent } from "vue";
// Default theme
import '@splidejs/vue-splide/css';
// or other themes
import '@splidejs/vue-splide/css/skyblue';
import '@splidejs/vue-splide/css/sea-green';
// or only core styles
import '@splidejs/vue-splide/css/core';
export default defineComponent({
  components: {
    Splide,
    SplideSlide,
  },
  setup() {
      const options = {
         rewind: true,
         gap: "4px",
         autoplay: true,
      };

      return { options };
   },
});
</script>
<style>
.splide__arrow svg{
    fill:black
}
</style>