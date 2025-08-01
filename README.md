# Animalhelper.tts

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Animal Helpers - Click to Listen</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: "Arial", sans-serif;
      background-color: #fffdf5;
      padding: 20px;
    }

    h1 {
      text-align: center;
      color: #2a5d84;
      margin-bottom: 20px;
    }

    .sentence-block {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    button {
      font-size: 1.2em;
      padding: 12px 16px;
      border: none;
      border-radius: 10px;
      background-color: #a7d8ff;
      color: #003049;
      box-shadow: 1px 2px 4px rgba(0,0,0,0.1);
      cursor: pointer;
      transition: background-color 0.3s;
      width: 100%;
      text-align: left;
    }

    button:hover {
      background-color: #90cbee;
    }

    @media (min-width: 600px) {
      button {
        max-width: 600px;
      }
    }
  </style>
</head>
<body>
  <h1>🐾 Animal Helpers</h1>

  <div class="sentence-block">
    <button onclick="speak('More than half of all U.S. homes have pets in them.')">▶ More than half of all U.S. homes have pets in them.</button>
    <button onclick="speak('People help animals.')">▶ People help animals.</button>
    <button onclick="speak('We give them homes and food.')">▶ We give them homes and food.</button>
    <button onclick="speak('Animals help people, too.')">▶ Animals help people, too.</button>
    <button onclick="speak('Let\'s see how.')">▶ Let's see how.</button>
    <button onclick="speak('Horses help people.')">▶ Horses help people.</button>
    <button onclick="speak('They take us for rides.')">▶ They take us for rides.</button>
    <button onclick="speak('Camels help people.')">▶ Camels help people.</button>
    <button onclick="speak('They carry heavy loads.')">▶ They carry heavy loads.</button>
    <button onclick="speak('Cows help people.')">▶ Cows help people.</button>
    <button onclick="speak('They make milk for us to drink.')">▶ They make milk for us to drink.</button>
    <button onclick="speak('Milk makes you strong and healthy.')">▶ Milk makes you strong and healthy.</button>
    <button onclick="speak('Bees help people.')">▶ Bees help people.</button>
    <button onclick="speak('They make our gardens grow.')">▶ They make our gardens grow.</button>
    <button onclick="speak('They make sweet honey, too.')">▶ They make sweet honey, too.</button>
    <button onclick="speak('Mmmmmmmm!')">▶ Mmmmmmmm!</button>
    <button onclick="speak('Goats help people.')">▶ Goats help people.</button>
    <button onclick="speak('They eat up thick weeds.')">▶ They eat up thick weeds.</button>
    <button onclick="speak('Sheep help people.')">▶ Sheep help people.</button>
    <button onclick="speak('They give us wool to make yarn.')">▶ They give us wool to make yarn.</button>
    <button onclick="speak('Some people use dog sleds to race!')">▶ Some people use dog sleds to race!</button>
    <button onclick="speak('Dogs help people in many ways.')">▶ Dogs help people in many ways.</button>
    <button onclick="speak('They pull sleds in the cold.')">▶ They pull sleds in the cold.</button>
    <button onclick="speak('Wheeeeeeeee!')">▶ Wheeeeeeeee!</button>
    <button onclick="speak('Dogs help farmers get their sheep to go places.')">▶ Dogs help farmers get their sheep to go places.</button>
    <button onclick="speak('They also help people in wheelchairs.')">▶ They also help people in wheelchairs.</button>
    <button onclick="speak('Dogs open doors and fetch things.')">▶ Dogs open doors and fetch things.</button>
    <button onclick="speak('Cats help people, too.')">▶ Cats help people, too.</button>
    <button onclick="speak('How?')">▶ How?</button>
    <button onclick="speak('They make us so happy!')">▶ They make us so happy!</button>
  </div>

  <script>
    function speak(text) {
      const utterance = new SpeechSynthesisUtterance(text);
      utterance.lang = 'en-US';
      utterance.rate = 0.8; // 느린 속도 (초2 맞춤)
      utterance.pitch = 1.0;
      utterance.volume = 1.0;

      const voices = speechSynthesis.getVoices();
      const preferred = voices.find(v => v.lang === 'en-US' && v.name.includes('Google'));
      if (preferred) utterance.voice = preferred;

      window.speechSynthesis.cancel();
      window.speechSynthesis.speak(utterance);
    }

    if (speechSynthesis.onvoiceschanged !== undefined) {
      speechSynthesis.onvoiceschanged = () => {};
    }
  </script>
</body>
</html>
