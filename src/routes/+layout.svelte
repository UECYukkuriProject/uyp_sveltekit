<script>
  import { page } from "$app/stores";
</script>

<h1>UEC Yukkuri Project</h1>

<nav>
  <a href="/" aria-current={$page.url.pathname === "/"}>トップ</a>
  <a href="/products" aria-current={$page.url.pathname === "/products"}>
    作ったもの
  </a>
  <a href="/members" aria-current={$page.url.pathname === "/members"}>
    メンバー
  </a>
</nav>

<slot />

<style>
  @import url(http://fonts.googleapis.com/earlyaccess/notosansjp.css);

  h1 {
    padding-top: 10px;
    background-color: tomato;
    color: black;
    -webkit-text-stroke: white 1px;
    text-align: center;
    font-weight: bold;
    font-family: "Noto Sans JP", sans-serif;
  }

  nav {
    padding: 10px;
    background-color: #e3e3e3;
    text-align: center;
    font-family: "Noto Sans JP", sans-serif;
  }

  a {
    margin: auto 1em auto;
    color: black;
    text-decoration: none;
  }

  a[aria-current="true"] {
    border-bottom: 2px solid;
  }
</style>
