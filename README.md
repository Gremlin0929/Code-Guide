

# Code-Guide

代码规范（根据自己代码风格做记录）

## 命名规则

### 项目（目录/文件/）命名

全部小写，以下划线分割。

例：my_project_name

## HTML

* 缩进使用soft tab（4个空格）。

* html标签上加lang属性（方便为语音工具和翻译工具提供帮助）。

  ```html
  <!DOCTYPE html>
  <html>
      ...
  </html>
  ```

  

* 属性应该按照特定的顺序出现以保证易读性；

  * `class`
  
  * `id`
  
  * `name`
  
  * `data-*`
  
  * `src` , `for` , `type`, `href` , `value` , `max-length` , `max` , `min` , `pattern`
  
  * `placeholder` , `title` , `alt`
  
  * `aria-*` , `role`
  
  * `required` , `readonly` , `disabled`
  
* boolean属性指不需要声明取值的属性。

  ​	boolean属性的存在表示取值为true，不存在则表示取值为false 

  ```html
  
  <input type="text" disabled>
  
  <input type="checkbox" value="1" checked>
  
  <select>
  	<option value="1" selected>1</option>
  </select>
  
  ```

* id采用驼峰式命名

  ```html
  <div id="myDiv">
      <span class="my-span"></span>
  </div>
  ```

  

* 尽量避免使用JS生成html标签，因为这样会让内容更难查找，更难编辑，性能更差。

## CSS

* 缩进使用soft tab（4个空格）。

* 注释统一使用‘/* */’ 。

  ```css
  /*
   * Modal Header
   */
  .modal-header{
      width: 100px;
      height: 100px;
      background-color: #000;
  }
  ```

  

* 引号

  * 最外层统一使用双引号；

  * url的内容要用引号；

  * 属性选择器中的属性需要引号。

    ```css
    .element:after {
        content: "";
        background-image: url("logo.png");
    }
    
    li[data-type="single"] {
        ...
    }
    ```

