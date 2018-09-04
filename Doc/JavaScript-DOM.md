

2018-09-03

##### History

| 属性   | 描述                                                  |
| :----- | :---------------------------------------------------- |
| length | 返回浏览器历史列表中的URL数量。(列表中指的是当前窗口) |



| 方法      | 描述                                                         |
| :-------- | :----------------------------------------------------------- |
| back()    | 加载 history 列表中的前一个 URL---------history.back()       |
| forward() | 加载history列表中的下一个URL---------history.forward()       |
| go()      | 加载 history 列表中的某个具体页面---------history.go(number[正前负后]\|URL) |



##### Location

| 属性     | 描述                              |
| :------- | :-------------------------------- |
| href     | 设置或返回完整的URL               |
| host     | 设置或返回主机名和当前URL的端口号 |
| hostname | 设置或返回当前URL主机名           |
| port     | 设置或返回当前URL端口号           |
| hash     | 设置或返回锚点                    |
| pathname | 设置或返回当前URL的路径           |
| protocal | 设置或返回当前URL协议             |
| search   | 设置或返回URL参数                 |

​

| 方法      | 描述             |
| --------- | ---------------- |
| reload()  | 重载             |
| assign()  | 加载新的文档     |
| replace() | 用新文档替换当前 |



##### JavaScript的三种跳转方式

  1. location.replace(newURL)
  2. location.assign(newURL)
  3. location.href = "https://www.baidu.com"



##### Screen

​	

| 属性   | 方法                 |
| ------ | -------------------- |
| width  | 返回显示器屏幕的宽度 |
| height | 返回显示器屏幕的高度 |



##### Navigator

| 属性       | 方法                                         |
| ---------- | -------------------------------------------- |
| appVersion | 返回浏览器的平台和版本信息                   |
| userAgent  | 返回由客户机发送服务器的 user-agent 头部的值 |



## DOM 文档对象模型

​	

### Document对象



###### Document对象集合

| 集合   | 描述                                           |
| ------ | ---------------------------------------------- |
| all    | 页面中所有标签,不去重,返回一个数组             |
| forms  | 返回对文档中所有 Form 对象的引用,返回一个数组  |
| images | 返回对文档中所有 Image 对象的引用,返回一个数组 |
| links  | 返回对文档中所有 Area 和 Link 对象的引用       |



###### Document对象属性

| 属性         | 描述                                                         |
| ------------ | ------------------------------------------------------------ |
| domain       | 返回当前服务器域名                                           |
| lastModified | 返回文档被最后修改的日期和时间<br />该值来自于 Last-Modified HTTP 头部, 它是由 Web 服务器发送的可选项 |
| title        | 当前文档的标题                                               |
| URL          | URL 属性可返回当前文档的 URL                                 |
| referrer     | 上一跳地址来源                                               |
| cookie       | cookie是之前php脚本通过setcookie()设置到客户端浏览器的<br>创建/修改cookie <br>document.cookie = 'sex = "女 " '; <br>**设置过期时间** <br>*1.new时间对象*<br>var oDate = new Date(); <br>*2.设置过期时间*<br>oDate.setTime(oDate.getTime() + 60\*60*1000); <br>*3*.转为UTC时间*<br>document.cookie = 'username=xx; path=/; expires='+d.toUTCString(); <br>**删除cookie** <br>将时间设置为过期时间 |

###### Document的对象方法

| 方法                   | 描述                                     |
| ---------------------- | ---------------------------------------- |
| getElementById()       | 返回对拥有指定 ID 的第一个对象的引用     |
| getElementsByName()    | 返回带有指定名称的对象的集合             |
| getElementsByTagName() | 可返回带有指定标签名的对象的集合         |
| write()                | 向文档写入 HTML 表达式或 JavaScript 代码 |





### Form对象

###### Form对象属性

```
acceptCharset 	 服务器可接受的字符集。 
action 			设置或返回表单的 action 属性。 
enctype 		设置或返回表单用来编码内容的 MIME 类型。 
id 			    设置或返回表单的 id。 
length 			返回表单中的元素数目。 
method 			设置或返回将数据发送到服务器的 HTTP 方法。 
name 			设置或返回表单的名称。 
target 			设置或返回表单提交结果的 Frame 或 Window 名。 

```

###### Form的对象方法

| 方法     | 描述                             |
| -------- | -------------------------------- |
| reset()  | 把表单中的元素重置为它们的默认值 |
| submit() | 提交表单                         |

