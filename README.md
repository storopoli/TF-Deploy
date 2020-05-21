# Deploying-Deep-Learning-Models-using-TensorFlow-Serving-with-Docker-and-Flask
In this project, we will deploy a Pre-trained TensorFlow model with the help of TensorFlow Serving with Docker, and we will also create a visual web interface using Flask web framework which will serve to get predictions from the served TensorFlow model and help end-users to consume through API calls. 

## Execution Steps: 

  1.  Setting up tensorflow serving server on localhost:

      ```bash
      sudo docker run -d -p 8501:8501 --name=pets -v "$(full_path_to_directory)/pets:/models/pets/1" -e MODEL_NAME=pets tensorflow/serving
      ```

  2.  Setup virtual environment and installing flask and its dependencies: 

      ```bash
      python3 -m venv env
      source env/bin/activate
      
      python3 -m pip install requirements.txt
      ```

3. Run the Flask app:

   ```python
   python app.py
   ```

4. Access the app by going to `localhost:5000` in your browser

---

> Ref: https://www.coursera.org/projects/deploy-models-tensorflow-serving-flask