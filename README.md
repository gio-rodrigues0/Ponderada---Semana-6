# Detector de rachaduras
Para a criação desse detector, dois processos precisaram ser realizados: o treinamento do modelo e a criação de um script em python.

## Treinamento do modelo
1. Instalação da biblioteca ultralytics, ela possui o YOLO, utilizado na detecção de objetos em tempo real.
2. Instalação do Roboflow, onde há diversos datasets prontos para várias versões do YOLO.
3. Importação do Roboflow e acesso a minha chave de API.
4. Declaração de onde achar o dataset que eu preciso, passando o workspace e o nome do projeto, depois, download desse dataset no modelo feito para o yolov8.
5. Treinamento do modelo com os dados do dataset com 10 épocas, esse treinamento gera um arquivo que é utilizado no script a seguir, denominado como "best.pt".

## Script em python
1. Importação da biblioteca ultralytics e cv2, para usar o OpenCV.
2. Usamos a função VideoCapture do OpenCV para ter acesso a webcam do computador.
3. Depois o método predict do YOLO em cima dos frames do vídeo.
4. Com o método imshow a gente abre esse vídeo numa nova janela e clicando em "q" conseguimos interromper a operação.

Vídeo do funcionamento: https://drive.google.com/file/d/14Nbwy1B1udTjLZ-1SLXxx7fvecvdua1E/view?usp=sharing
