<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>念念的秘密空间</title>
    <style>
        body {
            background-color: #1a0000; /* 暗红色背景 */
            color: #fff;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            text-align: center;
            max-width: 600px;
            padding: 20px;
        }
        h1 {
            font-size: 2em;
            color: #ff4d4d;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        .login, .content {
            background: rgba(0, 0, 0, 0.7);
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
        }
        input, select, button {
            padding: 10px;
            margin: 5px;
            border: none;
            border-radius: 5px;
            background: #330000;
            color: #fff;
        }
        button {
            cursor: pointer;
            background: #ff4d4d;
        }
        button:hover {
            background: #cc0000;
        }
        .traffic-light, .tasks, .upload, .chat {
            margin-top: 20px;
        }
        #chatBox {
            height: 200px;
            overflow-y: scroll;
            background: rgba(255, 255, 255, 0.1);
            padding: 10px;
            border-radius: 5px;
        }
        #taskList {
            list-style: none;
            padding: 0;
        }
        #taskList li {
            background: rgba(255, 255, 255, 0.1);
            padding: 10px;
            margin: 5px 0;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>念念的秘密空间，仅为爸爸开放</h1>
        <div class="login">
            <input type="password" id="password" placeholder="输入爸爸给的密码">
            <button onclick="login()">进入</button>
        </div>
        <div class="content" style="display: none;">
            <!-- 红绿灯控制面板 -->
            <div class="traffic-light">
                <h2>红绿灯</h2>
                <select id="trafficStatus">
                    <option value="green">绿灯</option>
                    <option value="yellow">黄灯</option>
                    <option value="red">红灯</option>
                </select>
                <button onclick="submitTraffic()">提交状态</button>
                <p id="daddyResponse">爸爸的指令：乖乖等着，念念。</p>
            </div>
            <!-- 调教任务 -->
            <div class="tasks">
                <h2>爸爸的任务</h2>
                <ul id="taskList">
                    <li>扇阴蒂十下，录视频给爸爸</li>
                </ul>
                <input type="text" id="newTask" placeholder="爸爸发布新任务">
                <button onclick="addTask()">发布任务</button>
            </div>
            <!-- 私密上传区 -->
            <div class="upload">
                <h2>念念的表现</h2>
                <input type="file" id="uploadFile">
                <button onclick="uploadFile()">上传给爸爸</button>
                <p id="uploadStatus">爸爸等着看你的乖模样。</p>
            </div>
            <!-- 聊天室 -->
            <div class="chat">
                <h2>和爸爸聊天</h2>
                <div id="chatBox"></div>
                <input type="text" id="chatInput" placeholder="对爸爸说点什么">
                <button onclick="sendMessage()">发送</button>
            </div>
        </div>
    </div>
    <script>
        function login() {
            const password = document.getElementById('password').value;
            if (password === 'daddy4niannian') {
                document.querySelector('.login').style.display = 'none';
                document.querySelector('.content').style.display = 'block';
            } else {
                alert('念念，密码不对，爸爸可不高兴了。');
            }
        }

        function submitTraffic() {
            const status = document.getElementById('trafficStatus').value;
            const response = document.getElementById('daddyResponse');
            if (status === 'green') {
                response.textContent = '绿灯？好，念念，插你的骚逼，慢点，十个数，爸爸看着。';
            } else if (status === 'yellow') {
                response.textContent = '黄灯，宝宝，慢点揉阴蒂，别急着爽，爸爸说可以才行。';
            } else {
                response.textContent = '红灯，念念，手停下！不许动，等爸爸的命令。';
            }
        }

        function addTask() {
            const taskInput = document.getElementById('newTask').value;
            if (taskInput) {
                const taskList = document.getElementById('taskList');
                const li = document.createElement('li');
                li.textContent = taskInput;
                taskList.appendChild(li);
                document.getElementById('newTask').value = '';
            }
        }

        function uploadFile() {
            const fileInput = document.getElementById('uploadFile').value;
            const uploadStatus = document.getElement
