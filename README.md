# Face-Recognition-using-SiameseNet
facedata source : https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&dataSetSn=83  
=> 해당 facedata는 저,중,고화질 데이터로 나뉘어져 있는데 그중 중화질을 사용하였음(사유 : 용량 문제)  
1인당 20~40장 정도 사용 권장
  
  1. Preprocessing : 이미지들을 face detection 하여 주변 배경이 학습에 영향 주지 않도록 하고 resizing 함  
  2. make .txt : training, testing에 사용할 데이터들을 무작위 추출하여 [name, 파일번호, 파일번호] => label 1, [name, 파일번호, name, 파일번호] => label 0 (data_loader.py에서 txt 파일 기반으로 레이블링 하게 되어있음)  
  3. experiment.py : txt 파일을 읽어들여 pickle 파일을 생성 및 기록하고, weights 폴더내에 weights 파일을 만들어 training 동안 weights를 업데이트하고 재기록함  
  
AntiSpoofing에 사용할 shape_predictor_68_face_landmarks.dat 파일 추가로 다운받아야함
