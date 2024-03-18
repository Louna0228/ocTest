# Hydeout

欢迎光临缝合拼凑恐怖馆！
您有可能在任何地方、任何时间、以任何身份遇见本馆。本着“友好、开放、平等”的原则，恐怖馆对每个有缘人开放！恐怖馆大门不设置门锁，您可以自由进入！

以下是入馆须知，请每一位友善的客人牢记在心:


<img alt="Mobile home page" src="/_screenshots/2.png?raw=true" width="300px" />
<img alt="Mobile post page" src="/_screenshots/3.png?raw=true" width="300px" />

### Usage

馆内禁止热武器，所有热武器将在进入洋馆后被空间锁定，处于无法使用也无法被破坏的状态。
馆内生活着6位住客和馆长。每位住客都有自己的活动范围，在你拜访住客之前，请务必确认住客们的喜恶以免发生不必要的争执。在没有收到邀请的情况下，住客们通常不会前往其他人的领地。
在地上建筑中，一楼大厅、二楼活动厅、三楼图书馆以及天台、所有走廊属于公共区域，你有可能在这里遇到任何一位住客和馆长。
馆长拥有恐怖馆的所有权，可以随意进入洋馆的任何一处。无论你在哪里遇到馆长都不是一件稀奇的事。馆长没有攻击性，请放心。
馆内提供定时刷新的食物和饮用水，但不保证食物的无害性。
馆内提供各种冷兵器和少量医疗用品，希望各位在使用时注意馆内卫生，如果能及时清理争执之后出现的血迹馆长会十分欣慰。
馆内存在机关和暗房，但不为拜访者提供详细地图，欢迎各位细心探索。
馆内各位住客皆为长期住客，来自于不同时空、不同世界。如果你从他们口中得到一些信息，请注意辨别这些信息的真假以及适用条件。
如需离开本馆，需要收集到3把钥匙，4个金苹果以及5颗宝石。将这些东西交给馆长，馆长会送你离开。
如果没有收集到足够的离馆必需物品，可以采用“等价交换”的方法向馆长换取该道具。
```
---
layout: index
title: Home
---
```


以上内容仅为面对拜访者的简要说明，希望各位拜访者在恐怖馆度过轻松愉快的人生。


### Keep It Simple

In keeping with the original Hyde theme, Hydeout aims to keep the overall
design lightweight and plugin-free. JavaScript is currently limited only
to Disqus and Google Analytics (and is only loaded if you provide configuration
variables).

Hydeout makes heavy use of Flexbox in its CSS. If Flexbox is not available,
the CSS degrades into a single column layout.

### Customization

Hydeout replaces Hyde's class-based theming with the use
of the following SASS variables:

```scss
$sidebar-bg-color: #202020 !default;
$sidebar-fg-color: white !default;
$sidebar-sticky: true !default;
$layout-reverse: false !default;
$link-color: #268bd2 !default;
```

To override these variables, create your own `assets/css/main.scss` file.
Define your own variables, then import in Hydeout's SCSS, like so:

```scss
---
# Jekyll needs front matter for SCSS files
---

$sidebar-bg-color: #ac4142;
$link-color: #ac4142;
$sidebar-sticky: false;
@import "hydeout";
```

See the [_variables](_sass/hydeout/_variables.scss) file for other variables
you can override.

You can see the full set of partials you can replace in the
[`_includes`](_includes) folder, but there are a few worth noting:

* `_includes/copyright.html` - Insert your own copyright here.

* `_includes/custom-head.html` - Insert custom head tags (e.g. to load your
  own stylesheets)

* `_includes/custom-foot.html` - Insert custom elements at the end of the
  body (e.g. for custom JS)

* `_includes/custom-nav-links.html` - Additional nav links to insert at the
  end of the list of links in the sidebar.

  Pro-tip: The `nav`s in the sidebar are flexboxes. Use the `order` property
  to order your links.

* `_includes/custom-icon-links.html`- Additional icon links to insert at the
  end of the icon links at the bottom of the sidebar. You can use the `order`
  property to re-order.

* `_includes/favicons.html` - Replace references to `favicon.ico` and
  `favicon.png` with your own favicons references.

* `_includes/font-includes.html` - The Abril Fatface font used for the site
  title is loaded here. If you're overriding that font in the CSS, be sure
  to also remove the font load reference here.

### New Features

* Hydeout adds a new tags page (accessible in the sidebar). Just create a
  new page with the tags layout:

  ```
  ---
  layout: tags
  title: Tags
  ---
  ```

* Hydeout adds a new "category" layout for dedicated category pages.
  Category pages are automatically added to the sidebar. All other pages
  must have `sidebar_link: true` in their front matter to show up in
  the sidebar. To create a category page, use the `category` layout"

  ```
  ---
  layout: category
  title: My Category
  ---

  Description of "My Category"
  ```

* You can control how pages are sorted by using the `sidebar_sort_order`
  parameter in the front matter. This works for both category and non-category
  pages, although non-category pages will always come first. Take a look at
  [`_includes/sidebar-nav-links.html`](./_includes/sidebar-nav-links.html) if
  you want to customize this behavior.

  ```
  ---
  layout: page
  title: My page
  sidebar_sort_order: 123
  ---

  Some content.
  ```

* A simple redirect-to-Google search is available. Just create a page with
  the `search` layout.

  ```
  ---
  layout: search
  title: Google Search
  ---
  ```

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