* 属性声明分组处理，组之间需要有一个空行

  ```css
  .declaration-order {
      display: block;
      float: right;
  
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      z-index: 100;
  
      border: 1px solid #e5e5e5;
      border-radius: 3px;
      width: 100px;
      height: 100px;
  
      font: normal 13px "Helvetica Neue", sans-serif;
      line-height: 1.5;
      text-align: center;
  
      color: #333;
      background-color: #f5f5f5;
  
      opacity: 1;
  }
  /* 
   * 下面是推荐的属性的顺序
   */
  [
      [
          "display",
          "visibility",
          "float",
          "clear",
          "overflow",
          "overflow-x",
          "overflow-y",
          "clip",
          "zoom"
      ],
      [
          "table-layout",
          "empty-cells",
          "caption-side",
          "border-spacing",
          "border-collapse",
          "list-style",
          "list-style-position",
          "list-style-type",
          "list-style-image"
      ],
      [
          "-webkit-box-orient",
          "-webkit-box-direction",
          "-webkit-box-decoration-break",
          "-webkit-box-pack",
          "-webkit-box-align",
          "-webkit-box-flex"
      ],
      [
          "position",
          "top",
          "right",
          "bottom",
          "left",
          "z-index"
      ],
      [
          "margin",
          "margin-top",
          "margin-right",
          "margin-bottom",
          "margin-left",
          "-webkit-box-sizing",
          "-moz-box-sizing",
          "box-sizing",
          "border",
          "border-width",
          "border-style",
          "border-color",
          "border-top",
          "border-top-width",
          "border-top-style",
          "border-top-color",
          "border-right",
          "border-right-width",
          "border-right-style",
          "border-right-color",
          "border-bottom",
          "border-bottom-width",
          "border-bottom-style",
          "border-bottom-color",
          "border-left",
          "border-left-width",
          "border-left-style",
          "border-left-color",
          "-webkit-border-radius",
          "-moz-border-radius",
          "border-radius",
          "-webkit-border-top-left-radius",
          "-moz-border-radius-topleft",
          "border-top-left-radius",
          "-webkit-border-top-right-radius",
          "-moz-border-radius-topright",
          "border-top-right-radius",
          "-webkit-border-bottom-right-radius",
          "-moz-border-radius-bottomright",
          "border-bottom-right-radius",
          "-webkit-border-bottom-left-radius",
          "-moz-border-radius-bottomleft",
          "border-bottom-left-radius",
          "-webkit-border-image",
          "-moz-border-image",
          "-o-border-image",
          "border-image",
          "-webkit-border-image-source",
          "-moz-border-image-source",
          "-o-border-image-source",
          "border-image-source",
          "-webkit-border-image-slice",
          "-moz-border-image-slice",
          "-o-border-image-slice",
          "border-image-slice",
          "-webkit-border-image-width",
          "-moz-border-image-width",
          "-o-border-image-width",
          "border-image-width",
          "-webkit-border-image-outset",
          "-moz-border-image-outset",
          "-o-border-image-outset",
          "border-image-outset",
          "-webkit-border-image-repeat",
          "-moz-border-image-repeat",
          "-o-border-image-repeat",
          "border-image-repeat",
          "padding",
          "padding-top",
          "padding-right",
          "padding-bottom",
          "padding-left",
          "width",
          "min-width",
          "max-width",
          "height",
          "min-height",
          "max-height"
      ],
      [
          "font",
          "font-family",
          "font-size",
          "font-weight",
          "font-style",
          "font-variant",
          "font-size-adjust",
          "font-stretch",
          "font-effect",
          "font-emphasize",
          "font-emphasize-position",
          "font-emphasize-style",
          "font-smooth",
          "line-height",
          "text-align",
          "-webkit-text-align-last",
          "-moz-text-align-last",
          "-ms-text-align-last",
          "text-align-last",
          "vertical-align",
          "white-space",
          "text-decoration",
          "text-emphasis",
          "text-emphasis-color",
          "text-emphasis-style",
          "text-emphasis-position",
          "text-indent",
          "-ms-text-justify",
          "text-justify",
          "letter-spacing",
          "word-spacing",
          "-ms-writing-mode",
          "text-outline",
          "text-transform",
          "text-wrap",
          "-ms-text-overflow",
          "text-overflow",
          "text-overflow-ellipsis",
          "text-overflow-mode",
          "-ms-word-wrap",
          "word-wrap",
          "-ms-word-break",
          "word-break"
      ],
      [
          "color",
          "background",
          "filter:progid:DXImageTransform.Microsoft.AlphaImageLoader",
          "background-color",
          "background-image",
          "background-repeat",
          "background-attachment",
          "background-position",
          "-ms-background-position-x",
          "background-position-x",
          "-ms-background-position-y",
          "background-position-y",
          "-webkit-background-clip",
          "-moz-background-clip",
          "background-clip",
          "background-origin",
          "-webkit-background-size",
          "-moz-background-size",
          "-o-background-size",
          "background-size"
      ],
      [
          "outline",
          "outline-width",
          "outline-style",
          "outline-color",
          "outline-offset",
          "opacity",
          "filter:progid:DXImageTransform.Microsoft.Alpha(Opacity",
          "-ms-filter:\\'progid:DXImageTransform.Microsoft.Alpha",
          "-ms-interpolation-mode",
          "-webkit-box-shadow",
          "-moz-box-shadow",
          "box-shadow",
          "filter:progid:DXImageTransform.Microsoft.gradient",
          "-ms-filter:\\'progid:DXImageTransform.Microsoft.gradient",
          "text-shadow"
      ],
      [
          "-webkit-transition",
          "-moz-transition",
          "-ms-transition",
          "-o-transition",
          "transition",
          "-webkit-transition-delay",
          "-moz-transition-delay",
          "-ms-transition-delay",
          "-o-transition-delay",
          "transition-delay",
          "-webkit-transition-timing-function",
          "-moz-transition-timing-function",
          "-ms-transition-timing-function",
          "-o-transition-timing-function",
          "transition-timing-function",
          "-webkit-transition-duration",
          "-moz-transition-duration",
          "-ms-transition-duration",
          "-o-transition-duration",
          "transition-duration",
          "-webkit-transition-property",
          "-moz-transition-property",
          "-ms-transition-property",
          "-o-transition-property",
          "transition-property",
          "-webkit-transform",
          "-moz-transform",
          "-ms-transform",
          "-o-transform",
          "transform",
          "-webkit-transform-origin",
          "-moz-transform-origin",
          "-ms-transform-origin",
          "-o-transform-origin",
          "transform-origin",
          "-webkit-animation",
          "-moz-animation",
          "-ms-animation",
          "-o-animation",
          "animation",
          "-webkit-animation-name",
          "-moz-animation-name",
          "-ms-animation-name",
          "-o-animation-name",
          "animation-name",
          "-webkit-animation-duration",
          "-moz-animation-duration",
          "-ms-animation-duration",
          "-o-animation-duration",
          "animation-duration",
          "-webkit-animation-play-state",
          "-moz-animation-play-state",
          "-ms-animation-play-state",
          "-o-animation-play-state",
          "animation-play-state",
          "-webkit-animation-timing-function",
          "-moz-animation-timing-function",
          "-ms-animation-timing-function",
          "-o-animation-timing-function",
          "animation-timing-function",
          "-webkit-animation-delay",
          "-moz-animation-delay",
          "-ms-animation-delay",
          "-o-animation-delay",
          "animation-delay",
          "-webkit-animation-iteration-count",
          "-moz-animation-iteration-count",
          "-ms-animation-iteration-count",
          "-o-animation-iteration-count",
          "animation-iteration-count",
          "-webkit-animation-direction",
          "-moz-animation-direction",
          "-ms-animation-direction",
          "-o-animation-direction",
          "animation-direction"
      ],
      [
          "content",
          "quotes",
          "counter-reset",
          "counter-increment",
          "resize",
          "cursor",
          "-webkit-user-select",
          "-moz-user-select",
          "-ms-user-select",
          "user-select",
          "nav-index",
          "nav-up",
          "nav-right",
          "nav-down",
          "nav-left",
          "-moz-tab-size",
          "-o-tab-size",
          "tab-size",
          "-webkit-hyphens",
          "-moz-hyphens",
          "hyphens",
          "pointer-events"
      ]
  ]
  ```