###### Form对象事件句柄

| 事件句柄 | 描述                   |
| -------- | ---------------------- |
| onreset  | 在重置表单元素之前调用 |
| onsubmit | 在提交表单之前调用     |

###### Form表单提交的三种方式

1. 直接在form表单中设置提交按钮或button
2. 使用HTML5方法,在表单外面也可使用,类似label
3. 使用JavaScript中的submit()方法







### Image对象

###### Image对象的属性

```
align 	 	设置或返回与内联内容的对齐方式。 
alt 	 	设置或返回无法显示图像时的替代文本。 
border 	 	设置或返回图像周围的边框。 
complete 	返回浏览器是否已完成对图像的加载。 
height 		设置或返回图像的高度。 
hspace 		设置或返回图像左侧和右侧的空白。 
id 			设置或返回图像的 id。 
isMap 		返回图像是否是服务器端的图像映射。 
longDesc 	设置或返回指向包含图像描述的文档的 URL。 
lowsrc 		设置或返回指向图像的低分辨率版本的 URL。 
name 		设置或返回图像的名称。 
src 		设置或返回图像的 URL。 
useMap 		设置或返回客户端图像映射的 usemap 属性的值。 
vspace 		设置或返回图像的顶部和底部的空白。 
width 		设置或返回图像的宽度。 

```

###### Image对象的事件句柄

| 事件句柄 | 描述                                       |
| -------- | ------------------------------------------ |
| onerror  | 在加载图像的过程中发生错误时调用的事件句柄 |
| onabort  | 当用户放弃图像的加载时调用的事件句柄       |
| onload   | 当图像加载完成时调用的事件句柄             |







### Anchor 对象

###### Anchor对象的属性

```
accessKey 		 设置或返回访问一个链接的快捷键。 
charset 		 设置或返回被链接资源的字符集。 
coords 			 设置或返回逗号分隔列表，包含了图像映射中链接的坐标。 
href 			 设置或返回被链接资源的 URL。 
hreflang		 设置或返回被链接资源的语言代码。 
id 				 设置或返回一个链接的 id。 
innerHTML 		  设置或返回一个链接的内容。 
name     		  设置或返回一个链接的名称。 
rel 			  设置或返回当前文档与目标 URL 之间的关系。 
rev 			  设置或返回目标 URL 与之间当前文档的关系。 
shape 			  设置或返回图像映射中某个链接的形状。 
tabIndex 		  设置或返回某个链接的 Tab 键控制次序。 
target 			  设置或返回在何处打开链接。 
type 			  设置或返回被链接资源的 MIME 类型。 
```

###### Anchor对象的方法

| 方法  | 描述               |
| ----- | ------------------ |
| focus | 给链接应用焦点     |
| blur  | 把焦点从链接上移开 |









### Base对象

###### Base对象的属性

| 属性   | 描述                                             |
| ------ | ------------------------------------------------ |
| href   | 设置或返回针对页面中所有链接的基准 URL           |
| id     | 设置或返回 <base> 元素的 id                      |
| target | 设置或返回针对页面中所有链接的默认打开位置的窗口 |







### Canvs对象

###### 	

###### CanvasRenderingContext2D 对象的方法

| 方法                   | 描述                                                         |
| ---------------------- | ------------------------------------------------------------ |
| arc()                  | 用一个中心点和半径，为一个画布的当前子路径添加一条弧线。     |
| arcTo()                | 使用目标点和一个半径，为当前的子路径添加一条弧线。           |
| beginPath()            | 开始一个画布中的一条新路径（或者子路径的一个集合）。         |
| bezierCurveTo()        | 为当前的子路径添加一个三次贝塞尔曲线。                       |
| clearRect()            | 在一个画布的一个矩形区域中清除掉像素。                       |
| clip()                 | 使用当前路径作为连续绘制操作的剪切区域。                     |
| closePath()            | 如果当前子路径是打开的，就关闭它。                           |
| createLinearGradient() | 返回代表线性颜色渐变的一个 CanvasGradient 对象。             |
| createPattern()        | 返回代表贴图图像的一个 CanvasPattern 对象。                  |
| createRadialGradient() | 返回代表放射颜色渐变的一个 CanvasGradient 对象。             |
| drawImage()            | 绘制一幅图像。                                               |
| fill()                 | 使用指定颜色、渐变或模式来绘制或填充当前路径的内部。         |
| fillRect()             | 绘制或填充一个矩形。                                         |
| lineTo()               | 为当前的子路径添加一条直线线段。                             |
| moveTo()               | 设置当前位置并开始一条新的子路径。                           |
| quadraticCurveTo()     | 为当前路径添加一条贝塞尔曲线。                               |
| rect()                 | 为当前路径添加一条矩形子路径。                               |
| restore()              | 为画布重置为最近保存的图像状态。                             |
| rotate()               | 旋转画布。                                                   |
| save()                 | 保存 CanvasRenderingContext2D 对象的属性、剪切区域和变换矩阵。 |
| scale()                | 标注画布的用户坐标系统。                                     |
| stroke()               | 沿着当前路径绘制或画一条直线。                               |
| strokeRect()           | 绘制（但不填充）一个矩形。                                   |
| translate()            | 转换画布的用户坐标系统。                                     |



