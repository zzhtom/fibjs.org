# 模块 path
文件路径处理模块

引用方法：
@code
var path = require(&#39;path&#39;);
@endcode
## 函数
        
### normalize
标准化路径，处理路径中父目录等信息
```JavaScript
String path.normalize(String path);
```

** 调用参数: **
* path - 给定的未处理的路径

** 返回结果:**
* 返回经过处理的路径

### basename
查询路径中的文件名称，若指定扩展名，则自动取消匹配的扩展名
```JavaScript
String path.basename(String path,
                String ext = "");
```

** 调用参数: **
* path - 给定查询的路径
* ext - 指定扩展名，若文件名中有符合条件的扩展名，将自动取消

** 返回结果:**
* 返回文件名称

### extname
查询路径中的文件扩展名
```JavaScript
String path.extname(String path);
```

** 调用参数: **
* path - 给定查询的路径

** 返回结果:**
* 返回得到的扩展名

### dirname
查询路径中的目录路径
```JavaScript
String path.dirname(String path);
```

** 调用参数: **
* path - 给定查询的路径

** 返回结果:**
* 返回得到的目录的路径

### fullpath
转换给定路径为全路径
```JavaScript
String path.fullpath(String path);
```

** 调用参数: **
* path - 给定转换的路径

** 返回结果:**
* 返回转换的全路径

### isAbsolute
识别给定的路径是否是绝对路径
```JavaScript
Boolean path.isAbsolute(String path);
```

** 调用参数: **
* path - 给定需要识别的路径

** 返回结果:**
* 是绝对路径则返回 true

### join
合并一系列路径成为一个单一路径
```JavaScript
String path.join(...);
```

** 调用参数: **
* ... - 一个或多个相关的路径

** 返回结果:**
* 返回得到的新路径

### resolve
合并一系列路径成为一个绝对路径
```JavaScript
String path.resolve(...);
```

** 调用参数: **
* ... - 一个或多个相关的路径

** 返回结果:**
* 返回得到的新路径

## 属性
        
### sep
查询当前操作系统的路径分割字符，posix 返回 &#39;/&#39;, windows 返回  &#39;\\&#39;
```JavaScript
readonly String path.sep;
```

### delimiter
查询当前操作系统的多路径组合字符，posix 返回 &#39;:&#39;, windows 返回  &#39;;&#39;
```JavaScript
readonly String path.delimiter;
```

### posix
posix 实现，参见 path_posix
```JavaScript
readonly Object path.posix;
```

### win32
windows 实现，参见 path_win32
```JavaScript
readonly Object path.win32;
```
