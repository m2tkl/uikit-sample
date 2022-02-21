<script>
import UIkit from "uikit";
import Icons from "uikit/dist/js/uikit-icons";
import "uikit/dist/css/uikit.css";
import "uikit/dist/css/uikit.min.css";
UIkit.use(Icons);
</script>

<template>
  <header>
    <nav uk-navbar class="uk-navbar-conatiner uk-background-secondary uk-light">
      <div class="uk-navbar-left uk-margin-small-left">
        <a
          class="uk-navbar-item uk-logo uk-hidden@m"
          uk-icon="menu"
          uk-toggle="target: #offcanvas-nav"
        />
        <div class="uk-navbar-item uk-logo">
          <NuxtLink to="/">UIkit</NuxtLink>
        </div>
      </div>
      <div class="uk-navbar-right uk-margin-right">Menu</div>
    </nav>
  </header>

  <section class="uk-flex">
    <div
      class="
        sidenav
        uk-width-medium
        uk-section
        uk-section-secondary
        uk-padding-small
        uk-visible@m
      "
    >
      <ul uk-nav class="uk-nav-default uk-nav-parent-icon">
        <li class="uk-nav-header">Container</li>
        <li>
          <nuxt-link to="/container/dashboard">Dashboard</nuxt-link>
        </li>
        <li class="uk-parent">
          <a href="#">Parent</a>
          <ul class="uk-nav-sub">
            <li>
              <a href="#">Sub item</a>
            </li>
            <li>
              <a href="#">Sub item</a>
            </li>
          </ul>
        </li>
        <li class="uk-nav-header">Header</li>
        <li>
          <a href="#">
            <span class="uk-margin-small-right" uk-icon="icon: table"></span>
            Item</a
          >
        </li>
        <li>
          <a href="#">
            <span
              class="uk-margin-small-right"
              uk-icon="icon: thumbnails"
            ></span>
            Item</a
          >
        </li>
        <li class="uk-nav-divider"></li>
        <li>
          <a href="#">
            <span class="uk-margin-small-right" uk-icon="icon: trash"></span>
            Item</a
          >
        </li>
      </ul>
    </div>

    <div
      class="uk-width-auto"
      uk-offcanvas="overlay: true; esc-close: true; mode: none;"
    >
      <div class="uk-offcanvas-bar">
        <button class="uk-offcanvas-close" type="button" uk-close></button>

        <div id="offcanvas-nav"></div>
        <ul class="uk-nav uk-nav-default">
          <li class="uk-active"><a href="#">Active</a></li>
          <li class="uk-parent">
            <a href="#">Parent</a>
            <ul class="uk-nav-sub">
              <li><a href="#">Sub item</a></li>
              <li><a href="#">Sub item</a></li>
            </ul>
          </li>
          <li class="uk-nav-header">Header</li>
          <li>
            <a href="#"
              ><span class="uk-margin-small-right" uk-icon="icon: table"></span>
              Item</a
            >
          </li>
          <li>
            <a href="#"
              ><span
                class="uk-margin-small-right"
                uk-icon="icon: thumbnails"
              ></span>
              Item</a
            >
          </li>
          <li class="uk-nav-divider"></li>
          <li>
            <a href="#"
              ><span class="uk-margin-small-right" uk-icon="icon: trash"></span>
              Item</a
            >
          </li>
        </ul>
      </div>
    </div>

    <div
      class="main uk-width-expand uk-padding"
      uk-height-viewport="offset-top: 20"
    >
      <NuxtPage />
    </div>
  </section>
</template>