##### HTML5canvs操作

###### 颜色、样式和阴影

| 属性          | 描述                                     |
| ------------- | ---------------------------------------- |
| fillStyle     | 设置或返回用于填充绘画的颜色、渐变或模式 |
| strokeStyle   | 设置或返回用于笔触的颜色、渐变或模式     |
| shadowColor   | 设置或返回用于阴影的颜色                 |
| shadowBlur    | 设置或返回用于阴影的模糊级别             |
| shadowOffsetX | 设置或返回阴影距形状的水平距离           |
| shadowOffsetY | 设置或返回阴影距形状的垂直距离           |

| 方法                   | 描述                                    |
| ---------------------- | --------------------------------------- |
| createLinearGradient() | 创建线性渐变（用在画布内容上）          |
| createPattern()        | 在指定的方向上重复指定的元素            |
| createRadialGradient() | 创建放射状/环形的渐变（用在画布内容上） |
| addColorStop()         | 规定渐变对象中的颜色和停止位置          |

###### 线条样式

| 属性       | 描述                                     |
| ---------- | ---------------------------------------- |
| lineCap    | 设置或返回线条的结束端点样式             |
| lineJoin   | 设置或返回两条线相交时，所创建的拐角类型 |
| lineWidth  | 设置或返回当前的线条宽度                 |
| miterLimit | 设置或返回最大斜接长度                   |

###### 矩形

| 方法         | 描述                         |
| ------------ | ---------------------------- |
| rect()       | 创建矩形                     |
| fillRect()   | 绘制“被填充”的矩形           |
| strokeRect() | 绘制矩形（无填充）           |
| clearRect()  | 在给定的矩形内清除指定的像素 |

###### 路径

| 方法               | 描述                                                    |
| ------------------ | ------------------------------------------------------- |
| fill()             | 填充当前绘图（路径）                                    |
| stroke()           | 绘制已定义的路径                                        |
| beginPath()        | 起始一条路径，或重置当前路径                            |
| moveTo()           | 把路径移动到画布中的指定点，不创建线条                  |
| closePath()        | 创建从当前点回到起始点的路径                            |
| lineTo()           | 添加一个新点，然后在画布中创建从该点到最后指定点的线条  |
| clip()             | 从原始画布剪切任意形状和尺寸的区域                      |
| quadraticCurveTo() | 创建二次贝塞尔曲线                                      |
| bezierCurveTo()    | 创建三次方贝塞尔曲线                                    |
| arc()              | 创建弧/曲线（用于创建圆形或部分圆）                     |
| arcTo()            | 创建两切线之间的弧/曲线                                 |
| isPointInPath()    | 如果指定的点位于当前路径中，则返回 true，否则返回 false |

###### 转换

| 方法           | 描述                                           |
| -------------- | ---------------------------------------------- |
| scale()        | 缩放当前绘图至更大或更小                       |
| rotate()       | 旋转当前绘图                                   |
| translate()    | 重新映射画布上的 (0,0) 位置                    |
| transform()    | 替换绘图的当前转换矩阵                         |
| setTransform() | 将当前转换重置为单位矩阵。然后运行 transform() |

###### 文本

| 属性         | 描述                                     |
| ------------ | ---------------------------------------- |
| font         | 设置或返回文本内容的当前字体属性         |
| textAlign    | 设置或返回文本内容的当前对齐方式         |
| textBaseline | 设置或返回在绘制文本时使用的当前文本基线 |

