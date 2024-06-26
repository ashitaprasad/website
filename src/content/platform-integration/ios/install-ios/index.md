---
title: Add iOS as a target platform for Flutter
description: Configure your system to develop Flutter for iOS.
short-title: Set up iOS compilation
target-list: [macOS, Android, web]
---

To choose the guide to add the iOS compiler and simulator
to your Flutter configuration,
click the [Getting Started path][] you followed.

<div class="card-deck mb-8">
{% for target in target-list %}
{% assign targetlink='/platform-integration/ios/install-ios/install-ios-from-' | append: target | downcase %}
  <a class="card card-app-type card-macos"
     id="install-{{target | downcase}}"
     href="{{targetlink}}">
    <div class="card-body">
      <header class="card-title text-center m-0">
        <span class="d-block h1">
          {% assign icon = target | downcase -%}
          {% case icon %}
          {% when 'macos' -%}
            <span class="material-symbols">laptop_mac</span>
          {% when 'android' -%}
            <span class="material-symbols">phone_android</span>
          {% when 'web' -%}
            <span class="material-symbols">web</span>
          {% endcase -%}
          <span class="material-symbols">add</span>
          <span class="material-symbols">phone_iphone</span>
        </span>
        <span class="text-muted d-block">
        Make iOS and {{ target }}{% if target == 'macOS' %} desktop{% endif %} apps
        </span>
      </header>
    </div>
  </a>
{% endfor %}
</div>

[Getting Started path]: /get-started/install
