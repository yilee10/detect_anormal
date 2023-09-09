make_new_data.ipynb로 origin데이터를 바탕으로 한 오류가 없는 데이터셋(normal)과 오류가 존재하는 데이터(anormal/...)을 생성합니다

오류가 존재하는 데이터는 drift,erratic,hard-over,spike,stuck으로 총 5개로 구분됩니다.

각 데이터 셋은 1000개의 csv파일로 구성되고 각 csv은 4032크기의 시계열 데이터 값과 오류로 구성됩니다.


