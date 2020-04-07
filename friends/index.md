---
title: 好伙伴们
date: 2018-08-06 12:44:02
---
<div class="linkpage"><ul id="friendsList"></ul></div>

<script type="text/javascript">
// 以下为样例内容，按照格式可以随意修改
var myFriends = [
    ["http://crystalrays.lofter.com/", "https://avaimg.nosdn.127.net/img/WUx6WXltMXVsUFp2UlY3V3pBdWxaYXVXaXA3UEl6dHBHbEZMVGZORzQvcFFHa3NJREYzbS9RPT0.jpg", "CrystalRays", "一位程序大佬"], 
    ["https://www.bokutake.com/", "https://cn.gravatar.com/avatar/e57379eaaadeba99e175d5173eb6ba0d", "Октябрьская революция", "Welt von Bokutake"], 
    ["https://www.fczbl.vip/", "https://cn.gravatar.com/avatar/5e6892e999ca8c85a358d21164167f38", "犬's Blog", "一位掌握了微软的独特打开方式的大佬"], 
    ["https://diygod.me/", "https://diygod.me/images/DIYgod.jpg", "DIYgod", "是裙里最大的绒布球"],
    ["https://www.fghrsh.net/", "https://cn.gravatar.com/avatar/0c5d77513a08b8c3e38336859b53b027", "FGHRSH", "一只可爱的阿狸"]
];

// 以下为核心功能内容，修改前请确保理解您的行为内容与可能造成的结果
var  targetList = document.getElementById("friendsList");
while (myFriends.length > 0) {
    var rndNum = Math.floor(Math.random()*myFriends.length);
    var friendNode = document.createElement("li");
    var friend_link = document.createElement("a"), 
        friend_img = document.createElement("img"), 
        friend_name = document.createElement("h4"), 
        friend_about = document.createElement("p")
    ;
    friend_link.target = "_blank";
    friend_link.href = myFriends[rndNum][0];
    friend_img.src=myFriends[rndNum][1];
    friend_name.innerText = myFriends[rndNum][2];
    friend_about.innerText = myFriends[rndNum][3];

    friend_link.appendChild(friend_img);
    friend_link.appendChild(friend_name);
    friend_link.appendChild(friend_about);

    friendNode.appendChild(friend_link);
    targetList.appendChild(friendNode);

    myFriends.splice(rndNum, 1);
}
</script>
