# GitHub

## 1. 简要说明

## 2. 跟踪日志

### 2.1. 标签打开 <https://github.com>， 首先获取到的是document文档

参看 [HTML源码](./assets/github.init.html)

从HTML源码上看，可以确定以下几点：

- `GitHub 首页，采用服务器渲染(SSR)`
- 以下用法需要注意：
  - `link` 资源使用了以下特性
    - `dns-prefetch`: DNS 预获取。
      - [为什么要使用 dns-prefetch](https://developer.mozilla.org/zh-CN/docs/Web/Performance/dns-prefetch)
    - `preconnect`: 预连接。
      - [为什么要使用 preconnect](https://developer.mozilla.org/zh-CN/docs/Web/Preconnect),
      - [dns-prefetch，preconnect，prefetch和prerender的区别](https://segmentfault.com/a/1190000011065339)
    - `crossorign`: [跨源资源共享(CORS)](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/CORS)
      - `anonymous`: 匿名资源共享
    - `media`: `all`
    - `integrity`：为了防止CDN篡改资源，可以使用 `integrity` 属性
      - [js--script和link中的 integrity 属性](https://www.cnblogs.com/zuojiayi/p/7207031.html)
      - [link标签中的integrity和crossorigin字段](https://www.jianshu.com/p/7c7f00c0dc8c)
      - eg. `sha512-v+hxrr/7LrDH9DTy8tzqdDqKoXOnyWGr12dO4VTOYorMfADgcOjIRDVoy0RyTsLIj5gKzBTOpiFDwkze7/n8Iw==`
    - `rel`:
      - `rel = stylesheet`:
      - `rel = mask-icon`: Safari固定选项卡图标
        - 阅读文章: [https://developer.yoast.com/blog/safari-pinned-tab-icon-mask-icon/](https://developer.yoast.com/blog/safari-pinned-tab-icon-mask-icon/)
        - eg. `<link rel="mask-icon" href="https://github.githubassets.com/pinned-octocat.svg" color="#000000">`
      - `rel = alternate`:
        - 适用于PC站点
        - eg. `<link rel="alternate" type="application/atom+xml" title="ATOM" href="/lauer3912.private.atom?token=AAMPFSXIQDTZALS7672YVIV7F36DO" />`
      - `rel = alternate icon`:
        - eg. `<link rel="alternate icon" class="js-site-favicon" type="image/png" href="https://github.githubassets.com/favicons/favicon.png">`
      - `rel = icon`:
        - eg. `<link rel="icon" class="js-site-favicon" type="image/svg+xml" href="https://github.githubassets.com/favicons/favicon.svg">`
      - `rel = manifest`:
        - eg. `<link rel="manifest" href="/manifest.json">`
      - `rel = assets`:
        - eg. `<link rel="assets" href="https://github.githubassets.com/">`
      - `rel = shared-web-socket`
        > `<link rel="shared-web-socket" href="wss://alive.github.com/_sockets/u/1635018/ws?session=eyJ2IjoiVjMiLCJ1IjoxNjM1MDE4LCJzIjo3MTMyMjU3ODEsImMiOjMzNTQwMDg3MDYsInQiOjE2Mjk2OTA2Nzl9--87c63fd86a3e6e87f7a0e6f69d77ab3d87f234b99a08b02925d6a8dc899dd2c3" data-refresh-url="/_alive" data-session-id="de62121be298a192a3a4b349189208479f722db76ec5dae048b4eff98bfac6f8"> </link>`

      - `rel = shared-web-socket-src`:
        - eg. `<link rel="shared-web-socket-src" href="/socket-worker-3f088aa2.js">`
      - `rel = sudo-modal`:
        - eg. `<link rel="sudo-modal" href="/sessions/sudo_modal">`
  - `script` 资源使用了以下特性
    - `crossorigin`: `anonymous`
    - `defer`: `defer`
    - `integrity`：eg. `sha512-v+hxrr/7LrDH9DTy8tzqdDqKoXOnyWGr12dO4VTOYorMfADgcOjIRDVoy0RyTsLIj5gKzBTOpiFDwkze7/n8Iw==`
    - `data-module-id`: eg. "./chunk-access-groups.js"
    - `data-src`: eg. "<https://github.githubassets.com/assets/chunk-access-groups-bfe871ae.js>
