<!DOCTYPE html>
<html>
<head>
  <title>Online Voting System</title>
  <style>
    body {
      font-family: Arial;
      background: #f2f2f2;
      text-align: center;
    }

    .box {
      background: white;
      width: 350px;
      margin: 100px auto;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0px 0px 10px gray;
    }

    button {
      padding: 10px 20px;
      margin: 10px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .bjp { background: orange; color: white; }
    .congress { background: blue; color: white; }
    .aap { background: green; color: white; }

    #result {
      margin-top: 20px;
      font-weight: bold;
    }
  </style>
</head>

<body>

<div class="box">
  <h2>🗳️ Online Voting System</h2>

  <button class="bjp" onclick="vote('BJP')">Vote BJP</button>
  <button class="congress" onclick="vote('Congress')">Vote Congress</button>
  <button class="aap" onclick="vote('AAP')">Vote AAP</button>

  <div id="result"></div>
</div>

<script>
  let votes = {
    BJP: 0,
    Congress: 0,
    AAP: 0
  };

  function vote(party) {
    votes[party]++;
    showResult();
  }

  function showResult() {
    document.getElementById("result").innerHTML =
      "BJP: " + votes.BJP + "<br>" +
      "Congress: " + votes.Congress + "<br>" +
      "AAP: " + votes.AAP;
  }
</script>

</body>
</html>
