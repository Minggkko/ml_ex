# ml_ex
머신러닝 scikit-learn 실습 - 지도학습,비지도학습

# app 설치 라이브러리
```
pip insatll streamlit
```
# streamlit 배포시 필수 사항
- os는 linux임, 인식하는 path로 변경해야함
# 1. 파일 path
- 예시 : 모델 로딩 방법
``
@st.cache_resource # 자원 캐싱 기능
def load_model():
    model_path = os.path.join(base_path, "models", "iris_model_rfc.pkl") # models/iris_model_rfc.pkl
    # with open('models/iris_model_rfc.pkl', 'rb') as f:
    with open(model_path, 'rb') as f:
        model = pickle.load(f)
    return model
model = load_model()
```



# requiremnts.txt 파일 생성방법
```
pip freeze > requirements.txt
```

# 예시 requitremts 
numpy==2.3.5
streamlit==1.15.0
scikit-learn==1.7.2
joblib==1.5.2