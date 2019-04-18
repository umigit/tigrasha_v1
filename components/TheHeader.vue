<template>
  <header>
    <div class="header-container">
      <div class="search-container">
        <input type="search" class="header-search" id="postSearch" />
      </div>
      <img class="header-icon" src="~assets/images/icon-white.png"/>
    </div>
  </header>
</template>

<script>
export default {

}
</script>

<style>
header {
  background-color: darkorange;
  height: 60px;
  width: 100%;
  position: fixed;
}

.header-container {
  height: 100%;
  width: 1020px;
  margin: 0 auto;
  display: flex;
  position: relative;
}

.search-container {
  width: 100%;
}

.header-search {
  background-color: white;
  box-sizing: border-box;
  width: 360px;
  height: 40px;
  margin: 10px;
  padding: 5px 20px 5px 5px;
  font-size: 16px;
}

.header-icon {
  height: 100%;
  padding: 10px;
  object-fit: contain;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

@media screen and (max-width: 1024px) {
  .header-container {
    width: 800px;
  }
}
@media screen and (max-width: 896px) {
  .header-container {
    width: 100%;
  }

  .header-icon {
    display: none;
  }
}
@media screen and (max-width: 480px) {
  .header-container {
    width: 100%;
  }

  .header-icon {
    display: none;
  }

  .search-container {
    width: 100%;
  }

  .header-search {
    box-sizing: border-box;
    width: calc(100% - 20px);
  }
}
</style>
