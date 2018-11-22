# MFC
用MFC开发一个数字图像处理器
  
**相关概念**  
菜单：下拉式菜单（通常由主菜单栏，子菜单及子菜单中的菜单项和分隔条所组成的）  
      弹出式菜单（一般可以通过单击鼠标右键等操作显示，它的主菜单不可见，只显示子菜单）  
ps:若要选择有menu的，新建项目时选择生成单文档，而不是基于对话框  
热键定义：caption中的中文名（&热键大写）  
更改完caption与id后，还要去Accelerator中添加热键操作  
  
CMenu类除了加载菜单资源函数BOOL LoadMenu(UINT nIDResource)与删除菜单项BOOL DeleteMenu(UINT nPosition,UINT nFlags)外，还有在指定位置显示一个浮动的弹出式菜单 BOOL TrackPopupMenu(UINT nFlags,int x,int y,CWnd* pWnd,LPCRECT lpRect = 0) 参数nFlags指定屏幕坐标和鼠标位置的标志  
  
菜单消息：COMMAND消息和UPDATE_COMMAND_UI消息   
COMMAND消息：在菜单项被点击时发送该消息。  
UPDATE_COMMAND_UI消息：用来维护菜单项的各项状态，包括激活、禁用、变灰、选中、未选中等。在下拉菜单每次打开的时候，所有菜单项的此消息都会被发送出去。如果所属类中为菜单项的该消息添加了处理函数，则执行相应函数更新菜单状态，如果菜单项没有此消息处理函数，也没有COMMAND消息的处理函数，那么它就会变灰。  
  
  



