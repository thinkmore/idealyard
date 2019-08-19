
# 前端

借助[此处](https://github.com/shimh-develop/blog-vue-springboot)写好的`Vue`页面。
[预览地址](http://shiminghui.top:8000/)

# 后端
## BUGs:
- [x] 首页摘要信息获取错误
- [x] 概览页（index）显示
- [x] 更新文章，对原有标签删除时，不成功，但新加正常
- [x] 首页点击查看全部进入空白页
- [x] 编辑文章时已经存在的标签会二次添加（查询中间表可以看到写了两次！！！）  
    ~~1. 新建标签失败~~  
    ~~2. 标题无法修改（目前有该入口，正常来说应该是可以更新的<除非代码没有这块逻辑，如果没有，则不添加，文章新建之后就不要改变链接了>）~~
- [x] 新建文章报错
- [x] 首页无限滚动时：Duplicate keys detected: 'xxxx'. This may cause an update error.
- [ ] 点击页内锚点，跳转到文章分类页面，应该在本页面内跳转

~~- [] 访问已删除文章时，不会跳转到首页！~~
    目前可以跳转，但是由于abort函数，导致会有报错闪现。
- [ ] token超时时弹出很多message,应该使用更友好的方式！！！或者精准提示，一次只提示一条即可
- [ ] 数据库迁移报错
    ```bash
    werkzeug.utils.ImportStringError: import_string() failed for 'mains.bp'. Possible reasons are:
    
    - missing __init__.py in a package;
    - package or module path not included in sys.path;
    - duplicated package or module name taking precedence in sys.path;
    - missing module, class, function or variable;
    
    Debugged import:
    
    - 'mains' not found.
    
    Original exception:
    
    ModuleNotFoundError: No module named 'mains'
    ```

## TODO:

- [x] 文章阅读计数
- [x] 添加获取用户信息API
- [x] 博客自己修改  
  view页面需要summary,因为在编辑时，摘要不能消失  
  编辑时需要对新的和旧的标签对比，正常不走add逻辑  
  编辑时应该是post请求，将用户提交的全量更新，没有的置空
- [x] 博客作者自己删除
- [x] slug选项在更新文章时应该是不可见的（url确定之后不可修改！）
- [x] 链接由id变成数字和slug的组合
- [x] 标签云
~~参考[这里](https://github.com/MikeCoder/hexo-tag-cloud)~~
~~参考[这里](https://juejin.im/post/5c99a0f7e51d454e9b3c3343)~~
~~参考[这里](https://github.com/nobalmohan/vue-tag-cloud)~~
- [x] 本次/上次提交中header样式需要调整
- [ ] 使aside侧边栏固定，不会随鼠标滚动消失
- [ ] 标签、分类页面，item数量为0时，点击事件 disable
- [ ] 标签管理员手动添加
- [ ] 分类管理员手动添加
---
优先级中等
- [ ] 管理员账户
- [ ] i18n（en&zh）

---
优先级低

- [ ] 移动端自适应，之后再做