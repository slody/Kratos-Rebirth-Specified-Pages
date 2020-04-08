---
title: 好伙伴们
date: 2018-08-06 12:44:02
---
<div class="linkpage"><ul id="friendsList"></ul></div>

<script type="text/javascript">
// 以下为样例内容，按照格式可以随意修改
var myFriends = [
    ["#", "https://candinya.com/images/avatar.png", "猫猫", "喵喵~"], 
    ["#", "https://candinya.com/images/avatar.png", "猫猫猫", "喵喵喵~"], 
    ["#", "https://candinya.com/images/avatar.png", "猫猫猫猫", "喵喵喵喵~"]
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
