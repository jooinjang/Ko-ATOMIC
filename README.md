# Ko-ATOMIC
Korean Commonsense Knowledge Graph


## 작업 완료 목록

- [X] EleutherAI/polyglot-ko-5.8b 기반 zero-shot inference (2022.11월 1주차)

    > zero-shot inference 결과가 거의 못 쓸 정도. 
      GPT-3와 똑같은 형태의 prompt가 잘 먹히지 않는 듯.
      GPT-neox 논문 읽어보고 zero-shot prompt를 다시 만든 다음, 다시 zero-shot inference
    
    
- [X] KommonGen 완성형 문장의 'Human-Like entity'를 normalization(?)(ATOMIC의 PersonX처럼 사람 X, 사람 Y로 대치)


    - Human-Like entity: 특정 성별('남성', '여성', 남자', '여자',...)이나 세대('소녀', '소년', '십대', '젊은이', '노인',...) 등에 대한 정보가 담긴, "사람"을 나타내는 토큰
    
    - ATOMIC과 같이 PersonX, PersonY, ...의 형태로 치환해야 함
    
      1. ATOMIC_trans가 이러한 표현을 그대로 사용함
      
      2. KommonGen의 완성형 문장에 포함된 "Human-Like enitity"를 그대로 유지할 경우, 어떤 상식 정보가 특정 나이나 성별에서만 나타나거나 나타나지 않을 수도 있음
      
         Common-sense knowledge graph의 성격을 고려하여 그래프가 표현하는 정보는 "일반적인 것"이어야 함

