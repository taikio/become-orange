<template>
  <div class="page">
    <header class="page__header">
      <div class="page__header-logo">
        <img :src="logoPath" alt="Become Orange Logo" class="logo">
      </div>

      <div class="page__header-content">
        <h1>Become Orange Theme</h1>

        <p>
          This is a Visual Studio Code dark theme with orange highlight
        </p>

        <a
          href="https://marketplace.visualstudio.com/items?itemName=WelkerArantes.become-orange-theme"
          role="button"
        >
          Get it now from marketplace
        </a>
      </div>
    </header>

    <main class="row page__body">
      <div class="col page__body-content">
        <h1>Eye Friendly</h1>

        <p>
          Become Orange uses dark shades of orange and blue in its palette in order to provide
          a comfortable experience.
        </p>
      </div>

      <div class="col page__body-vuejs-image">
        <figure>
          <img :src="vueImagePath" alt="Vuejs Image">
        </figure>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    const logoPath = require('@/assets/images/become-orange-logo-no-background.png')
    const vueImagePath = require('@/assets/images/print-vscode-vuejs.png')

    return {
      logoPath,
      vueImagePath
    }
  }
}
</script>

<style lang="scss" scoped>
$page-background: #4B4B4B;
$primary-color: #DA8334;
$accent-color: #6F83BD;
$text-color: #FAFAFA;

.page {
  width: 96.6%;
  height: 100%;
  padding: 0 1.5rem;
  background: #4B4B4B;
  color: #FAFAFA;
}

.page__header {
  width: 100%;
  display: flex;
  flex-direction: row;
  min-height: 35vh;
  padding-bottom: 18px;
  border-bottom: 1px solid #6F83BD;
}

.page__header-logo {
  width: 32%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.page__header-logo img {
  width: 300px;
}

.page__header-content {
  width: 68%;
  display: flex;
  flex-direction: column;
}
.page__header-content h1 {
  font-family: 'Vampiro One', cursive;
  color: $accent-color;
  font-size: 3rem;
}
.page__header-content p {
  font-size: 1.9rem;
  color: $text-color;
  margin: 0;
}
.page__header-content a {
  width: 300px;
  padding: 12px 16px;
  border-radius: 6px;
  border: none;
  outline: none;
  text-decoration: none;
  background: $primary-color;
  font-size: 1.3rem;
  color: $text-color;
  text-align: center;
  margin-top: 32px;
  transition: 0.3s ease-in-out;
}
.page__header-content a:hover {
  background: #f2882c;
  color: #fff;
}

.page__body {
  margin-top: 20px;
}

.page__body-content {
  padding-top: 50px;
}
.page__body-content h1 {
  font-size: 2.4rem;
  color: $accent-color;
}
.page__body-content p {
  font-size: 1.7rem;
}

.page__body-vuejs-image figure {
  padding: 12px;
  border-radius: 6px;
  background: linear-gradient(180deg, #FFB674 0%, #A44E00 100%);
}
.page__body-vuejs-image figure img {
  max-width: 764px;
}



@media screen and (min-width: 1441px) and (max-width: 1930px) {

}

@media screen and (min-width: 1025px) and (max-width: 1440px) {
  .page__body-vuejs-image figure img {
    max-width: 630px;
  }
}

@media screen and (min-width: 769px) and (max-width: 1024px) {
  .page__body-vuejs-image figure img {
    max-width: 500px;
  }
}

@media screen and (min-width: 426px) and (max-width: 768px) {
  .page {
    width: 93.7%;
  }

  .page__header-logo img {
    width: 230px;
  }

  .page__body-vuejs-image figure img {
    max-width: 640px;
  }
}

@media screen and (max-width: 425px) {
  .page {
    width: 88.7%;
  }

  .page__header {
    flex-direction: column;
  }

  .page__header-logo {
    width: 90%;
    padding-top: 12px;
  }
  .page__header-logo img {
    width: 220px;
  }

  .page__header-content {
    width: 90%;
  }

  .page__body-vuejs-image figure img {
    max-width: 250px;
  }
}
</style>
