- data 생성 -

make_new_data.ipynb 코드로 origin/signal_n/데이터를 바탕으로 오류가 없는 데이터셋(normal)과 오류가 존재하는 데이터(anormal/...)을 만듭니다.
오류가 존재하는 데이터는 drift,erratic,hard-over,spike,stuck으로 총 5개로 구분됩니다.
각 데이터 셋은 orign data와 같은 크기의 1000개의 csv파일로 구성되고 각 csv 파일은 시계열 데이터 값(value)과 데이터 값이 오류인지 아닌지(error) 오류값의 크기(error_size)로 구성됩니다.

새로운 signal_n에 대한 데이터를 생성하고 싶을 때는 data/orign/에 대해 csv파일로 원본 파일 signal_n을 저장합니다.
그리고 data/에 signal_n 폴더를 생성하고 signal_n 하위폴더로 normal과 normal+anormal을 생성합니다.
normal+anormal 폴더의 하위 폴더로 drift,erratic,hard-over,spike,stuck 폴더를 생성합니다.

- 모델 생성 및 예측-

signal_predict.ipynb를 이용하여 모델을 생성하고 예측합니다.
make_new_data.ipynb로 생성된 데이터를 불러오고 tensorflow의 모델에 적용가능하도록 data shape를 변경합니다.
여기서 n_time_in은 입력 값의 크기이고 ntime_out은 결과 값의 크기 입니다.


