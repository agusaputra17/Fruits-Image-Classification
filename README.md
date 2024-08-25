# Fruits Image Classification (Apple, Mango, Guava, Banana, Dragon Fruit, and Pomegranate)

This project is the final assignment for the Dicoding course "Belajar Pengembangan Machine Learning - Intermediate level". In this project, I developed a fruit image classification system that includes apples, mangoes, guavas, bananas, dragon fruits, and pomegranates.

The training and validation accuracy reached 96%. The dataset used consists of 12,792 images, which I downloaded from several sources including [Mendeley Data](https://data.mendeley.com), [Dataset Ninja](https://datasetninja.com), and [Vicos](https://www.vicos.si).

## tf_serving

TensorFlow Serving is used to serve the trained model. Below is an example response from the TensorFlow Serving model version status endpoint:

```
{
 "model_version_status": [
  {
   "version": "1",
   "state": "AVAILABLE",
   "status": {
    "error_code": "OK",
    "error_message": ""
   }
  }
 ]
}
```

```
docker run -it -v C:\Users\ThinkPad\Documents\Machine_Learning\Dicoding_Belajar_Pengembangan_Machine_Learning\FRUITS_CLASSIFICATION\saved_model:/models -p 8501:8501 --entrypoint /bin/bash tensorflow/serving

tensorflow_model_server --rest_api_port=8501 --model_name=fruits_model --model_base_path=/models/

http://localhost:8501/v1/models/fruits_model

```


