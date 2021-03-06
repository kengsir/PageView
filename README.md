## PageView
  - An easy way to use Tabbar NavigationBar
  - 切换有颜色渐变效果
  
## How to use PageView
  - copy file to your project file
  
  <img src="https://github.com/coderLL/PageView/blob/master/step.png" width=200 height=130 />
  - create PageTitleView
  
    ```swift
       let titles = ["推荐", "游戏", "娱乐", "体育"]
       let titleView = PageTitleView(frame: titleFrame, titles: titles)
    ```
  - implement pageTitleViewDelegate method in viewController
  
    ```swift
       func pageTitltView(titleView: PageTitleView, selectedIndex index: Int)
    ```
  - create PageContentView
  
    ```swift
       var childVcs = [UIViewController]()
       for _ in 0..<4 {
           let vc = UIViewController()
           childVcs.append(vc) // 添加子控制器
       }
       let pageContentView = PageContentView(frame: contentFrame, childVcs: childVcs, parentViewController: self)
    ```
  - implement pageContentDelegate method in viewController
  
    ```swift
       func pageContentView(contentView: PageContentView, progress: CGFloat, sourceIndex: Int, targetIndex: Int)
    ```
  
## Preview
  <img src="https://github.com/coderLL/PageView/blob/master/Run.gif" width=320 height=568 />
  
## 后期完善
  - 1. 颜色自定义
  - 2. 多个pageTitleView多个Item滑动
  - 3. ......
