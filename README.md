# 20151016
중간고사 

구글검색시스템
클라우딩컴퓨팅이란? 이런것에 대해 시험에 나온다.

오늘 TSDB 인스톨을 하고 웹브라우저에 TSD를 띄워도 보았다.

wget 은 파일을 다운받을때 씀.
tar은 다운 받은 파일압축을 풀때 씀.

다음시간에는 TSD로 실시간 날씨를 볼 수 있게끔 할 것 이다.

#아까 만든 TSD에 Data Input test(Restful 방법)

                sudo yum install python-setuptools python-setuptools-devel
                sudo easy_install pip
                pip install requests

        vi post_test.py <- py는 파이썬형식으로 만드는것 

        import time
        import requests
        import json

        url = "http://127.0.0.1:4242/api/put"

        data = {
        "metric": "foo.bar",
        "timestamp": time.time(),
        "value": 2015,
        "tags": {
          "host": "mypc"
        }
    }

    ret = requests.post(url, data=json.dumps(data))
    print "ok"

    python post_test.py <- 파이썬 vi가 제대로 작동하는지 확인하는 코드. 
    제대로 작동이 한다면 ok가 뜬다

