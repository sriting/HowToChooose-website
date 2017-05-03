# HowToChooose 开放性投票社交网站
**HowToChooose -- a Open Voting Social Website**  

一个可以快速发起投票问题、有多种轻量型投票模式、投票过程公开且可对投票问题进行评论的开放性社区/社交网站。
A social online community/website that support quickly posting voting questions, multiple lightweight types of voting, open process and result of voting and making comments for questions. 

---
[TOC]
## 灵感和网站的目的

HowToChooose的灵感来自于我经常能在微信朋友圈看到同学、朋友甚至很多长辈发的简单的投票文字，询问大家对选择某件事、某物品的建议，通过对评论的手动计数来得到结果。这种消息在朋友圈经常能出现，而且大家的问题普遍是短时效、轻量化、依赖社交、非正式化的单一问题，而这是目前大多数问卷、投票网站不能满足的，比如问卷星、monkeySurvey等，制作问卷的过程复杂、问卷形式太正式而提问者只想对一个问题发起投票、投票过程和结果不公开即不能满足提问者的社交化投票的需求。
*The inspiration of HowToChooose came from the Moment of WeChat. Many young people get confused on choosing something and then post one question with several pictures in Moment to ask friends about suggestions. These questions generally have some features that posting quickly and simply, requiring short-time voting result and counting result manually ,and questions are unformal and social. However, most exisited websites like monkeySurvey cannot satisfy these requirements. Because these surveys are too formal, posting processes are too complex while users only want to start a vote on one question and the result is not open to public, let alone share to friends.* 

HowToChooose 网站正如名字一样，Chooose中多的一个o象征着年轻人普遍被越来越多的选择所困扰，所以网站目的是为了帮助使用者们尤其是年轻人快速轻松解决“不懂怎么选择”、选择恐惧症等“现代病”。通过简便的图文制作并发起单个问题的投票，分享投票页面到各个社交问题，实时查看公开的投票数据，评论中别人给出更详细的建议，HowToChooose 可以满足广大年轻人日常生活中频率较高的征求好友及网友意见、晒照片、晒投票结果等的社交需求。另外，HowToChooose 本身也是个开放的社区，用户可以互相关注、收藏问题、展示或隐藏自己的动态，分享自己喜爱的别人的问题， HowToChooose 希望提供给大家一个更贴近日常生活的轻松的投票环境。

##网站技术

这是一个小组作业的作品，网站的开发部分主要由两个人负责。我 [sriting][1] - 前端页面设计开发；陈军 [garvinchen][2] 负责后端数据库开发。组里其他有调查、设计、测试、报告工作的组员有：刘一宁、王烯、付艾宁、陈珂瑾、陈鑫圆。
*It's a group project that website is completed by two authors. I, [sriting][3] , am responsible for front-end design and programming, and Chen Jun, [garvinchen][4] , is in charge of back-end database. Other teammates that work on survey, design, testing and report are Liu Yining, Wang Xi, Fu Aining, Chen Kejin, Chen Xinyuan.* 

前端部分使用（front-end）：html5, css3, javaScript, jQuery, Bootstrap
后端部分使用（back-end）：python, Django, MySQL
网站使用过的开源库会在后续的网站各部分功能的说明中申明。
*We will declare references of open sources and libraries we used in each function description in the following.*

#HowToChooose网站功能

##用户注册、登录
###1. 功能
- [x] 新用户注册有验证码，以防恶意大量注册 --> [预览register.html][5]
      New users need to fill in verification code before register to avoid malicious registration. --> [View register.html][6]
- [x] 新用户填写注册表单后，发邮件给注册邮箱进行验证，用以绑定邮箱 --> [预览verification.html][7]
      After submit register form, system will send email to users to varify the email address.  --> [View verification.html][8]
- [x] 已注册用户可登录 --> [预览login.html][9]
      Registered users can sign in. --> [View login.html][10]
- [x] 已注册用户忘记密码可发验证请求给绑定邮箱 --> [预览forgetpw.html][11]
      Users who forgat passward can send the verification email to their email address. --> [View forgetpw.html][12]
- [x] 邮箱收到重设密码邮件，打开邮件中链接重新设置密码 --> [预览resetpw.html][13]
      Users can open the link in verification email and reset their password. --> [View resetpw.html][14]
- [ ] 非注册用户可通过各社交平台账号不注册直接登录（需备案域名申请，未实现，预留了按键） --> [预览login.html][15]
      Unregistered users can login website by social accounts directly. (need to put on record, unimplement, we reserve the buttons for socail accounts)  --> [View login.html][16]
- [x] 所有页面实现自适应（响应式网页），符合大部分主流笔记本、手机等设备的尺寸。展示如下：
      All pages are self-adaption so that they can match most types of screen and display differently. See: 
![rigester-iphone6][17] 
这是iphone6尺寸的register页面，验证码输入框旁边的空位是给后端放验证码图片的预留位。
It is the register page in iPhone6 screen size. The empty space after verificate box is to reserve for verification images from the back-end.
![rigester-laptop][18]
这是正常笔记本浏览器显示的样子。 Website layout in laptop's browsers.
###2. 使用技术
> * 好看的渐变色背景的代码来自于 [uigradients][19] 这个网站
    The gradient background's code is from the [uigradients][19] website.
> * 后端的验证码图片、验证方法使用了库
    The verification codes and images in back-end is from the library.


  [1]: https://github.com/sriting
  [2]: https://github.com/junchen14
  [3]: https://github.com/sriting
  [4]: https://github.com/junchen14
  [5]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/register.html
  [6]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/register.html
  [7]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/verification.html
  [8]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/verification.html
  [9]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/login.html
  [10]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/login.html
  [11]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/forgetpw.html
  [12]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/forgetpw.html
  [13]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/resetpw.html
  [14]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/resetpw.html
  [15]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/login.html
  [16]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/login.html
  [17]: https://sriting.github.io/HowToChooose-website/register-iphone6.png
  [18]: https://sriting.github.io/HowToChooose-website/register-laptop.png
  [19]: https://uigradients.com