<template>
  <div id="app">
<!--    <div id="maket"></div>-->
    <router-view/>
  </div>
</template>

<style lang="scss">
  *{margin:0;padding:0;box-sizing:border-box;background-position:center;background-repeat:no-repeat;outline: none;-webkit-tap-highlight-color: rgba(0,0,0,0);
    font-family: 'Roboto', sans-serif;
    font-weight: normal;
  }
  a:after,a:before,br:after,br:before,img:after,img:before,span:after,span:before,sup:after,sup:before,table:after,table:before,td:after,td:before,tr:after,tr:before{content:none}
  a{text-decoration:none;color:inherit;outline:0!important}
  button,input,textarea{outline:0; background: none; border: none;-webkit-tap-highlight-color: rgba(0,0,0,0)}
  #maket {
    background: url('../public/chronology/maket.jpg');
    position: absolute;
    top: 0px;
    left: 0;
    width: 100%;
    background-repeat: no-repeat;
    background-position: top center;
    opacity: 0.5;
    z-index: 5;
    height: 9000px;
  }
  /* width */
  ::-webkit-scrollbar {
    width: 4px;
  }

  /* Track */
  ::-webkit-scrollbar-track {
    background: #c5c5c5;
    border-radius: 2px;
  }

  /* Handle */
  ::-webkit-scrollbar-thumb {
    background: #6e6c79;
    border-radius: 2px;
  }

  /* Handle on hover */
  ::-webkit-scrollbar-thumb:hover {
    background: #b30000;
  }

  input[type="search"]::-webkit-search-decoration,
  input[type="search"]::-webkit-search-cancel-button,
  input[type="search"]::-webkit-search-results-button,
  input[type="search"]::-webkit-search-results-decoration {
      display: none;
  }
button, a {
    cursor: pointer;
}
  body {
    background: #FAFAFA;
  }
  .wrap {
    width: 100%;
    margin: 0 auto;
    max-width: 1476px;

  }
</style>
