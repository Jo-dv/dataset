dataset 주소
* 3일차
  * 예제
    * https://drive.google.com/file/d/1Je5g4vCWihSN6Qw8irjlv8UhUGr-uiSf/view?usp=sharing
* 4 ~ 5일차
  * 참조  
    * train
        * https://drive.google.com/file/d/1co4YGFnm0VPgW-JeIZjLnurNCeauZs6e/view?usp=share_link
    * test
        * https://drive.google.com/file/d/1chKI1BSex81u52DDEkoBAkDri4DcUmKt/view?usp=share_link
  * 캐글 설문  
    * https://drive.google.com/file/d/1cem-XNqPAjqUdA5bIbn1XX9OMqSrS2bv/view?usp=sharing
  * 당뇨병  
    * https://drive.google.com/file/d/1cgTV6grYybWRwpEFfG80RsUHQENh3rxD/view?usp=share_link
  * 코로나  
    * https://drive.google.com/file/d/1cqctUe_n4oXMIrxe6ChaZbLvE4Tv-B2H/view?usp=share_link
* 6일차
  * 스마트 그리드
    * https://drive.google.com/file/d/1KhmFh8SxCkoiSI-KCic2xtpx1X2Q6r1T/view?usp=sharing
  * 실습 예제
    * 예제 1
      * https://drive.google.com/file/d/1KteGsQNUTm9v_fXNINSywekIdiYuKGcz/view?usp=sharing
      * https://drive.google.com/file/d/1Kt4LgULhNmty-M_PPh0xi0650zkzEThx/view?usp=sharing
    * 예제 2
      * https://drive.google.com/file/d/1KuZ6xs3ovhmSqkNHR8m9Kl_KyonWLkI6/view?usp=share_link
* 7일차
  * 영양소 및 의류 데이터 분석
    * 영양소
      * https://drive.google.com/file/d/1Kh8V6PLTZeaaE9IwLZauyM_L6paWh8Ou/view?usp=share_link
    * 의류 데이터
      * https://drive.google.com/file/d/1LACyLvNMhC64BA-aeC08qVPPI1lP2jfn/view?usp=share_link
      * https://drive.google.com/file/d/1LB0XLwFK3JYwxsrvViODjYRBpTEuaYMf/view?usp=share_link
  * 예제 - 전자상거래(의류시장)
      * https://drive.google.com/file/d/1LLiugidoWp6GUt8DF4ngh5MNXd541jkb/view?usp=share_link
* 8일차
  * 유전자 분석
    * 나방 염기서열
      * https://drive.google.com/file/d/1KI2lgNLDmT7fvhhK7Yii4KyPFENVg1I7/view?usp=share_link
    * 포유류 염기서열
      * https://drive.google.com/file/d/1LgcpRK9hGKElO1hnC21o3CtPI--5SgS1/view?usp=share_link
  * 예제 - 자동차 부품
     * https://drive.google.com/file/d/1LbKAJgxSnm4K9TTXXrkRt5E9RMd6h-dd/view?usp=share_link
 * 9일차
   * 예제
     * ~~https://drive.google.com/file/d/1MA9f_jjiWj4QsSMTTiJtrvAyK2RpjAka/view?usp=share_link~~
     * https://drive.google.com/file/d/1MHixBw5G6JKdm0zj6CevwbqmN5NWlNVj/view?usp=share_link
   * 수집데이터
     * x-o
       * https://drive.google.com/file/d/1M1akvads1sBxuajdhWoon78WQBAd0u2-/view?usp=sharing
       * https://drive.google.com/file/d/1M02sFFrIzskpfOHE59_iupGYQOuCAohw/view?usp=sharing
     * anomaly
       * https://drive.google.com/file/d/1M6NnklOAWr61kGGbqom06iJnTSt7qBfp/view?usp=share_link
     * nasa
       * https://drive.google.com/file/d/1M2zlb7Qi4wj9zLr8tqXluozd3eiIm3Ln/view?usp=share_link
 * 10일차
   * 게임 데이터
     * https://drive.google.com/file/d/1SV0lSf3mlVbb2HP-N5mHBORamvvpSv31/view?usp=share_link
     * https://drive.google.com/file/d/1Sc3JN0udS5mlfsci5oYrtT2L-J5E-TNm/view?usp=sharing
   * 설치 및 실행 intro
     * https://drive.google.com/file/d/1MapUG2WnAvoX8yg6YvXPFW_6TN4hdGLy/view?usp=share_link
   * api
     * RGAPI-1769947f-cee1-4ba9-99a4-a644cd363fc7
     * 농구선수 갓관희

보조 프로그램
* 이진 분류 혼동 행렬 시각화
    * https://drive.google.com/file/d/1KiM56o2YLbg6nIk6V0TPTNA9iT3YKVqg/view?usp=sharing
* 기본 실습 세팅
    * https://drive.google.com/file/d/1KwZ76TID2brWN1ncgJwTIuq1EfcWc4Qj/view?usp=sharing
    
```
from sklearn.metrics import accuracy_score, f1_score, precision_score, recall_score

def get_metrics(y_test, y_predicted):
    display(pd.crosstab(pd.Series(y_test, name='Actual'), pd.Series(y_predicted, name='Predicted')).\
            style.background_gradient(cmap='Reds'))
    
    accuracy = accuracy_score(y_test, y_predicted)
    precision = precision_score(y_test, y_predicted, average='weighted')
    recall = recall_score(y_test, y_predicted, average='weighted')
    f1 = f1_score(y_test, y_predicted, average='weighted')
    
    print(f'\naccuracy \t= {round(accuracy, 2)} \
    \nprecision \t= {round(precision, 2)} \
    \nrecall \t\t= {round(recall, 2)} \
    \nf1-score \t= {round(f1, 2)}')
```

```
puuid = summoner_info['puuid']
count = "100"
url = "https://asia.api.riotgames.com/lol/match/v5/matches/by-puuid/"+ puuid + "/ids?api_key=" + api_key +"&count=" + count
match_ids = requests.get(url).json()

matches = []
for match_id in tqdm(match_ids):
    match = {}
    url = "https://asia.api.riotgames.com/lol/match/v5/matches/"+match_id+"?api_key="+api_key
    result = requests.get(url).json()
    if 'status' in result : continue
    match['매치아이디'] = match_id
    match['게임모드'] = result['info']['gameMode']
    match['매치시간'] = result['info']['gameStartTimestamp']
    my_participants = list(filter(lambda x: x['summonerName']==summoner_name, result['info']['participants']))[0]
    match['챔피언'] = my_participants['championName']
    match['킬'] = my_participants['kills']
    match['데스'] = my_participants['deaths']
    match['어시스트'] = my_participants['assists']
    match['결과'] = '승리' if my_participants['win'] else '패배'
    matches.append(match)
matches = pd.DataFrame(matches)
matches.head()
```
