# "CODE Marketing Cloud" スタートガイド

---

## [管理画面構成](/ja/admin/)

<ul>
  {% for page in site.html_pages %}
  {% if page.url contains "/ja/admin/" and page.url != "/ja/admin/" %}
  <li>
    <a href="{{ page.url }}">{{ page.title }}</a>
  </li>
  {% endif %}
  {% endfor %}
</ul>

---

## Web接客ツールについて

### [設定の流れ](/ja/in-browser/setting/)

#### 初期導入の流れ

<ul>
  {% for page in site.html_pages %}
  {% if page.url contains "/ja/in-browser/setting/site/" and page.url != "/ja/in-browser/setting/site/" %}
  <li>
    <a href="{{ page.url }}">{{ page.title }}</a>
  </li>
  {% endif %}
  {% endfor %}
</ul>

#### キャンペーン作成の流れ

<ul>
  {% for page in site.html_pages %}
  {% if page.url contains "/ja/in-browser/setting/campaign/" and page.url != "/ja/in-browser/setting/campaign/" %}
  <li>
    <a href="{{ page.url }}">{{ page.title }}</a>
  </li>
  {% endif %}
  {% endfor %}
</ul>

### [成果レポート](/ja/in-browser/report/)

<ul>
  {% for page in site.html_pages %}
  {% if page.url contains "/ja/in-browser/report/" and page.url != "/ja/in-browser/report/" %}
  <li>
    <a href="{{ page.url }}">{{ page.title }}</a>
  </li>
  {% endif %}
  {% endfor %}
</ul>

<!--
### [動的コンテンツの設定](/ja/in-browser/dynamic-contents/)

<ul>
  {% for page in site.html_pages %}
  {% if page.url contains "/ja/in-browser/dynamic-contents/" and page.url != "/ja/in-browser/dynamic-contents/" %}
  <li>
    <a href="{{ page.url }}">{{ page.title }}</a>
  </li>
  {% endif %}
  {% endfor %}
</ul>
-->


---

## [code.js ライブラリについて](/ja/js-sdk/)

<ul>
  {% for page in site.html_pages %}
  {% if page.url contains "/ja/js-sdk/" and page.url != "/ja/js-sdk/" %}
  <li>
    <a href="{{ page.url }}">{{ page.title }}</a>
  </li>
  {% endif %}
  {% endfor %}
</ul>

---

## [他ツールとの連携](/ja/integration/)

<ul>
  {% for page in site.html_pages %}
  {% if page.url contains "/ja/integration/" and page.url != "/ja/integration/" %}
  <li>
    <a href="{{ page.url }}">{{ page.title }}</a>
  </li>
  {% endif %}
  {% endfor %}
</ul>
