<script setup lang="ts">
import 'bootstrap/dist/css/bootstrap.min.css'
import 'bootstrap'
import { ref, onMounted } from 'vue'

const carouselElement = ref<HTMLElement | null>(null)

onMounted(() => {
  if (carouselElement.value) {
    const carousel = new bootstrap.Carousel(carouselElement.value, {
      interval: 3000,
      ride: 'carousel'
    })

    carouselElement.value.querySelector('.carousel-control-prev')?.addEventListener('click', () => {
      carousel.prev()
    })

    carouselElement.value.querySelector('.carousel-control-next')?.addEventListener('click', () => {
      carousel.next()
    })
  }
})
</script>

<template>
  <link
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
    rel="stylesheet"
    integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
    crossorigin="anonymous"
  />
  <div class="page-wrapper">
    <div class="">
      <header></header>
      <div class="d-flex align-items-center justify-content-between py-2 px-3">
        <div>
          <h5 class="m-0"><b>NUTRI FRESH</b></h5>
        </div>

        <div class="inicio d-flex align-items-right">
          <span class="separator"></span>
          <a href="https://es-la.facebook.com/" target="_blank">
            <img src="C:\Users\PC\Desktop\desayunos-vue\img\facebook.png" alt="Facebook" />
          </a>

          <a href="https://www.tiktok.com/upload?lang=es" target="_blank">
            <img src="C:\Users\PC\Desktop\desayunos-vue\img\tiktok.png" alt="TikTok" />
          </a>

          <a href="https://www.instagram.com/" target="_blank">
            <img src="C:\Users\PC\Desktop\desayunos-vue\img\instagram.png" alt="Instagram" />
          </a>
        </div>
      </div>
    </div>

    <main>
      <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-indicators">
          <button
            type="button"
            data-bs-target="#carouselExampleCaptions"
            data-bs-slide-to="0"
            class="active"
            aria-current="true"
            aria-label="Slide 1"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleCaptions"
            data-bs-slide-to="1"
            aria-label="Slide 2"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleCaptions"
            data-bs-slide-to="2"
            aria-label="Slide 3"
          ></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img
              src="C:\Users\PC\Desktop\desayunos-vue\img\first-slide.jpg"
              class="d-block w-100"
              alt="First Slide"
            />
            <div class="carousel-caption d-none d-md-block">
              <h1>DESAYUNOS SALUDABLES</h1>
            </div>
          </div>
          <div class="carousel-item">
            <img
              src="C:\Users\PC\Desktop\desayunos-vue\img\second-slide.png"
              class="d-block w-100"
              alt="Second Slide"
            />
            <div class="carousel-caption d-none d-md-block">
              <h1>DESAYUNOS SALUDABLES</h1>
            </div>
          </div>
          <div class="carousel-item">
            <img
              src="C:\Users\PC\Desktop\desayunos-vue\img\third-slide.png"
              class="d-block w-100"
              alt="Third Slide"
            />
            <div class="carousel-caption d-none d-md-block">
              <h1>DESAYUNOS SALUDABLES</h1>
            </div>
          </div>
        </div>
        <button
          class="carousel-control-prev"
          type="button"
          data-bs-target="#carouselExampleCaptions"
          data-bs-slide="prev"
        >
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button
          class="carousel-control-next"
          type="button"
          data-bs-target="#carouselExampleCaptions"
          data-bs-slide="next"
        >
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>

      <div class="d-flex justify-content-around align-items-center">
        <div class="position-relative align-items-center">
          <img
            src="C:\Users\PC\Desktop\desayunos-vue\img\Ellipse1.png"
            class="circle"
            alt="Desayuno Ligero"
          />
          <img
            src="C:\Users\PC\Desktop\desayunos-vue\img\like.png"
            class="icon-overlay"
            alt="Ícono Desayuno Ligero"
          />
          <figcaption>
            <h5>Desayuno Saludable</h5>
            <p>Perfecto para una dieta equilibrada y rica en fibra.</p>
          </figcaption>
        </div>

        <div class="position-relative align-items-center">
          <img
            src="C:\Users\PC\Desktop\desayunos-vue\img\Ellipse1.png"
            class="circle"
            alt="Desayuno Completo"
          />
          <img
            src="C:\Users\PC\Desktop\desayunos-vue\img\humbleicons.png"
            class="icon-overlay"
            alt="Ícono Desayuno Completo"
          />
          <figcaption>
            <h5>Desayuno Completo</h5>
            <p>Una opción balanceada con todos los nutrientes.</p>
          </figcaption>
        </div>

        <div class="position-relative text-center">
          <img
            src="C:\Users\PC\Desktop\desayunos-vue\img\Ellipse1.png"
            class="circle"
            alt="Desayuno Saludable"
          />
          <img
            src="C:\Users\PC\Desktop\desayunos-vue\img\coffee.png"
            class="icon-overlay"
            alt="Ícono Desayuno Saludable"
          />
          <figcaption>
            <h5>Desayuno Ligero</h5>
            <p>Ideal para comenzar el día con energía.</p>
          </figcaption>
        </div>
      </div>

      <nav>
        <div class="texto">
          <h5>Beneficios</h5>
          <p>• Aportan Energía para el Día.</p>
          <p>• Mejoran la Concentración y el Rendimiento.</p>
          <p>• Contribuyen a Mantener un Peso Saludable.</p>
        </div>

        <div class="imagen">
          <img src="C:\Users\PC\Desktop\desayunos-vue\img\Honey.png" alt="Honey Image" />
        </div>
      </nav>

      <div class="question">
        <h5>¿Te gusta el desayuno saludable?</h5>
        <div class="options">
          <label>
            <input type="radio" name="answer" value="Sí" />
            <span>Sí</span>
          </label>
          <label>
            <input type="radio" name="answer" value="No" />
            <span>No</span>
          </label>
        </div>
      </div>

      <section class="muestras">
        <img src="C:\Users\PC\Desktop\desayunos-vue\img\muestra1.jpg" alt="Muestra 1" />
        <img src="C:\Users\PC\Desktop\desayunos-vue\img\muestra2.jpg" alt="Muestra 2" />
        <img src="C:\Users\PC\Desktop\desayunos-vue\img\muestra3.jpg" alt="Muestra 3" />
        <img src="C:\Users\PC\Desktop\desayunos-vue\img\muestra4.jpg" alt="Muestra 4" />
        <img src="C:\Users\PC\Desktop\desayunos-vue\img\muestra5.jpg" alt="Muestra 5" />
        <img src="C:\Users\PC\Desktop\desayunos-vue\img\muestra6.jpg" alt="Muestra 6" />
        <img src="C:\Users\PC\Desktop\desayunos-vue\img\muestra7.jpg" alt="Muestra 7" />
      </section>

      <nav class="brunch">
        <div class="imagen1">
          <img src="C:\Users\PC\Desktop\desayunos-vue\img\brunch.png" alt="Brunch Image" />
        </div>

        <div class="texto1">
          <h5>Porcentaje de Bienestar</h5>
          <br />
          <div
            class="progress"
            role="progressbar"
            aria-label="Basic example"
            aria-valuenow="0"
            aria-valuemin="0"
            aria-valuemax="100"
          >
            <div class="progress-bar" style="width: 45%">45%</div>
          </div>
          <br />
          <div
            class="progress"
            role="progressbar"
            aria-label="Basic example"
            aria-valuenow="25"
            aria-valuemin="0"
            aria-valuemax="100"
          >
            <div class="progress-bar" style="width: 78%">78%</div>
          </div>
          <br />
          <div
            class="progress"
            role="progressbar"
            aria-label="Basic example"
            aria-valuenow="50"
            aria-valuemin="0"
            aria-valuemax="100"
          >
            <div class="progress-bar" style="width: 89%">89%</div>
          </div>
        </div>
      </nav>
    </main>
  </div>
  <footer></footer>