| 方法          | 描述                       |
| ------------- | -------------------------- |
| fillText()    | 在画布上绘制“被填充的”文本 |
| strokeText()  | 在画布上绘制文本（无填充） |
| measureText() | 返回包含指定文本宽度的对象 |

###### 图像绘制

| 方法        | 描述                         |
| ----------- | ---------------------------- |
| drawImage() | 向画布上绘制图像、画布或视频 |

###### 像素操作

| 属性   | 描述                                                |
| ------ | --------------------------------------------------- |
| width  | 返回 ImageData 对象的宽度                           |
| height | 返回 ImageData 对象的高度                           |
| data   | 返回一个对象，其包含指定的 ImageData 对象的图像数据 |

| 方法              | 描述                                                      |
| ----------------- | --------------------------------------------------------- |
| createImageData() | 创建新的、空白的 ImageData 对象                           |
| getImageData()    | 返回 ImageData 对象，该对象为画布上指定的矩形复制像素数据 |
| putImageData()    | 把图像数据（从指定的 ImageData 对象）放回画布上           |

###### 合成

| 属性                     | 描述                                   |
| ------------------------ | -------------------------------------- |
| globalAlpha              | 设置或返回绘图的当前 alpha 或透明值    |
| globalCompositeOperation | 设置或返回新图像如何绘制到已有的图像上 |

###### 其他

| 方法          | 描述                           |
| ------------- | ------------------------------ |
| save()        | 保存当前环境的状态             |
| restore()     | 返回之前保存过的路径状态和属性 |
| createEvent() |                                |
| getContext()  |                                |
| toDataURL()   |                                |





### Event对象

###### 	

###### 事件句柄

| 属性        | 此事件发生在何时...                  |
| ----------- | ------------------------------------ |
| onabort     | 图像的加载被中断。                   |
| onblur      | 元素失去焦点。                       |
| onchange    | 域的内容被改变。                     |
| onclick     | 当用户点击某个对象时调用的事件句柄。 |
| ondblclick  | 当用户双击某个对象时调用的事件句柄。 |
| onerror     | 在加载文档或图像时发生错误。         |
| onfocus     | 元素获得焦点。                       |
| onkeydown   | 某个键盘按键被按下。                 |
| onkeypress  | 某个键盘按键被按下并松开。           |
| onkeyup     | 某个键盘按键被松开。                 |
| onload      | 一张页面或一幅图像完成加载。         |
| onmousedown | 鼠标按钮被按下。                     |
| onmousemove | 鼠标被移动。                         |
| onmouseout  | 鼠标从某元素移开。                   |
| onmouseover | 鼠标移到某元素之上。                 |
| onmouseup   | 鼠标按键被松开。                     |
| onreset     | 重置按钮被点击。                     |
| onresize    | 窗口或框架被重新调整大小。           |
| onselect    | 文本被选中。                         |
| onsubmit    | 确认按钮被点击。                     |
| onunload    | 用户退出页面。                       |

###### 鼠标 / 键盘属性

| 属性          | 描述                                         |
| ------------- | -------------------------------------------- |
| altKey        | 返回当事件被触发时，"ALT" 是否被按下。       |
| button        | 返回当事件被触发时，哪个鼠标按钮被点击。     |
| clientX       | 返回当事件被触发时，鼠标指针的水平坐标。     |
| clientY       | 返回当事件被触发时，鼠标指针的垂直坐标。     |
| ctrlKey       | 返回当事件被触发时，"CTRL" 键是否被按下。    |
| metaKey       | 返回当事件被触发时，"meta" 键是否被按下。    |
| relatedTarget | 返回与事件的目标节点相关的节点。             |
| screenX       | 返回当某个事件被触发时，鼠标指针的水平坐标。 |
| screenY       | 返回当某个事件被触发时，鼠标指针的垂直坐标。 |
| shiftKey      | 返回当事件被触发时，"SHIFT" 键是否被按下。   |

###### IE 属性

除了上面的鼠标/事件属性，IE 浏览器还支持下面的属性：

