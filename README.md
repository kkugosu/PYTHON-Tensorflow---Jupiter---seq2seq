(https://img.shields.io/github/license/RubixML/RubixML)](https://github.com/RubixML/ML/blob/master/LICENSE.md)
# seq2seq
안녕하세요 seq2seq로 영어 프랑스어 간의 번역기를 만드려고 텐서플로로 구현해보았는데요
텐서플로구조가 define and run 이라 워낙에 복잡해서 check point를 만들어두었습니다.

제가 하이퍼파라미터를 변형하는수준을 넘어서 텐서플로를 자유자재로 다루며 깊이 이해하려 하다보니
일부러 encoder decoder를 분리하여 각기 다른파일에 배치하고 그 안에서 텐서플로를 정의하고 
거기서 제공하는 seq2seq를 활용하지않고 dynamic하게 직접 다 짜서 썼습니다

텐서플로에서 사용하는 seq2seq툴은 디코더의 max길이가 정해져있던데
직접 짜보면 이게 evaluate할땐 몰라도 training할땐 길이값을 굳이 하나로 고정시키지 않아도 되더라구요

파일은 총 4개의 ipython으로 이루어져있고
main을 실행시키면 나머지 세개를 임포트하여 실행이됩니다.

제가만든모델은 encoder와 decoder가 분리되어 동작하는데
training을 시키려고보니 training도 따로 되더랍니다..

그래서 다 갈아업다보니 일이 너무많아져서
나중에라도 분리된상태로 training시킬일이 있을지 모르니 코드를 살려두었습니다.

tensorflow에서 미리 그려진 그래프를 dynamic하게 활용하다보니 튜토리얼에서 배우던 문법으론 한계가 있더라구요

그래서 개인적으로 get_variable_scope, get_variable, variable_scope 등에 대해 공부를 하면서
tf.scan문의 활용법 그리고 place_holder, sparse_place_holder 등에 대해서도 공부하는 시간이 되었습니다.

encoder는 naive encoder이며
decoder에서 attention은 dot product하는 방식으로 구현하였습니다.

pytorch tutorial을 참조하면서 구현하다보니 어느정도 비슷한면이 있을지 모르겠군요
