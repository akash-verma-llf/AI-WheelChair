<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Voice-Controlled Wheelchair</title>
  <style>
    body { font-family: Arial; text-align: center; padding: 30px; }
    #label-container div { margin: 8px; font-size: 20px; }
    button { padding: 12px 24px; font-size: 18px; }
  </style>
</head>
<body>
  <h2>Voice Control: Wheelchair Commands</h2>
  <button onclick="init()">Start Listening</button>
  <div id="label-container"></div>

  <!-- Load TensorFlow.js and speech commands model -->
  <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@1.3.1/dist/tf.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@tensorflow-models/speech-commands@0.4.0/dist/speech-commands.min.js"></script>

  <script>
    // Replace with your own model link from Teachable Machine
    const MODEL_URL = "https://teachablemachine.withgoogle.com/models/A7x7dP2Bg/";
    
    let recognizer;
    let labelContainer;

    async function createModel() {
      const checkpointURL = MODEL_URL + "model.json";
      const metadataURL = MODEL_URL + "metadata.json";

      recognizer = speechCommands.create("BROWSER_FFT", undefined, checkpointURL, metadataURL);
      await recognizer.ensureModelLoaded();
    }

    async function init() {
      await createModel();
      const classLabels = recognizer.wordLabels();
      labelContainer = document.getElementById("label-container");
      labelContainer.innerHTML = "";

      for (let i = 0; i < classLabels.length; i++) {
        const div = document.createElement("div");
        div.id = "label" + i;
        labelContainer.appendChild(div);
      }

      recognizer.listen(result => {
        const scores = result.scores;
        let maxScore = 0;
        let maxLabel = "";

        for (let i = 0; i < scores.length; i++) {
          const score = scores[i];
          const label = classLabels[i];
          const text = `${label}: ${score.toFixed(2)}`;
          document.getElementById("label" + i).innerHTML = text;

          if (score > maxScore) {
            maxScore = score;
            maxLabel = label;
          }
        }

        // Send result back to MIT App Inventor (WebView)
        if (window.AppInventor) {
          window.AppInventor.setWebViewString(maxLabel);
        }
      }, {
        includeSpectrogram: false,
        probabilityThreshold: 0.75,
        overlapFactor: 0.5
      });
    }
  </script>
</body>
</html>