</template>

<style scoped>
.page-wrapper {
  background-color: #f5f5f5;
  display: flex;
  flex-direction: column;
  min-height: 200vh;
}

header,
footer {
  background-color: #0b0b0b;
  padding: 20px;
  border-radius: 5px;
}

nav {
  background-color: #f0eeef;
  padding: 20px;
  border-radius: 5px;
  margin-top: 120px;
  display: flex;
  align-items: center;
}

.inicio {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border: none;
  outline: none;
  transition: none;
}

.inicio a img {
  border: none;
  outline: none;
  transition: none;
}

.inicio a img:hover {
  border-color: transparent;
  background-color: transparent;
}

.texto {
  flex: 1;
  margin-left: 160px;
}

.imagen {
  flex: 0 0 auto;
  margin-right: 80px;
  margin-top: 20px;
}

.imagen img {
  height: auto;
  margin: 2px;
  max-width: 150px;
  margin-right: 30px;
}

.texto1 {
  flex: 1;
  margin-left: 100px;
  padding: 10px;
}

.imagen1 {
  flex: 0 0 auto;
  margin-right: 50px;
  margin-top: 10px;
}

.imagen1 img {
  height: auto;
  margin: 2px;
  max-width: 150px;
  margin-right: 30px;
  margin-left: 100px;
}