| 属性            | 描述                                                         |
| --------------- | ------------------------------------------------------------ |
| cancelBubble    | 如果事件句柄想阻止事件传播到包容对象，必须把该属性设为 true。 |
| fromElement     | 对于 mouseover 和 mouseout 事件，fromElement 引用移出鼠标的元素。 |
| keyCode         | 对于 keypress 事件，该属性声明了被敲击的键生成的 Unicode 字符码。对于 keydown 和 keyup  事件，它指定了被敲击的键的虚拟键盘码。虚拟键盘码可能和使用的键盘的布局相关。 |
| offsetX,offsetY | 发生事件的地点在事件源元素的坐标系统中的 x 坐标和 y 坐标。   |
| returnValue     | 如果设置了该属性，它的值比事件句柄的返回值优先级高。把这个属性设置为 fasle，可以取消发生事件的源元素的默认动作。 |
| srcElement      | 对于生成事件的 Window 对象、Document 对象或 Element 对象的引用。 |
| toElement       | 对于 mouseover 和 mouseout 事件，该属性引用移入鼠标的元素。  |
| x,y             | 事件发生的位置的 x 坐标和 y 坐标，它们相对于用CSS动态定位的最内层包容元素。 |

###### 标准 Event 属性

下面列出了 2 级 DOM 事件标准定义的属性。

| 属性          | 描述                                           |
| ------------- | ---------------------------------------------- |
| bubbles       | 返回布尔值，指示事件是否是起泡事件类型。       |
| cancelable    | 返回布尔值，指示事件是否可拥可取消的默认动作。 |
| currentTarget | 返回其事件监听器触发该事件的元素。             |
| eventPhase    | 返回事件传播的当前阶段。                       |
| target        | 返回触发此事件的元素（事件的目标节点）。       |
| timeStamp     | 返回事件生成的日期和时间。                     |
| type          | 返回当前 Event 对象表示的事件的名称。          |

###### 标准 Event 方法

下面列出了 2 级 DOM 事件标准定义的方法。IE 的事件模型不支持这些方法：

| 方法              | 描述                                     |
| ----------------- | ---------------------------------------- |
| initEvent()       | 初始化新创建的 Event 对象的属性。        |
| preventDefault()  | 通知浏览器不要执行与事件关联的默认动作。 |
| stopPropagation() | 不再派发事件。                           |



### Input对象

###### Input对象方法

