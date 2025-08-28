# 🗞️뉴스?! 애매하긴 해~
### BBC뉴스 기반 감정분석 (긍정, 부정, 중립)

### 🔎데이터 출처 및 사용 모델
- 데이터 출처: https://www.kaggle.com/code/gpreda/bbc-news-rss-feeds?select=bbc_news.csv(BBC 뉴스 데이터)
- 사용 모델: https://huggingface.co/datasets/SetFit/bbc-news

### 🖼️주제 선정 배경
디지털 환경에서 뉴스가 여론·소비·투자에 미치는 영향이 커졌지만, 사람이 모든 기사를 읽고 톤을 파악하긴 어렵습니다.
본 프로젝트는 BBC 뉴스 헤드라인/요약을 대상으로 감성(부정·중립·긍정) 분류를 수행해 시기·주제별 분위기 변화를 정량화하려고 합니다.
카테고리 구성이 명확하고 품질이 안정적인 BBC 데이터를 사용했으며, 사전학습 언어모델(Hugging Face) 로 빠르게 베이스라인을 구축했습니다.
또한, 헤드라인만으로 해당 뉴스의 분위기 파악을 하긴 어렵기 때문에 요약을 함께 보고 판단할 수 있게 했습니다. 

### ⚙️진행과정
<img width="1517" height="655" alt="image" src="https://github.com/user-attachments/assets/b89cb1b2-e554-424b-95c8-06723d4347f3" />
<img width="526" height="212" alt="image" src="https://github.com/user-attachments/assets/d1663156-413e-4374-987c-102cbc9faa87" /><br>
=> 모델을 정한 후 성능을 테스트하기 위한 문장을 간략하게 입력해보았습니다. <br>
<br>

<img width="1755" height="485" alt="image" src="https://github.com/user-attachments/assets/cc70361e-4d82-4041-8a4e-d4dc9f2ca4de" />
<img width="1022" height="704" alt="image" src="https://github.com/user-attachments/assets/55ea5913-f4ac-4450-adfe-8f32e491ec10" />
=> 데이터 전처리를 위해 데이터 확인 후 필요 없는 컬럼은 삭제했습니다. <br>
<br>

<img width="720" height="666" alt="image" src="https://github.com/user-attachments/assets/813ccc9a-5ea6-4952-b20b-d02ed886fa0b" />
<img width="1466" height="663" alt="image" src="https://github.com/user-attachments/assets/fe066115-4d6a-445d-b15b-826e99c4f4c8" /><br>
=> 위와 같이 결과를 도출했습니다. 조회 결과 전쟁 관련은 negative, 꽃과 같이 아름다운 것들엔 positive로 분류되는 것을 알 수 있습니다.