.question {
  font-family: 'Arial', sans-serif;
  text-align: center;
  flex-direction: row;
  margin-top: 60px;
  margin-block-end: 80px;
}

.question h5 {
  color: #000000;
  font-size: 20px;
  text-align: center;
  margin-bottom: 15px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.options {
  display: flex;
  flex-direction: column;
  border: 1px solid #e0e0e0;
  border-radius: 4px;
  overflow: hidden;
  width: 200px;
  align-items: center;
  justify-content: center;
  margin: 0 auto;
  margin-top: 25px;
}

label {
  display: flex;
  align-items: center;
  padding: 10px;
  cursor: pointer;
  font-size: 16px;
  background-color: #e0e0e0;
  transition: background-color 0.3s ease;
  width: 100%;
}

label:not(:last-child) {
  border-bottom: 1px solid #d9d9d9;
}

input[type='radio'] {
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  width: 20px;
  height: 20px;
  margin-right: 10px;
  background-color: #d0d0d0;
  border-radius: 3px;
  border: 1px solid #d9d9d9;
  display: inline-block;
  cursor: pointer;
  position: relative;
}

input[type='radio']:checked {
  background-color: #000000;
}

input[type='radio']:focus {
  outline: none;
}

span {
  font-weight: bold;
}

label:hover {
  background-color: #666;
}

.m-0 {
  text-align: right;
  color: #000000;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  letter-spacing: 3px;
}

.m-3 b {
  text-align: right;
  align-items: flex-end;
  flex-direction: row;
  color: #000000;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.px-3 {
  text-align: right;
  color: #000000;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.w-100 {
  height: 350px;
  box-shadow: #0b0b0b;
}

section {
  display: flex;
  width: 100%;
  height: 280px;
  margin: 0;
  padding: 0px;
  box-sizing: border-box;
  /* margin-block-end: 50px; */
}

section img {
  width: 20px;
  flex-grow: 1;
  object-fit: cover;
  opacity: 0.8;
  transition: 0.5s ease;
}

section img:hover {
  cursor: crosshair;
  width: 300px;
  opacity: 1;
  filter: contrast(120%);
}

.brunch {
  background-color: #f5f5f5;
  margin-top: 20px;
  margin-block-end: 20px;
}

.progress {
  border: 1px solid #d9d9d9;
  background-color: #ffffff;
}

.progress-bar {
  border: #666;
  background-color: #0b0b0b;
}

.d-flex img {
  height: 30px;
  margin: 2px;
  margin-right: 20px;
}

.d-flex .position-relative {
  height: 30px;
  margin: 55px;
}

.position-relative {
  width: 200px;
  position: relative;
  text-align: center;
}

.position-relative img {
  position: relative;
  text-align: center;
  align-items: center;
}

.img {
  width: 10px;
  height: 10px;
}

.icon-size {
  width: 20px;
  height: 20px;
  margin-right: 15px;
}

.icon-size:last-child {
  margin-right: 0;
}

.d-none,
.d-none h1 {
  margin-top: 0px;
  margin-bottom: 0.9rem;
  font-weight: 500;
  line-height: 3;
  font-size: 4rem;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  text-shadow: 3px 3px 2px #000000;
}

.d-none img {
  margin-top: 0px;
  margin-bottom: 0.5rem;
  font-weight: 500;
  line-height: 8;
}

.central {
  position: relative;
  text-align: center;
  margin: 20px 0;
}

.circle {
  display: inline-block;
  width: 40px;
  margin-right: 200px;
  position: relative;
  align-items: center;
  transform: translate(-45%, -50%);
  left: 27%;
  top: 70%;
}

.icon-overlay {
  position: relative;
  transform: translate(-10%, -10%);
  right: 8%;
  top: 30%;
  max-width: 23px;
}

.carousel-caption {
  position: absolute;
  bottom: 1.25rem;
  left: 15%;
  padding-top: 1.25rem;
  padding-bottom: 1.25rem;
  color: #fff;
  text-align: center;
  box-shadow: #0b0b0b;
}

.separator {
  border-left: 2px solid #0b0b0b;
  height: 40px;
  display: inline-block;
  margin-right: 20px;
}

figcaption {
  margin-top: 10px;
  color: #333;
  font-family: 'Arial', sans-serif;
}

h5 {
  margin: 5px 0;
  font-size: 18px;
  font-weight: bold;
  margin-top: 30px;
  margin-block-end: 10px;
}

p {
  margin: 0;
  font-size: 16px;
  color: #666;
}

/* a,
a .green {
  color: transparent;
} */
</style>