* 尽量不适用简写属性（`margin` 和 `padding` 除外）

  ```css
  /* not good */
  .element {
      transition: opacity 1s linear 2s;
  }
  
  /* good */
  .element {
      transition-delay: 2s;
      transition-timing-function: linear;
      transition-duration: 1s;
      transition-property: opacity;
  }
  ```

* 无前缀的标准属性应该写在有前缀的属性后面

  ```css
  .element {
      -webkit-border-radius: 3px;
         -moz-border-radius: 3px;
              border-radius: 3px;
  
      background: -webkit-linear-gradient(top, #fff 0, #eee 100%);
      background:    -moz-linear-gradient(top, #fff 0, #eee 100%);
      background:         linear-gradient(to bottom, #fff 0, #eee 100%);
  }
  ```

## JavaScript

* 缩进使用soft tab（4个空格）。

* 尽量不要省略分号 `;`

* 最外层统一使用单引号

* 驼峰式命名

  * 'ID' 在变量名中全大写

    ```javascript
    var personID = '2345678';
    ```

  * 'URL' 在变量名中全大写

    ```javascript
    var queryURL = 'github.com';
    ```

  * 常亮全大写，用下划线连接

    ```javascript
    var MAX_VALUE = 4567;
    ```

  * 构造函数，第一个字母大写

    ```javascript
    function Student(name){
        this.name = name;
    }
    ```

  * jquery对象必须以 '$' 开头命名

    ```javascript
    var $body = $('body');
    ```

  * 尽量不要省略大括号 '{}'

    ```javascript
    if (true) {
        doSomething();
    }
    ```

  * 变量声明时即初始化

    ```javascript
    var str = '';
    var num = 3;
    var boo = false;
    var arr = [];
    var obj = null;
    ```

  * 使用 `===` , `!===` 代替 `==` , `!=`

    ```javascript
    if (a === '1') {
        b = '2';
    }
    ```

  * `for-in` 中一定要有 `hasOwnProperty` 的判断

    ```javascript
    for (key in obj) {
        if (obj.hasOwnProperty(key)) {
            // 确保 obj中包含非继承的obj[key]
            console.log(obj[key]);
        }
    }
    ```

    

