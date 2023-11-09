<body>
<html>
<head>
  <title>心理測驗</title>
  <style>
    body {
      font-family: Arial;
      background-color:LightCoral;
    }
    
    .question {
      margin-bottom: 10px;
     
       border: 5px solid #f5f5f5; 
    }
     .smaller-image {
            width: 300px;
           height: 300px; 
        }
    .options input {
      margin-right: 10px;
    }
     #result {
      display: none;
      font-weight: bold;
    }
   
  </style>
</head>
<body>
  <h1 style="text-align: center;">心理測驗</h1>
  
  <div class="question" style="text-align: center;">
    <p>選擇一種小動物，看看你朋友對你真實評價</p>
    <div class="options" style="display: flex; flex-direction: column; align-items: center;">
       <a href="#"><img class="smaller-image" src="https://img.onl/9hfok3" alt="松鼠"></a>
      <input type="radio" name="q1" value="a">松鼠<br>
       <a href="#"><img class="smaller-image" src="https://img.onl/4PxiHF" alt="無尾熊"></a>
      <input type="radio" name="q1" value="b">無尾熊<br>
       <a href="#"><img class="smaller-image" src="https://img.onl/2WDnP3" alt="綿羊"></a>  
      <input type="radio" name="q1" value="c">綿羊<br>
        <a href="#"><img class="smaller-image" src="https://img.onl/npblrg" alt="長頸鹿"></a>
        <input type="radio" name="q1" value="d">長頸鹿<br>
        <a href="#"><img class="smaller-image" src="https://img.onl/WZiqUn" alt="小鹿"></a>
      <input type="radio" name="q1" value="e">小鹿<br>
      <p>按下方按鈕查看答案</p>
    </div>
  </div>
  
  <div style="text-align: center;">
    <button onclick="calculateResult()">按我按我!</button>
    
    <div id="result" style="font-weight: bold;"></div>
  </div>
  
  <script>
    function calculateResult() {
      var q1Answer = document.querySelector('input[name="q1"]:checked').value;
      
      var result = "";
      
      if (q1Answer === "a" ) {
        result = "你的察覺能力很強，是朋友心中的靠山!";
      } else if (q1Answer === "b") {
        result = "你是個嚮往寧靜生活的人，會專注在自己喜歡的事物上。";
      } else if (q1Answer === "c" ) {
        result = "你很清楚自己的目標，會積極地找尋人生方向。";
      } 
      else if (q1Answer === "d" ) {
        result = "你是個自律的人，完美主義者。";
      } 
      else {
        result = "不論發生什麼事情，你都會給予朋友幫助。";
      }
      
      document.getElementById("result").innerHTML = result;
 document.getElementById("result").style.display = "block";
    }
  </script>
</body>


</html>
