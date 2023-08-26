 [![GitHub](https://img.shields.io/github/license/RubixML/RubixML)](https://github.com/RubixML/ML/blob/master/LICENSE.md)
 
# Seq2Seq 영어-프랑스어 번역기

텐서플로를 활용하여 `Seq2Seq` 모델로 영어와 프랑스어 간의 번역기를 구현해보았습니다.

## 📝 프로젝트 개요

- 텐서플로의 구조가 "define and run" 방식이라 복잡합니다. 따라서 중간마다 **check point**를 설정해두었습니다.
- 기본 제공되는 `seq2seq` 대신 **dynamic**한 구조로 직접 구현하였습니다.
- 파일 구조는 총 4개의 ipython 파일로 구성되어 있으며, `main` 실행 시 나머지 세 파일이 임포트됩니다.

## 💡 주요 특징

- **Encoder와 Decoder 분리**: 모델 구조상 Encoder와 Decoder가 독립적으로 작동합니다. 또한, training 시에도 독립적으로 진행됩니다.
- **Dynamic Seq2Seq**: 텐서플로에서 미리 정의된 그래프를 dynamic하게 조절하는 방식을 택하였습니다. 이를 위해 여러 텐서플로 문법과 기능을 활용하였습니다.
- **Attention Mechanism**: Decoder에서의 attention은 dot product 방식으로 구현되었습니다.

## 📚 공부 내용

텐서플로와 관련하여 다음과 같은 주제에 대해 깊이 공부하였습니다:

- `get_variable_scope`, `get_variable`, `variable_scope`
- `tf.scan` 활용법
- `place_holder`, `sparse_place_holder` 등

## 📌 참고

이 프로젝트는 pytorch tutorial을 참조하였기 때문에, 어느 정도 유사한 점이 있을 수 있습니다.