| 方法     | 描述                                                         |
| -------- | ------------------------------------------------------------ |
| blur()   | 把焦点从表单上移开                                           |
| click()  | 模拟一次鼠标单击                                             |
| focus()  | 表单赋予焦点                                                 |
| select() | 全选<br>var oC = document.getElementById('copy');<br />oC.onclick = function() {<br />if (window.clipboardData) {<br />// 复制类型,复制的值<br />clipboardData.setData('text',oT.value);<br />alert('已复制到剪切板');<br />}else{<br />oT.select();<br />alert('请使用ctrl+c复制');<br />}<br />} |







### select对象

###### select对象集合

```
options
如果把 options.length 属性设置为 0,Select 对象中所有选项都会被清除。 
如果 options.length 属性的值比当前值小，出现在数组尾部的元素就会被丢弃。 
如果把 options[] 数组中的一个元素设置为 null，那么选项就会从 Select 对象中删除。 
可以通过构造函数 Option() 来创建一个新的 option 对象（需要设置 options.length 属性）。 
```

###### select对象方法

| 方法     | 对象                     |
| -------- | ------------------------ |
| add()    | 向下拉列表添加一个选项   |
| blur()   | 从下拉列表移开焦点       |
| focus()  | 在下拉列表上设置焦点     |
| remove() | 从下拉列表中删除一个选项 |

###### select对象事件句柄

| 事件句柄 | 描述                       |
| -------- | -------------------------- |
| onchange | 当改变选择时调用的事件句柄 |



### style对象

###### Background 属性

| 属性                 | 描述                              |
| -------------------- | --------------------------------- |
| background           | 在一行中设置所有的背景属性        |
| backgroundAttachment | 设置背景图像是否固定或随页面滚动  |
| backgroundColor      | 设置元素的背景颜色                |
| backgroundImage      | 设置元素的背景图像                |
| backgroundPosition   | 设置背景图像的起始位置            |
| backgroundPositionX  | 设置backgroundPosition属性的X坐标 |
| backgroundPositionY  | 设置backgroundPosition属性的Y坐标 |
| backgroundRepeat     | 设置是否及如何重复背景图像        |

###### Border 和 Margin 属性

| 属性              | 描述                                    |
| ----------------- | --------------------------------------- |
| border            | 在一行设置四个边框的所有属性            |
| borderBottom      | 在一行设置底边框的所有属性              |
| borderBottomColor | 设置底边框的颜色                        |
| borderBottomStyle | 设置底边框的样式                        |
| borderBottomWidth | 设置底边框的宽度                        |
| borderColor       | 设置所有四个边框的颜色 (可设置四种颜色) |
| borderLeft        | 在一行设置左边框的所有属性              |
| borderLeftColor   | 设置左边框的颜色                        |
| borderLeftStyle   | 设置左边框的样式                        |
| borderLeftWidth   | 设置左边框的宽度                        |
| borderRight       | 在一行设置右边框的所有属性              |
| borderRightColor  | 设置右边框的颜色                        |
| borderRightStyle  | 设置右边框的样式                        |
| borderRightWidth  | 设置右边框的宽度                        |
| borderStyle       | 设置所有四个边框的样式 (可设置四种样式) |
| borderTop         | 在一行设置顶边框的所有属性              |
| borderTopColor    | 设置顶边框的颜色                        |
| borderTopStyle    | 设置顶边框的样式                        |
| borderTopWidth    | 设置顶边框的宽度                        |
| borderWidth       | 设置所有四条边框的宽度 (可设置四种宽度) |
| margin            | 设置元素的边距 (可设置四个值)           |
| marginBottom      | 设置元素的底边距                        |
| marginLeft        | 设置元素的左边距                        |
| marginRight       | 设置元素的右边据                        |
| marginTop         | 设置元素的顶边距                        |
| outline           | 在一行设置所有的outline属性             |
| outlineColor      | 设置围绕元素的轮廓颜色                  |
| outlineStyle      | 设置围绕元素的轮廓样式                  |
| outlineWidth      | 设置围绕元素的轮廓宽度                  |
| padding           | 设置元素的填充 (可设置四个值)           |
| paddingBottom     | 设置元素的下填充                        |
| paddingLeft       | 设置元素的左填充                        |
| paddingRight      | 设置元素的右填充                        |
| paddingTop        | 设置元素的顶填充                        |

###### Layout 属性

| 属性             | 描述                                                         |
| ---------------- | ------------------------------------------------------------ |
| clear            | 设置在元素的哪边不允许其他的浮动元素                         |
| clip             | 设置元素的形状                                               |
| content          | 设置元信息                                                   |
| counterIncrement | 设置其后是正数的计数器名称的列表。其中整数指示每当元素出现时计数器的增量。默认是1。 |
| counterReset     | 设置其后是正数的计数器名称的列表。其中整数指示每当元素出现时计数器被设置的值。默认是0。 |
| cssFloat         | 设置图像或文本将出现（浮动）在另一元素中的何处。             |
| cursor           | 设置显示的指针类型                                           |
| direction        | 设置元素的文本方向                                           |
| display          | 设置元素如何被显示                                           |
| height           | 设置元素的高度                                               |
| markerOffset     | 设置marker box的principal box距离其最近的边框边缘的距离      |
| marks            | 设置是否cross marks或crop marks应仅仅被呈现于page box边缘之外 |
| maxHeight        | 设置元素的最大高度                                           |
| maxWidth         | 设置元素的最大宽度                                           |
| minHeight        | 设置元素的最小高度                                           |
| minWidth         | 设置元素的最小宽度                                           |
| overflow         | 规定如何处理不适合元素盒的内容                               |
| verticalAlign    | 设置对元素中的内容进行垂直排列                               |
| visibility       | 设置元素是否可见                                             |
| width            | 设置元素的宽度                                               |

###### List 属性

| 属性              | 描述                     |
| ----------------- | ------------------------ |
| listStyle         | 在一行设置列表的所有属性 |
| listStyleImage    | 把图像设置为列表项标记   |
| listStylePosition | 改变列表项标记的位置     |
| listStyleType     | 设置列表项标记的类型     |

###### Positioning 属性

| 属性     | 描述                                                   |
| -------- | ------------------------------------------------------ |
| bottom   | 设置元素的底边缘距离父元素底边缘的之上或之下的距离     |
| left     | 置元素的左边缘距离父元素左边缘的左边或右边的距离       |
| position | 把元素放置在static, relative, absolute 或 fixed 的位置 |
| right    | 置元素的右边缘距离父元素右边缘的左边或右边的距离       |
| top      | 设置元素的顶边缘距离父元素顶边缘的之上或之下的距离     |
| zIndex   | 设置元素的堆叠次序                                     |

###### Printing 属性

| 属性            | 描述                               |
| --------------- | ---------------------------------- |
| orphans         | 设置段落留到页面底部的最小行数     |
| page            | 设置显示某元素时使用的页面类型     |
| pageBreakAfter  | 设置某元素之后的分页行为           |
| pageBreakBefore | 设置某元素之前的分页行为           |
| pageBreakInside | 设置某元素内部的分页行为           |
| size            | 设置页面的方向和尺寸               |
| widows          | 设置段落必须留到页面顶部的最小行数 |

###### Scrollbar 属性 (IE-only)

| 属性                     | 描述                                               |
| ------------------------ | -------------------------------------------------- |
| scrollbar3dLightColor    | 设置箭头和滚动条左侧和顶边的颜色                   |
| scrollbarArrowColor      | 设置滚动条上的箭头颜色                             |
| scrollbarBaseColor       | 设置滚动条的底色                                   |
| scrollbarDarkShadowColor | 设置箭头和滚动条右侧和底边的颜色                   |
| scrollbarFaceColor       | 设置滚动条的表色                                   |
| scrollbarHighlightColor  | 设置箭头和滚动条左侧和顶边的颜色，以及滚动条的背景 |
| scrollbarShadowColor     | 设置箭头和滚动条右侧和底边的颜色                   |
| scrollbarTrackColor      | 设置滚动条的背景色                                 |

###### Table 属性

| 属性           | 描述                                                         |
| -------------- | ------------------------------------------------------------ |
| borderCollapse | 设置表格边框是否合并为单边框，或者像在标准的HTML中那样分离。 |
| borderSpacing  | 设置分隔单元格边框的距离                                     |
| captionSide    | 设置表格标题的位置                                           |
| emptyCells     | 设置是否显示表格中的空单元格                                 |
| tableLayout    | 设置用来显示表格单元格、行以及列的算法                       |

###### Text 属性

| 属性           | 描述                             |
| -------------- | -------------------------------- |
| color          | 设置文本的颜色                   |
| font           | 在一行设置所有的字体属性         |
| fontFamily     | 设置元素的字体系列。             |
| fontSize       | 设置元素的字体大小。             |
| fontSizeAdjust | 设置/调整文本的尺寸              |
| fontStretch    | 设置如何紧缩或伸展字体           |
| fontStyle      | 设置元素的字体样式               |
| fontVariant    | 用小型大写字母字体来显示文本     |
| fontWeight     | 设置字体的粗细                   |
| letterSpacing  | 设置字符间距                     |
| lineHeight     | 设置行间距                       |
| quotes         | 设置在文本中使用哪种引号         |
| textAlign      | 排列文本                         |
| textDecoration | 设置文本的修饰                   |
| textIndent     | 缩紧首行的文本                   |
| textShadow     | 设置文本的阴影效果               |
| textTransform  | 对文本设置大写效果               |
| unicodeBidi    |                                  |
| whiteSpace     | 设置如何设置文本中的折行和空白符 |
| wordSpacing    | 设置文本中的词间距               |





### Table对象

###### Table 对象集合

| 集合     | 描述                                                         |
| -------- | ------------------------------------------------------------ |
| cells    | 回包含表格中所有单元格的一个数组。                           |
| **rows** | 返回包含表格中所有行的一个数组。<br />可通过length获取到当前表格的数量 |
| tBodies  | 返回包含表格中所有 tbody 的一个数组。                        |



###### Table 对象方法

| 方法            | 描述                                |
| --------------- | ----------------------------------- |
| createCaption() | 为表格创建一个 caption 元素。       |
| createTFoot()   | 在表格中创建一个空的 tFoot 元素。   |
| createTHead()   | 在表格中创建一个空的 tHead 元素。   |
| deleteCaption() | 从表格删除 caption 元素以及其内容。 |
| **deleteRow()** | 从表格删除一行。                    |
| deleteTFoot()   | 从表格删除 tFoot 元素及其内容。     |
| deleteTHead()   | 从表格删除 tHead 元素及其内容。     |
| **insertRow()** | 在表格中插入一个新行。              |





### TableRow对象

###### TableRow 对象集合

| 集合    | 描述                               |
| ------- | ---------------------------------- |
| cells[] | 返回包含行中所有单元格的一个数组。 |

###### TableRow 对象方法

| 方法         | 描述                                       |
| ------------ | ------------------------------------------ |
| deleteCell() | 删除行中的指定的单元格。                   |
| insertCell() | 在一行中的指定位置插入一个空的 <td> 元素。 |





