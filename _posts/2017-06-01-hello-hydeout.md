---
layout: post
title: welcom 恐怖馆
excerpt_separator:  <!--more-->
---

### 欢迎光临缝合拼凑恐怖馆！

您有可能在任何地方、任何时间、以任何身份遇见本馆。本着“友好、开放、平等”的原则，恐怖馆对每个有缘人开放！恐怖馆大门不设置门锁，您可以自由进入！

以下是入馆须知，请每一位友善的客人牢记在心:

- 馆内禁止热武器，所有热武器将在进入洋馆后被空间锁定，处于无法使用也无法被破坏的状态。
- 馆内生活着6位住客和馆长。每位住客都有自己的活动范围，在你拜访住客之前，请务必确认住客们的喜恶以免发生不必要的争执。在没有收到邀请的情况下，住客们通常不会前往其他人的领地。
- 在地上建筑中，一楼大厅、二楼活动厅、三楼图书馆以及天台、所有走廊属于公共区域，你有可能在这里遇到任何一位住客和馆长。
- 馆长拥有恐怖馆的所有权，可以随意进入洋馆的任何一处。无论你在哪里遇到馆长都不是一件稀奇的事。馆长没有攻击性，请放心。
- 馆内提供定时刷新的食物和饮用水，但不保证食物的无害性。
- 馆内提供各种冷兵器和少量医疗用品，希望各位在使用时注意馆内卫生，如果能及时清理争执之后出现的血迹馆长会十分欣慰。
- 馆内存在机关和暗房，但不为拜访者提供详细地图，欢迎各位细心探索。
- 馆内各位住客皆为长期住客，来自于不同时空、不同世界。如果你从他们口中得到一些信息，请注意辨别这些信息的真假以及适用条件。
- 如需离开本馆，需要收集到3把钥匙，4个金苹果以及5颗宝石。将这些东西交给馆长，馆长会送你离开。
- 如果没有收集到足够的离馆必需物品，可以采用“等价交换”的方法向馆长换取该道具。

### 请注意

以上内容仅为面对拜访者的简要说明，希望各位拜访者在恐怖馆度过轻松愉快的人生。

```scss
$sidebar-bg-color: #202020 !default;
$sidebar-fg-color: white !default;
$sidebar-sticky: true !default;
$layout-reverse: false !default;
$link-color: #268bd2 !default;
```

To override these variables, create your own `assets/css/main.scss` file.
Define your own variables, then import in Hydeout's SCSS, like so:

```
---
# Jekyll needs front matter for SCSS files
---

$sidebar-bg-color: #ac4142;
$link-color: #ac4142;
$sidebar-sticky: false;
@import "hydeout";
```

See the [_variables](https://github.com/fongandrew/hydeout/blob/master/_sass/hydeout/_variables.scss) file for other variables
you can override.

You can also insert custom head tags (e.g. to load your own stylesheets) by
defining your own `_includes/custom-head.html` or insert tags at the end
of the body (e.g. for custom JS) by defining your own
`_includes/custom-foot.html`.

### New Features

* Hydeout also adds a new tags page (accessible in the sidebar) and a new
  "category" layout for dedicated category pages.

* Category pages are automatically added to the sidebar. All other pages
  must have `sidebar_link: true` in their front matter to show up in
  the sidebar.

* A simple redirect-to-Google search is available. If you want to use
  Google Custom Search or Algolia or something with more involved,
  override the `search.html`.

* Disqus integration is ready out of the box. Just add the following to
  your config file:

  ```yaml
  disqus:
    shortname: my-disqus-shortname
  ```

  If you don't want Disqus or want to use something else, override
  `comments.html`.

* For Google Analytics support, define a `google_analytics` variable with
  your property ID in your config file.

There's also a bunch of minor tweaks and adjustments throughout the
theme. Hope this works for you!
