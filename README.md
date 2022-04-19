# Lip synchronization model for the Tamil language

<div align="center">
    <img src="mesh.png" width="100"/>
</div>

<div align="center">
    <img src="https://img.shields.io/github/license/MohamedSabthar/Lip-synchronization-model-for-the-Tamil-language"/>
</div>

<div align="justify">
<p>
 Our model predicts 3D face animation for a given Tamil audio speech with considering the coarticulation effects. Our model achieved a Root Mean Square Error of 0.0648 in our test data split and achieved an 83% of overall subjective accuracy. Further, the Turing test confirmed that participants were unable to distinguish our predicted animation from the ground.
</p>

### Results

<table>
  <tr>
    <td>
      <a
        href="https://www.youtube.com/embed/videoseries?controls=0&amp;list=PLCeMyGcfkc9gAmnLjAPLfmiK7w-HkJFoM"
        target="_blank"
      >
        <img
          src="https://i3.ytimg.com/vi/1ydDP6Z28Y8/maxresdefault.jpg"
          alt="Watch the video"
          border="10"
        />
      </a>
      <div align="center">SHORT SPEECH</div>
    </td>
    <td>
      <a
        href="https://www.youtube.com/embed/videoseries?controls=0&amp;list=PLCeMyGcfkc9iZfYKbhFqbDMOyJyiywfFS"
        target="_blank"
      >
        <img
          src="https://i3.ytimg.com/vi/hR1Qkq4Rjdw/maxresdefault.jpg"
          alt="Watch the video"
          border="10"
        />
      </a>
      <div align="center">LONG SPEECH</div>
    </td>
  </tr>
  <tr>
    <td>
      <a
        href="https://www.youtube.com/embed/videoseries?controls=0&amp;list=PLCeMyGcfkc9gonnxxaP39nBCH-FOMZkUn"
        target="_blank"
      >
        <img
          src="https://i3.ytimg.com/vi/gm2goBVYTl8/maxresdefault.jpg"
          alt="Watch the video"
          border="10"
        />
      </a>
      <div align="center">FAST SPEECH</div>
    </td>
    <td>
      <a
        href="https://www.youtube.com/embed/videoseries?controls=0&amp;list=PLCeMyGcfkc9jhrbjYOkWy15_OYxsZITAg"
        target="_blank"
      >
        <img
          src="https://i3.ytimg.com/vi/0aUZLm46wV4/maxresdefault.jpg"
          alt="Watch the video"
          border="10"
        />
      </a>
      <div align="center">SLOW SPEECH</div>
    </td>
  </tr>
  <tr>
    <td>
      <a
        href="https://www.youtube.com/embed/videoseries?controls=0&amp;list=PLCeMyGcfkc9jGoLEHl9mM-AUJ3tRHjyF0"
        target="_blank"
      >
        <img
          src="https://i3.ytimg.com/vi/hpdGtkj_oD8/maxresdefault.jpg"
          alt="Watch the video"
          border="10"
        />
      </a>
      <div align="center">MIXED LANGUAGE SPEECH</div>
    </td>
  </tr>
</table>

### Required packages & libraries

- `librosa 0.8.1`
- `ffmpeg 4.3.1 `
- `opencv-python 4.5.2`
- `scipy 1.6.2`
- `tensorflow 2.6.0`
- `sklearn 0.22.2`
- `Blender 2.92.0`
- `pickle 4.0`
- `numpy 1.20.0`
- `matplotlib 3.3.4`
- `tqdm 4.59.0`
- `keras-tuner 1.1.2`
- `mediapipe 0.8.9.1`

### Model training

- Place all recorded training videos inside VIDEOs directory
- Run `PDM.py` and `Preprocess.py` in the specified order to perform feature extraction
- Run `HyperparameterTuning.py` to pick best possible hyperparameter combination (optional)
- Set the best hyperparameter values in the `BLSTM_128_64.py` file (optional)
- Run `BLSTM_128_64.py` to train the deeplearning model

### Model prediction

- Record the input Tamil speech audio and place it inside the `VIDEOs/AUDIOs/` directory
- Set Blender path in Prediction.py in `cmd` variable
- Run command `python Prediction.py <fileName> <audioFormat>` to generate animation

### Pre-trained model

To try our trained model download the preporocessor and model weights from [WeightsAndPreprocessor.zip](https://drive.google.com/file/d/1nRPOQnRJTJzOf20rFS7lXZzyWpGL69mQ/view?usp=sharing) and unzip them inside the `logs` directory


###### python implementation will be published soon after publishing the research paper.