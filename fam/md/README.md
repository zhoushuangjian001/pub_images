![icon](https://github.com/zhoushuangjian001/fam/blob/master/image/icon.png?raw=true)

语言:  [🇺🇸 English](https://pub.dev/packages/fam) | [🇨🇳 Chinese](https://github.com/zhoushuangjian001/fam/blob/master/README_CH.md)

- **Fam 基本简介**    
  
  Fam 是专为 Flutter 项目资产管理设计的脚本服务。该服务具有功能齐全、操作方便、支持多种平台、界面优美、可自定义化强等特点。

- **Fam 使用配置**

  Fam 是托管在 pub.dev  上，你可运行下面指令进行配置，指令如下：
  ```dart
  flutter pub global activate fam
  ```
  如果你从未配置过  .pub-cache 路径， 则上面指令执行完毕后会输出其配置提示，如下所示:    

  **macOS 用户:**
  ![fam - help](https://github.com/zhoushuangjian001/fam/blob/master/image/pub-catch.png?raw=true)
  按照上面提示配置即可。


- **Fam 指令**
  1. **`fam` or `fam --help` or `fam -h`**       
   该指令能够快速查看 Fam 所提供的一级指令和介绍，该指令运行输出如下所示: ![fam - help](https://github.com/zhoushuangjian001/fam/blob/master/image/fam-help.png?raw=true)
    
  2. **`fam init`**
   项目资产文件管理的 Fam 脚本服务初始化配置。在终端中运行该指令，会让你输入资产管理的文件名和类名，如下所示:    ![fam-init](https://github.com/zhoushuangjian001/fam/blob/master/image/fam-init.png?raw=true)      
  注意：      
      1.文件的名字是有小写字母组成，例如: **fam** ；后面会生成 **fam.dart** 文件。      
      2.文件的类名是有字母组成，首字母必须大写，例如 **Fam** ; 后面会生成类名 **abstract class Fam {}**.
            
  3. **`fam run`**   
   执行项目资产管理Fam的服务，执行成功后，就可以使用类名快速访问资产文件。该使用类名获取资源如下:  ![fam-run](https://github.com/zhoushuangjian001/fam/blob/master/image/fam-run.png?raw=true)  

  4. **`fam filter -h`**   
   进行过滤项目资产文件指令帮助信息，该指令运行输出如下:    ![fam-filter](https://github.com/zhoushuangjian001/fam/blob/master/image/fam-filter.png?raw=true)  
   从上图看出 `filter` 有两个子的指令，分别是: `size` 和 `unused` 。 `size` 是过滤资产文件大小的；`unused` 是过滤资产文件未使用的。

     1. **`fam filter size`**
      过滤项目资产文件中是否有超过指定大小的文件，默认大小为 200KB。如果有将按一下形式输出:    ![fam-filter-size](https://github.com/zhoushuangjian001/fam/blob/master/image/fam-filter-size.png?raw=true) 
      你也可以自定义查找大小的单位,例如: 
         ```shell
         fam filter size -b 200  // 200 b 
         fam filter size -k 200  // 200 kb 
         fam filter size -m 200  // 200 mb 
         fam filter size -g 200  // 200 gb 
         ```
     2. **`fam filter unused`**
       过滤项目资产文件中是否有在项目中未使用的文件。如果有则按一下形式输出，并不删除未使用文件。如下所示:    
       ![fam-filter-unused](https://github.com/zhoushuangjian001/fam/blob/master/image/fam-filter-unused.png?raw=true) 
       如果你想过滤后直接删除则可使用 `fam filter unused delete` 即可。    
  5. **`fam fix`**
   对已经被 Fam 管理后的项目出现问题进行修复。比如: **fam.dart** 文件被误删除；**.fam** 文件被删除。
  6. **`fam rename`**
   对项目资产管理的文件进行重命名或者对资产管理类进行重命名。有 `fam rename file xx` 和 `fam rename class xx`  两个指令。
  7. **`fam delete`** 
   删除项目的资源文件。有 `fam delete file xx` 和 `fam delete mfile xx` 两个指令。 `delete file` 是删除单个资源文件; `delete mfile`  是删除多个资源文件。

- **Fam 优势**
  **Fam** 和其他插件对比，有以下优点。
  1. **Fam** 是依托于 **pub.dev**  进行管理。
  2. **Fam** 支持多种平台。
  3. **Fam** 不区分项目开发工具，只要有终端即可。
  4. **Fam** 提供一些常用资源管理的功能。
  5. **Fam** 的资产引用时文件名字简短，能够完全被提示出来。
  6. **Fam** 对项目资产进行类目划分清晰。