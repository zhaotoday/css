### 详细的 Tailwind CSS 和 UnoCSS 样式类名排序指南

在使用 Tailwind CSS 和 UnoCSS 时，虽然框架本身没有强制的类名排序规范，但遵循一定的排序规则可以使代码更清晰、易于维护。以下是更详细的类名排序建议，按照不同类型的样式进行划分，并提供具体的示例。

#### 1. **布局类名 (Layout Classes)**
   布局类名定义了元素的基本结构、排列和布局属性。优先放置这些类名，以明确元素的布局和定位。

   - **容器与显示类型**: `container`, `block`, `inline-block`, `flex`, `grid`
   - **定位**: `relative`, `absolute`, `fixed`, `sticky`
   - **显示与可见性**: `hidden`, `block`, `inline`, `visible`, `invisible`
   - **浮动与清除**: `float-left`, `float-right`, `clear-both`
   - **Flexbox/Grid**: `flex`, `inline-flex`, `grid`, `inline-grid`
   - **对齐与分布**: `justify-center`, `items-center`, `justify-between`, `gap-4`
   - **列与顺序**: `flex-col`, `flex-row`, `order-1`, `col-span-2`

   **示例:**
   ```html
   <div class="container flex justify-center items-center relative">
   ```

#### 2. **尺寸与间距类名 (Size & Spacing Classes)**
   这些类名控制元素的尺寸、内边距和外边距，通常放在布局类名之后。

   - **宽度与高度**: `w-full`, `w-1/2`, `h-64`, `min-w-0`, `max-h-full`
   - **间距**: `m-4`, `mx-auto`, `p-2`, `pt-4`, `pb-8`, `space-x-4`, `space-y-2`
   - **边框尺寸**: `border`, `border-2`, `border-t`, `border-b-4`

   **示例:**
   ```html
   <div class="w-1/2 h-64 p-4 m-2">
   ```

#### 3. **排版类名 (Typography Classes)**
   排版类名定义文本的外观，包括字体、大小、行高等。排版类名通常在布局和尺寸类名之后。

   - **字体**: `font-sans`, `font-serif`, `font-mono`, `text-lg`, `text-xl`
   - **字体粗细**: `font-light`, `font-normal`, `font-bold`, `font-black`
   - **行高**: `leading-none`, `leading-tight`, `leading-relaxed`
   - **字间距**: `tracking-tight`, `tracking-wide`
   - **文本对齐**: `text-left`, `text-center`, `text-right`
   - **文本修饰**: `underline`, `line-through`, `no-underline`
   - **文本变换**: `uppercase`, `lowercase`, `capitalize`
   - **文本溢出**: `truncate`, `overflow-ellipsis`, `overflow-hidden`

   **示例:**
   ```html
   <p class="text-xl font-bold leading-tight text-center">
   ```

#### 4. **颜色与背景类名 (Color & Background Classes)**
   颜色和背景类名通常紧随排版类名之后，定义元素的文本颜色、背景颜色、边框颜色等。

   - **文本颜色**: `text-gray-800`, `text-red-500`, `text-blue-700`
   - **背景颜色**: `bg-white`, `bg-blue-100`, `bg-gradient-to-r`, `bg-opacity-50`
   - **边框颜色**: `border-gray-300`, `border-red-500`, `border-blue-700`
   - **颜色状态**: `hover:text-blue-600`, `focus:bg-gray-200`

   **示例:**
   ```html
   <button class="text-white bg-blue-500 hover:bg-blue-600">
   ```

#### 5. **边框与圆角类名 (Border & Radius Classes)**
   边框和圆角类名通常位于颜色类名之后，用于定义元素的边框样式和圆角。

   - **边框样式**: `border`, `border-dashed`, `border-solid`
   - **边框圆角**: `rounded`, `rounded-lg`, `rounded-full`
   - **分割线**: `divide-y`, `divide-x`, `divide-gray-200`

   **示例:**
   ```html
   <div class="border border-gray-300 rounded-lg">
   ```

#### 6. **效果与阴影类名 (Effect & Shadow Classes)**
   这些类名定义元素的视觉效果，如阴影、透明度、滤镜等，通常放在前面的基础类名之后。

   - **阴影**: `shadow`, `shadow-md`, `shadow-lg`, `shadow-inner`
   - **透明度**: `opacity-50`, `opacity-75`
   - **滤镜**: `filter`, `blur`, `brightness-110`, `contrast-125`
   - **背景混合**: `bg-blend-multiply`, `bg-blend-overlay`

   **示例:**
   ```html
   <div class="shadow-lg opacity-75">
   ```

#### 7. **动画与状态类名 (Animation & State Classes)**
   动画和状态类名定义元素的动态效果，如悬停、焦点、过渡等，通常放在所有基础样式类名的末尾。

   - **过渡**: `transition`, `transition-all`, `duration-300`
   - **变换**: `transform`, `scale-110`, `rotate-45`
   - **状态**: `hover:bg-blue-500`, `focus:outline-none`, `active:scale-95`
   - **动画**: `animate-bounce`, `animate-spin`, `motion-reduce:transform-none`

   **示例:**
   ```html
   <button class="transition-transform duration-300 hover:scale-105">
   ```

### **最终示例：**
将上述规范应用于一个完整的类名序列，例子如下：

```html
<div class="container flex justify-center items-center w-full h-64 p-4 text-lg font-bold text-white bg-blue-500 border border-gray-300 rounded-lg shadow-lg transition-transform duration-300 hover:scale-105">
   Example Content
</div>
```

### **注意事项：**
- **一致性**: 确保在整个项目中保持一致的类名顺序，有助于提高代码的可读性。
- **团队规范**: 如果是团队协作，建议制定并遵循一致的类名排序规范，以减少沟通成本。
- **灵活性**: 根据实际需求和个人或团队的习惯，可以调整顺序，但应避免混乱。

通过遵循这些详细的顺序建议，您可以编写出更具结构性和可维护性的样式代码。
