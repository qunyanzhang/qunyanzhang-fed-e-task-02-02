# qunyanzhang-fed-e-task-02-02

## 简答题

### 1.webpack的构建流程环节：
webpack根据项目配置找到其中一个文件作为打包的入口，根据入口文件中import和require解析推断出文件所依赖的资源模块，然后分别去解析每个资源模块所对应的依赖，这样就形成了整个项目中所有用到文件间的依赖关系的依赖树，然后webpack会递归这个依赖树找到每个节点所对应的资源文件，再根据配置文件的rules属性找到这个模块所对应的加载器，然后交给这个加载器去加载这个模块，最后将加载后的结果打包到bundle.js文件中，从而实现我们整个项目的打包

### 2.
loader: 专注各种各样资源文件的加载，实现整体项目的打包
plugin: 增强webpack自动化能力，如清除dist目录、拷贝静态文件到输出目录、压缩打包结果输出的代码

## 编程题

实现了项目的样式、HTML、图片文件的打包，及浏览器页面访问的功能