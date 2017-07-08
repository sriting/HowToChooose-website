<h1 id="1"> HowToChooose 开放性投票社交网站 </h1>

**HowToChooose -- a Open Voting Social Website**  

一个可以快速发起投票问题、有多种轻量型投票模式、投票过程公开且可对投票问题进行评论的开放性社区/社交网站。

A social online community/website that support quickly posting voting questions, multiple lightweight types of voting, open process and result of voting and making comments for questions. 

---

* [HowToChooose 开放性投票社交网站](#1)  
	* [灵感和网站的目的 Inspiration and the goal](#1.1)  
	* [网站技术 Technologies](#1.2)  
* [HowToChooose网站功能 Functions of HowToChooose](#2)  
	* [用户注册、登录 User register and login](#2.1)  
		* [1. 功能 Functions](#2.1.1)  
		* [2. 使用技术 Techniques](#2.1.2)  
	* [主页面（热门问题页）、子页面（问题细节页）Main page and subpage](#2.2)
		* [1. 功能 Functions](#2.2.1)
		* [2. 使用技术 Techniques](#2.2.2)
	* [搜索结果页、用户中心页、个人信息页  Search result page, user center page and personal information page](#2.3)
		* [1. 功能 Functions](#2.3.1)
		* [2. 使用技术 Techniques](#2.3.2)



<h2 id="1.1"> 灵感和网站的目的  Inspiration and the goal</h2>

HowToChooose的灵感来自于我经常能在微信朋友圈看到同学、朋友甚至很多长辈发的简单的投票文字，询问大家对选择某件事、某物品的建议，通过对评论的手动计数来得到结果。这种消息在朋友圈经常能出现，而且大家的问题普遍是短时效、轻量化、依赖社交、非正式化的单一问题，而这是目前大多数问卷、投票网站不能满足的，比如问卷星、monkeySurvey等，制作问卷的过程复杂、问卷形式太正式而提问者只想对一个问题发起投票、投票过程和结果不公开即不能满足提问者的社交化投票的需求。

*The inspiration of HowToChooose came from the Moment of WeChat. Many young people get confused on choosing something and then post one question with several pictures in Moment to ask friends about suggestions. These questions generally have some features that posting quickly and simply, requiring short-time voting result and counting result manually ,and questions are unformal and social. However, most exisited websites like monkeySurvey cannot satisfy these requirements. Because these surveys are too formal, posting processes are too complex while users only want to start a vote on one question and the result is not open to public, let alone share to friends.* 

HowToChooose 网站正如名字一样，Chooose中多的一个o象征着年轻人普遍被越来越多的选择所困扰，所以网站目的是为了帮助使用者们尤其是年轻人快速轻松解决“不懂怎么选择”、选择恐惧症等“现代病”。通过简便的图文制作并发起单个问题的投票，分享投票页面到各个社交问题，实时查看公开的投票数据，评论中别人给出更详细的建议，HowToChooose 可以满足广大年轻人日常生活中频率较高的征求好友及网友意见、晒照片、晒投票结果等的社交需求。另外，HowToChooose 本身也是个开放的社区，用户可以互相关注、收藏问题、展示或隐藏自己的动态，分享自己喜爱的别人的问题， HowToChooose 希望提供给大家一个更贴近日常生活的轻松的投票环境。

<h2 id="1.2"> 网站技术  Technologies</h2>

这是一个小组作业的作品，网站的开发部分主要由两个人负责。我 [sriting][1] - 前端页面设计开发；陈军 [garvinchen][2] 负责后端数据库开发。组里其他有调查、设计、测试、报告工作的组员有：刘一宁、王烯、付艾宁、陈珂瑾、陈鑫圆。  
*It's a group project that website is completed by two authors. I, [sriting][1] , am responsible for front-end design and programming, and Chen Jun, [garvinchen][2] , is in charge of back-end database. Other teammates that work on survey, design, testing and report are Liu Yining, Wang Xi, Fu Aining, Chen Kejin, Chen Xinyuan.* 

前端部分使用（front-end）： `html5`, `css3`, `javaScript`, `jQuery`, `Bootstrap`

后端部分使用（back-end）：`python`, `Django`, `MySQL`

网站使用过的开源库会在后续的网站各部分功能的说明中申明。

*We will declare references of open sources and libraries we used in each function description in the following.*

<h1 id="2"> HowToChooose网站功能  Functions of HowToChooose</h1>

<h2 id="2.1"> 用户注册、登录  User register and login</h2>

<h3 id="2.1.1"> 1. 功能  Functions</h3>

- [x] 新用户注册有验证码，以防恶意大量注册 --> [预览register.html][3]  

*New users need to fill in verification code before register to avoid malicious registration. --> [View register.html][3]*

- [x] 新用户填写注册表单后，发邮件给注册邮箱进行验证，用以绑定邮箱 --> [预览verification.html][4]  

*After submit register form, system will send email to users to varify the email address.  --> [View verification.html][4]*

- [x] 已注册用户可登录 --> [预览login.html][5]  

*Registered users can sign in. --> [View login.html][5]*

- [x] 已注册用户忘记密码可发验证请求给绑定邮箱 --> [预览forgetpw.html][6]  

*Users who forgat passward can send the verification email to their email address. --> [View forgetpw.html][6]*

- [x] 邮箱收到重设密码邮件，打开邮件中链接重新设置密码 --> [预览resetpw.html][7]  

*Users can open the link in verification email and reset their password. --> [View resetpw.html][7]*

- [ ] 非注册用户可通过各社交平台账号不注册直接登录（需备案域名申请，未实现，预留了按键） --> [预览login.html][8]  

*Unregistered users can login website by social accounts directly. (need to put on record, unimplement, we reserve the buttons for socail accounts)  --> [View login.html][8]*

- [x] 所有页面实现自适应（响应式网页），符合大部分主流笔记本、手机等设备的尺寸。展示如下：  

*All pages are self-adaption so that they can match most types of screen and display differently. See:*

![rigester-iphone6][9] 

这是iphone6尺寸的register页面，验证码输入框旁边的空位是给后端放验证码图片的预留位。  
It is the register page in iPhone6 screen size. The empty space after verificate box is to reserve for verification images from the back-end.

![rigester-laptop][10]

这是正常笔记本浏览器显示的样子。 This is the website layout in laptop's browsers.

<h3 id="2.1.2"> 2. 使用技术  Techniques</h3>

> * 好看的渐变色背景的代码来自于 [uigradients][11] 这个网站  
*The gradient background's code is from the [uigradients][11] website.*
> * 后端的验证码图片、验证方法使用了 [django-captcha][12] 库  
*The verification codes and images in back-end is from the [django-captcha][12] library.*

<h2 id="2.2"> 主页面（热门问题页）、子页面（问题细节页） Main page and subpage</h2>

<h3 id="2.2.1"> 1. 功能  Functions</h3>

#### 主页面（热门问题页） Main page (Hot topic page)  --> [mainpage.html][16] 

#### 子页面（问题细节页） Subpage（comment page)  --> [commentPage.html(赞踩页 Up or Down)][18] , [commentPage2.html(多选页 Multiple choice)][19] 


- [x] 可对感兴趣的问题进行**赞/踩**投票，投票结果立即以 百分比条 动态显示，且投完票后不可更改选项。 效果如下：

*Users can vote **Up/Down** in the questions that they are instersted in, and the result is directly displayed in percentage bar and cannot be changed. See:*

![mainpage-upDown][13]

- [x] 可对感兴趣的问题进行**多选项**投票（2至4选项），投票结果立即以 饼图 动态显示，且投完票后不可更改选项。 效果如下：

*Users can vote **Multiple Choices** in the questions that they are instersted in, and the result is directly displayed in percentage bar and cannot be changed. See:*

![mainpage-Multiple][14]

- [x] （主页面）可展开/折叠某一问题的文字描述或评论，主页面打开时默认将所有过长文字收缩展示以限制单个问题的展示长度，评论也只展示一条，便于用户浏览更多的问题。子页面的问题描述不会被折叠，且所有关于该问题的评论都会被展示。 效果如下：

*Users can expand or collapse the description or comments of one question in main page. When open main page, all questions that have too long text description will be collapsed by default and only one comment will be showed so that users can browse more questions handily. In subpage of questions, the description will not be collapsed and all comments of these question are displayed. See:*

![mainpage-Collapse+image][15]

- [x] 所有用于描述问题的图片，都可以点击放大查看，切换前后图片，再点击缩小回到页面，便于用户更好查看图片。 效果如上面的动图。

*All pictures of question can be zoomed in and zoomed out so that users can look throught images more conveniently. See the GIF above.*


- [x] 当用户浏览到页面的较后内容时，可按右下角按键一键回到页面顶部。 效果在下图可见。

*When users browse the content of pages, users can press the Scroll-to-top button to return to the top of pages. See:*

![mainpage-scroll-to-top][21]

- [x] 用户可以对感兴趣的题目按收藏按钮，也可以再次点击取消收藏。 效果在下面手机尺寸的GIF图里可见。

*Users can collect their favoraite questions by Star button, and they can also cancel collection by pressing Star button again. See the following GIF in phone size.*

![mainpage-All][17]

- [x] 用户可点击主页面的“post your question”来发布自己的问题，也可以在子页面的“leave a comment"下发表对别人问题的评论。效果如上面动图。

*Users can click the "Post your question" button in main page to publish their question. Users can also make comments on the "Leave a comment" block in subpages. See the GIF above.*

- [x] 所有页面实现自适应（响应式网页），符合大部分主流笔记本、手机等设备的尺寸。 效果如上面动图。

*All pages are self-adaption so that they can match most types of screen and display differently.*

<h3 id="2.2.2"> 2. 使用技术  Techniques</h3>

> * 饼图展示投票结果使用了 [Chart.js][20] 这个很酷炫的库，并对其中的Pie chart 的 JQuery 代码稍许改动以实现投票后重写饼图，或以json形式从后端获得已投票的结果并展示
*The multiple choices voting shows result by using the Pie chart module of the [Chart.js][20] library, and the JQuery code has been modified to implement the redisplay of voting result, or transmit the voted data by json to the Pie chart module.*
> * 图片展示的放大缩小功能使用了 [Zoom.js][22] 库
*The function of zooming in or out employed the [Zoom.js][22] library.*
> * 一键返回页面顶部的功能是一个叫 [Unify][28] 的Bootstrap模板提供的Scroll-To-Top功能提供的
*The function that scroll back to the page top is provided by the Scroll-To-Top module of a Bootstrap template named [Unify][28].*

<h2 id="2.3"> 搜索结果页、用户中心页、个人信息页  Search result page, user center page and personal information page</h2>

<h3 id="2.3.1"> 1. 功能  Functions </h3>

#### 搜索结果页 (Search result page)  -->  [searchResult.html][23]

#### 用户中心页 (User center page)  -->  [userCenter.html][24]

#### 个人信息页 (Personal information page)  -->  [personInfo.html][25]

- [x] （搜索结果页）用户不仅可以通过关键字来搜索标题或内容与搜索内容相匹配的问题，还可以通过搜索用户名来得到用户搜索结果。

*(Search Result page) Users can not only search questions by titles or contents, but also search other user accounts by users' nickname.*

- [x] （用户中心页）用户在自己的用户中心可以看到自己的“已发布问题”，“我的评论”，“我收藏的问题”，“我的投票历史”，“系统消息”和“我关注的用户”。其中除了“系统消息”，其他栏都默认对外开放可见（或根据用户在个人信息页的设置“对外不可见”来隐藏自己的动态），别的用户都可以浏览该用户的用户中心。

*(User Center page) Users can view their own statements like "My posted questions", "My comments", "My collected quesiton", "My voting history", "System message" and "My followed users" in their user center. Except "System message", all other columns are visible to other users (unless the user set "hide the records from visitors" to conceal their status).*

- [x] （用户中心页）用户可以删除自己的问题、评论、收藏、系统消息。注意，当用户删除自己的问题时，所有关于这个问题的投票和评论也都被删除了，所以HowToChooose社区规定：当投票总数超过50票时，该问题就成为公众问题，问题不可被提问者删除（该功能已在后端实现）。另外，用户不可以删除自己的投票记录，因为社区规定一旦用户投票完成以后，不可以改变自己的投票。

*(User Center page) Users can delete their posted question, comments, collections and system messages. Note that when users delete their posted questions, all votes and comments of this question will be removed too. Therefore, the How To Chooose community specifies that "When the number of votes exceeds 50, the question changes to public question and its questioner cannot delete it any more." (this function has been implement in back-end). In addition, users are not allowed to remove their voting histories because the community regulates that users cannot modify their votes after voting questions.*

- [x] （用户中心页）当访问者进入其他社区成员的用户中心页时，访问者可以点击心形按钮来关注该用户，再次点击按钮可取消关注。

*(User Center page) When visitors enter user center of one member, visitor can follow this user by clicking the heart-shaped button. Clicking this button again can unfollow.*

- [x] （用户中心页）用户可以在自己的用户中心页的“Edit Profile"按钮来进入个人信息页面，除用户自己之外的访问者看不到这个按钮，也不能进入该用户的个人信息页面。 以上四条功能的效果可看下面的动图：

*(User Center page) Users can press "Edit Profile" button in their own User Center page to enter the Personal Info page, while all other visitors are not allowed to see them. See：*

![userCenter-All][26]

- [x] （个人信息页）用户可以在个人信息页填写个人信息（非必填），还可以修改头像，已填的信息和头像会被展示在用户中心页。用户也可以设置是否允许来访者浏览自己的各种动态。页面如下图：

*(Personal Information page) Users can fill in their personal information in this page (dispensable), and can change their images. All filled information will be shown in User Center page. Users can also set whether the visitors are allowed to see their own status. See:* 

![personInfo-All][27]


<h3 id="2.3.2"> 2. 使用技术  Techniques </h3>
> * 在用户中心页使用了大量ajax异步来传输json，从而实现关注用户、删除问题、删除评论、删除收藏、删除系统消息等功能对后台数据库的异步请求而不需要重载整个页面。
*The asynchronous request of Ajax is used in User Center page to transmit json data, so the functions, such as following other users and deleting questions, comments, collections and system messages, can send request to database and execute without reloading the whole page.*

<h2 id="2.4"> 提问页面  Post Question page</h2>

<h3 id="2.4.1"> 1. 功能  Functions </h3>

#### 提问页面 (Post Question page)  -->  [post.html][29]

- [x] 第一步（Step 1）填写问题标题、选择问题的主题类型和投票形式。注意，问题标题（Title）不能为空，问题的主题类型（Topic）必须选择，问题的投票形式默认为 **赞/踩（Up/Down）**，也可选择 **多选(Multiple Choices)**。当标题为空或问题的主题类型未选中时提交问题，网页会报告提交错误。全部填完，则可按“Next”进行下一步。

*Step 1: Fill in title of question, choose topic and vote type of question. Note that Title of question cannot be empty and Topic must be selected. Default vote type of question is **Up/Down**, or you can choose **Multiple Choices**. When the title is null or the topic is unselected, the webpage will report error if you submit. Clicking "Next" can go to next step after you finish entering.*

- [x] 选择 **赞/踩（Up/Down）**的第二步（Step 2）：填写对问题的描述、上传和问题相关的图片。注意，问题描述和上传图片不能同时为空，至少要写问题描述，或至少上传一张图片，才能发表问题。完成问题，可按“Post”提交问题并跳到提交完成页面，也可按“Previous”按钮返回到上一步修改内容，且第二步已填的内容会被保留。但如果返回第一步更改了投票形式，第二步已填的内容就会被删除，需要重新填写。效果看如下动图：

*Step 2 of **Up/Down**: Fill in description of question, upload pictures related to question. Note that description and uploaded picture cannot be empty at the same time, which means that at least you should descript the question or you ought to upload at least one picture so that you can post question. When finishing, you can press "Post" button to submit question and the page will jumps to Completed page, or you can click "Previous" to go back to the last step to modify some data and the content of this step 2 will be retained. However, if you changes the vote type of question after you go back from step 2, the completed content in Step 2 will be removed and you need to enter again. See:

![post-UpDown][30]

- [x] 选择 **多选(Multiple Choices）**的第二步（Step 2）：选择多选的个数、填写每个选项的内容、填写问题的描述、上传图片。填写描述和上传图片与上面类似。注意，多选的个数默认为2。选完选项后，选项内容栏的数量会根据选择的数目改变。所有选项内容栏不能为空，否则提交问题时网页会报告提交错误。完成填写，可按“Post”提交问题，也可按“Previous"返回上一步。效果如下图：

* Step 2 of **Multiple Choices**: choose the number of choices, fill in contents of each choices, fill in description of question, upload pictures. Writing description and uploading images are similar to above. Note that the default number of multiple choices is 2. After you selected the number of choices, the number of choice content bars will change according to the number you choosed. All content of choice bars are not allowed to be empty, otherwise the webpage will report error when you submit question. After finishing, you can click "Post" to go forward or click "Previous" to go back. See:

![post-Multiple][31]

<h3 id="2.4.2"> 2. 使用技术  Techniques </h3>

> * 由于提交问题的逻辑比较复杂，分两条支线，我在网上下载的一个好看的分步填写表单的模板，并在此基础上用JQuery对模板的步骤逻辑部分（javascript）彻底重写。我用到了JQuery的遍历来使表单进入下步或返回上步（已填的数据会被保留），用JQuery的众多选择器来选中并判断用户输入的相应输入框的内容是否符合要求，且使用JQuery的事件监听来使得选项框的数量能根据用户选择的数字动态变化。
*Due to the complexity of logic of posting question, the main steps are separated into two paths. I use a template of step-by-step form and completely rewrite the logic part (javascript) of this template by JQuery. I use the traversal of JQuery to implement going forward and going back in same page and the filled data is retained. The selectors of JQuery are employed to select and check whether the users' inputs meet the requirements. I also use the event listening of JQuery to dynamically change the number of choice content bars correspoding to the digit user selected.*


  [1]: https://github.com/sriting
  [2]: https://github.com/junchen14
  [3]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/register.html
  [4]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/verification.html
  [5]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/login.html
  [6]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/forgetpw.html
  [7]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/resetpw.html
  [8]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/login.html
  [9]: image/register-iphone6.png
  [10]: image/register-laptop.png
  [11]: https://uigradients.com
  [12]: https://pypi.python.org/pypi/DjangoCaptcha
  [13]: image/mainpage-upDown.gif
  [14]: image/mainpage-Multiple.gif
  [15]: image/mainpage-Collapse+image.gif
  [16]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/mainpage.html
  [17]: image/mainpage-All.gif
  [18]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/commentPage.html
  [19]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/commentPage2.html
  [20]: http://www.chartjs.org
  [21]: image/mainpage-scroll-to-top.png
  [22]: https://github.com/hakimel/zoom.js
  [23]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/searchResult.html
  [24]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/userCenter.html
  [25]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/personInfo.html
  [26]: image/userCenter-All.gif
  [27]: image/personInfo-All.png
  [28]: http://www.gprinmobiliaria.cl/plantilla/Documentation/ 
  [29]: https://sriting.github.io/HowToChooose-website/HowToChooose-frontend/post.html
  [30]: image/post-UpDown.gif
  [31]: image/post-Multiple.gif


