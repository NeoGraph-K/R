# R 수업자료
## R 1일차
1. R 언어
    1. 통계와 분석에 사용되는 언어
    2. 인터프리터 언어
        1. 인터프리터 vs 컴파일
    3. 객체
        1. 다른 언어에서 변수라고 부르는 공간
        2. 변화하는 데이터를 저장하는 공간
        3. 이름 명명법
            1. 영문자, 숫자, 언더바로 이루어짐
            2. 첫글자는 무조건 영문자
        4. 데이터 할당
            1. A <- B - A 객체에 B 데이터 할당
            2. A -> B - B 객체에 A 데이터 할당
        5. 객체 확인
            1. ls()
            2. objects()
        6. 객체 제거
            1. rm(객체이름)
    4. 객체 타입
        1. 실수 - 소수점이 있는 숫자
        2. 문자열 - "글자가 들어있는 배열"
        3. 논리값 - TRUE or FALSE
        4. 벡터 - c(1,2,3,4) - 같은 자료형을 가진 스칼라 값의 나열
            1. 실수 벡터의 경우 A:B 형태로 제작 가능
            2. 실수 벡터의 경우 A:B 로 제작시 A, A + 1, A + 2, ... , B - 1, B 까지 제작
            3. 대괄호를 이용하여 벡터중 한개의 데이터에 접근 가능
            4. 대괄호 사용시 1, 2 인덱싱 필요
        5. 행렬 - matrix(벡터, nrow=행,ncol=열) - 다른 자료형을 가진 스칼라 값의 나열
            1. 3차원 이상 확장 - 배열(Array)
            2. 1차원 연관 - 리스트(List)
            3. 같은 항목 그룹 - 팩터(Factor)
            4. 2차원 자료구조로 저장 - 데이터프레임(DataFrame)
    5. 산술 연산자
        1. + - 덧셈
        2. - - 뺄셈
        3. * - 곱셈
        4. / - 나눗셈
        5. %/% - 정수 나눗셈
        6. %% - 나머지
        7. ^ - 제곱승
    6. if ~ else
        1. 조건문
        2. 다른 언어와 동일하게 True, False로 if, else가 선택 실행
    7. while
        1. 반복문
        2. 다른 언어와 동일하게 True, False로 실행 여부 선택
    8. for
        1. 반복문
        2. 다른 언어와 달리 괄호 안이 (객체명 in 벡터) 방식으로 벡터의 데이터를 한개씩 할당하여 사용하는 for-each 방식
    9. break, next
        1. break - 반복문의 모든 내용 중지
        2. next - 반복문의 모든 내용 무시 및 다음 반복으로 이동
2. R Studio
    1. Console - 기본 R 이 실행되는 콘솔창
    2. Environment - 할당된 객체들의 목록을 확인하는 공간
    3. History - 이전에 실행된 명령어 확인하는 공간
    4. Connections - DB등 외부 장치와 연결을 확인하는 공간
    5. Files - 파일 디렉토리를 확인하는 공간
    6. Plots - 시각화한 데이터를 눈으로 확인하는 공간
    7. Packages - 설치, 포함한 패키지를 확인하는 공간
    8. Proejct - R 언어를 활용한 데이터 사용이 겹치지 않도록 따로 공간을 할당하는 방식
    9. R Script - R 언어의 명령어를 미리 적어두는 메모장
    10. Ctrl + Enter(Return) - 현재 커서가 있는 줄 혹은 드래그(선택)한 명령어를 전체 실행
    11. Ctrl + Alt + R - 현재 R Script 전체 명령어 실행
    12. 붓모양 - 데이터 제거
3. 기초 사용법
    1. 변수에 데이터 할당
    2. 변수에 들어있는 데이터에 따라 다른 결과를 plot으로 화면에 뿌려보기
## R 2일차
1. 함수
    1. 수학적 함수
        1. sin(값), cos(값), tan(값) - 삼각함수 값
        2. log(값) - 자연 로그
        3. log10(값) - 상용 로그
        4. floor(실수) - 버림
        5. ceiling(실수) - 올림
        6. round(실수) - 반올림
        7. sqrt(값) - 제곱근
        8. min(벡터) - 최소
        9. max(벡터) - 최대
        10. mean(벡터) - 평균
        11. sum(벡터) - 합계
        12. sd(벡터) - 표준 편차
        13. runif(개수, 최소, 최대) - 난수 N개를 생성(초과,미만)
        14. 이외에도 매우 많은 기본 함수가 내제
    2. 사용자 정의 함수
        1. 특정 동작을 미리 만들어둔 소스
        2. function(입력값){코드; return(결과값)} - 함수 제작 방법
        3. 함수도 객체에 저장해서 사용
        4. 함수를 다른 객체에 복사하여 사용 가능
        5. function(입력값) 계산식 - 다른 코드 없이 계산식을 결과물로 돌려주는 함수
2. 패키지
    1. 미리 만들어진 모듈화 코드
    2. npm, pip, maven 과 같이 설치 후 사용
    3. install.packages("패키지명")으로 설치
    4. library(패키지명)으로 사용
    5. detach("package:패키지명")으로 패키지 언로드
    6. 유명한 패키지
        1. ggplot2 - 데이터 시각화
        2. googleVis - 구글 차트 툴
        3. RSQLite - DB 연결 툴
        4. dplyr - 데이터 핸들링
        5. tidyr - 데이터 레이아웃 변경
        6. stringr - 문자열 제어 및 정규 표현식
        7. lubridate - 날짜 및 시간
        8. randomForest - 머신 러닝 랜덤 포레스트
        9. multcomp - 다중 비교 툴
        10. caret - 회귀 분석 및 분류 모델 트레이닝 툴
3. 데이터 구조
    1. 스칼라
        1. 데이터가 1개인 벡터
    2. 벡터
        1. 동일한 데이터 타입을 가진 묶음
        2. 사용법 - c(1,2,3,4)
        3. 벡터[length(벡터)+1] <- 데이터 - 벡터 마지막에 데이터 추가
        4. 벡터[인덱스] <- NA - 데이터 삭제
        5. 벡터 %in% 벡터 - 오른쪽 벡터에 왼쪽 벡터 값이 있는지 T,F로 벡터타입 반환
        6. table(벡터, 벡터, ...) - 동일 데이터의 범주를 통계한 분할표 추출
    3. 펙터
        1. 범주형 데이터
        2. 특정 데이터가 특정 범주에 해당하는지 판단하는 형태
        3. factor(데이터 벡터, 범주 벡터)
        4. 범주에 없는 데이터는 N/A 형태로 나옴
        5. ordered로 순서형 자료를 제작 가능
        6. nlvels(팩터) - 범주 개수
        7. levels(팩터) - 범주 목록
        8. factor(벡터) - 정해진 값이 범주가 됨
        9. levels(팩터) <- 벡터 - 팩터의 범주를 수정, 먼저 삽입된 데이터가 범주에 포함 안될 경우 수정
    4. 리스트
        1. 서로 다른 데이터 타입을 가진 묶음(딕셔너리)
        2. 사용법 - list(key=데이터,key=데이터,...)
        3. list['키'] - 키값과 해당 키값의 데이터 추출
        4. list[['키']] - 해당 키값의 데이터 추출
        5. 키값 대신 인덱스 사용 가능
        6. list$키 - 키값 추출
        7. list(키=벡터,키=벡터) 방식으로 특정 키값의 데이터 저장 가능
            1. 벡터 타입을 저장시 list$키[2] 방식의 인덱싱이 가능
            2. 벡터 타입을 저장시 list['키'][2] 방식의 인덱싱 불가능, key-value 타입을 반환하므로
        8. list$키 <- 데이터 - 키 추가
            1. 중간에 키를 추가 못함
            2. 추가된 키는 마지막에 추가
        9. list$키 <- NULL - 키값에 NULL을 넣어 키 삭제
    5. 행렬
        1. 동일한 데이터 타입을 행렬로 저장하는 묶음
        2. 사용법 - matrix(벡터,nrow=행,ncol=열,byrow=데이터삽입순서)
        3. byrow값에 따라 열먼저 삽입할지 행먼저 삽입할지 구분
        4. dimnames(행렬) <- 리스트(행벡터,열벡터) - 행렬에 행렬 이름 지정, 리스트 사용해야하는 불편함에 자주 이용되지 않음
        5. rownames(행렬) <- 벡터 - 행이름 지정
        6. colnames(행렬) <- 벡터 - 열이름 지정
        7. 색인
            1. 숫자
                1. 행렬[행,열] - 행,열 데이터 추출
                2. 행렬[-행,] - -행 제외 데이터 추출
                3. 행렬[,-열] - -열 제외 데이터 추출
            2. 슬라이스
                1. 행렬[숫자:숫자,] - 범위 데이터 추출
            3. 벡터
                1. 행렬[행,벡터] - 행의 특정 열만 추출
                2. 행렬[벡터,열] - 열의 특정 행만 추출
                3. 행렬[벡터,벡터] - 특정 행의 특정 열만 추출
            4. 이름
                1. 행렬[행,벡터(열이름)] - 특정 행의 특정 이름 열 추출
                2. 행렬[벡터(행이름), 열] - 특정 열의 특정 이름 행 추출
        8. 행렬 조건
            1. 행렬 전체 데이터의 조건 판단
            2. 행렬 비교연산자 데이터 - 동일한 크기의 행렬에 T,F 값으로 추출
            3. 행렬[행렬 비교연산자 데이터] - 조건에 맞는 데이터 벡터로 추출
            4. 행렬[((행렬 추출) 비교 추출),] - 특정 조건에 맞는 데이터만 추출
        9. 행렬 준비
            1. rep(값, 개수) - 특정값을 특정 개수만큼 가진 벡터
            2. matrix(rep(값,개수),nrow=행개수)
        10. 행렬 연산
            1. 행렬 연산 스칼라(값) - 각 데이터의 산술 연산 가능
            2. 행렬 연산 행렬 - 크기가 같은 서로 다른 두 행렬 산술 연산 가능
            3. 행렬 연산은 크기가 다를시 연산 불가능
            4. 행렬 %*% 행렬 - 행렬 곱은 크기가 달라도 가능
        11. 전치 행렬
            1. 행과 열 교환
            2. t(행렬)
        12. 행렬 크기
            1. nrow(행렬) - 행 크기
            2. ncol(행렬) - 열 크기
            3. dim(행렬) - 행,열 크기
            4. dim(행렬) <- 벡터(행,열) - 행렬 크기 변경
        13. 행렬 결합
            1. rbind(벡터 or 행렬,벡터,...) - 각 벡터를 행으로 결합
            2. cbind(벡터 or 행렬,벡터,...) - 각 벡터를 열로 결합
    6. 배열
        1. 동일한 데이터 타입을 가진 다차원 구조
        2. array(벡터, 차원벡터)
        3. array(벡터) - 일반 벡터와 동일한 구조
        4. array(벡터) 이후 dim(배열) <- 벡터 방식으로 차원 확장 가능
        5. 행렬과 동일한 색인 사용
    7. 데이터 프레임
        1. 서로 다른 데이터 타입을 가지는 행렬 구조
        2. 사용법 - data.frame(열이름=벡터, 열이름=벡터..., stringAsFactors=문자열을 팩터로 저장하는지 여부)
            1. stringAsFactors는 기본 True
            2. stringAsFactors가 True 이면 문자열이 무조건 팩터로 저장, row 추가 불가능
        3. 행렬과 비슷 하지만 행번호가 자동 부여
        4. str(프레임) - 데이터 프레임 구조 확인
        5. rbind(프레임, 벡터) - 행추가
            1. 문자열 타입의 경우 stringAsFactors로 인하여 팩터타입이 되는 경우 없다면 NA 로 추가
        6. 프레임$열이름 <- factor(프레임$열이름) - 특정 열을 팩터로 변경
        7. 프레임$열이름 <- as.character(프레임$열이름) - 특정 열을 팩터에서 데이터 타입으로 변경
        8. 프레임$열이름 <- 벡터 - 특정 열(칼럼) 추가, 기본 팩터 타입이 안됨
        9. 행렬과 동일한 방법으로 행렬 이름 지정 가능
        10. 프레임[색인, drop=F] - 데이터 추출시 차원 축소가 일어나는데 차원 축소를 막는 기능
        11. head(프레임, 크기) - 데이터의 처음 일부분만 추출(대용량 데이터 사용시 유용)
        12. tail(프레임, 크기) - 데이터의 마지막 일부분만 추출
        13. View(프레임) - 데이터를 뷰어로 출력
4. 인덱싱
    1. 데이터 추출 방법
    2. 필요한 데이터 구조에서 필요한 데이터만 추출하는 방법
## R 3일차
1. 외부 데이터 임포트
    1. TXT
        1. read.table("파일경로", header=F, skip=0, nrows=-1, sep="", encoding="EUC-KR or CP949", fileEncoding="utf-8")
        2. header - 1행이 변수명인지 아닌지 판단
        3. skip - 특정 행까지 제외 후 추출
        4. nrows - 특정 행까지 추출
        5. sep - 데이터 구분 문자
        6. encoding - R 코드표 지정
        7. fileEncoding - 파일 코드표 지정
        8. 데이터 프레임 타입으로 추출
    2. CSV
        1. read.csv("파일경로")
        2. TXT와 비슷하지만 자동으로 1행을 칼럼명으로
    3. XLSX
        1. install.packages("readxl") - 엑셀 패키지
        2. read_excel("파일경로", sheet=시트)
2. 데이터 특성 파악
    1. head, tail - 데이터의 일부분만 출력
    2. dim - 행, 열 개수 확인
    3. str, int - 데이터 속성 확인
    4. summary - 데이터 요약 통계 확인
3. 행렬명 변경
    1. names(데이터), rownames(데이터), colnames(데이터) - 데이터의 이름 추출
    2. names(데이터) <- 벡터 - 데이터의 이름 변경
4. 파생 변수
    1. 데이터 프레임에 이미 존재하는 데이터를 이용하여 새로 추가하는 데이터
    2. 데이터프레임$추가열이름 <- 데이터공식 방식으로 추가
    3. 데이터프레임$열이름 연산자 데이터프레임$열이름 방식으로 일괄 연산 가능
    4. ifelse
        1. 특정 변수의 조건을 토대로 파생 변수의 데이터를 만드는 기능
        2. ifelse(데이터프레임$열이름 조건절, T, F) 를 통하여 새로운 파생 변수 제작
5. 데이터 추출
    1. 인덱싱
        1. 데이터프레임[데이터프레임$열이름 조건절,] - 조건에 맞는 행만 추출
        2. 인덱싱 방식은 T/F 방식으로 추출하기 때문에 NA 값 필터링 불가 및 대용량 속도 저하
        3. 두개 이상의 조건일 경우 &(AND), |(OR) 사용
    2. which
        1. 데이터프레임[which(데이터프레임$열이름 조건절), ] - 조건에 맞는 행만 추출
        2. True인 데이터만 다루므로 인덱싱보다 빠른 속도
        3. 두개 이상의 조건일 경우 intersect(AND), Union(OR) 사용
            1. intersect(which(),which(), ...)
## R 4일차
1. 데이터 전처리
    1. 데이터를 내가 원하는 형태로 가공하는 작업
    2. dplyr, tidyr, reshape2, stringr 등 여러가지 패키지 지원
    3. dplyr
        1. 데이터 프레임 처리에 특화된 전처리 패키지
        2. 파이프 라인 연산자(%>%) 지원
            1. 파이프 라인은 dplyr 패키지 함수 이용시 데이터 프레임 중복 작성 최소화
            2. 데이터프레임 %>% 함수명(옵션) 같은 방식으로 함수에서 기본적으로 넣는 데이터프레임을 안넣어도 되도록 제어
        3. rename
            1. 원하는 열 이름 변경
            2. rename(데이터프레임, 변경후열이름=기본열이름, ...)
        4. mutate
            1. 파생 변수를 일괄적으로 생성
            2. mutate(데이터프레임, 추가변수명=변수식, ...)
            3. 파이프 라인 연산자 이용시 변수식 부분에 데이터프레임명 안적어도 동작
        5. select
            1. 원하는 열만 추출
            2. select(데이터프레임, 열이름, 열이름, ...) - 열이름 추출
            3. select(데이터프레임, -열이름) - 특정 열 제외
            4. select(데이터프레임, 열이름:열이름) - A ~ B열까지 추출
        6. filter
            1. 원하는 행만 추출
            2. filter(데이터프레임, 조건)
            3. 논리 연산을 이용하여 여러 조건에 맞는 데이터만 추출 가능
        7. bind_rows
            1. 두 데이터 프레임의 열이 동일한 경우 행을 추가하는 기능
            2. bind_rows(데이터프레임,데이터프레임)
            3. 합치는 데이터 프레임의 열이름과 열 타입이 동일해야 가능 - character, factor 주의
        8. arrange
            1. 특정 열을 기준으로 정렬
            2. arrange(데이터프레임, 칼럼명) - 기본 오름차순 정렬
            3. arrange(데이터프레임, desc(칼럼명)) - 내림차순 정렬
            4. 여러개의 칼럼명을 넣으면 여러 변수를 기준으로 정렬
        9. summarise
            1. 총합, 평균등 요약 통계량 추출
            2. summarise(데이터프레임, 열이름=통계값)
            3. 데이터프레임 %>% summarise(열이름=통계값)
            4. mean(평균), min(최소), max(최대), sum(총합), median(중앙), sd(표준편차), n(빈도) - 자주 사용되는 요약 통계 함수
        10. group_by
            1. 동일 데이터 별로 그룹화하여 묶는 기능
            2. summarise와 같이 사용하는 편
            3. 데이터프레임 %>% group_by(열이름) %>% summarise(열이름=통계값, ...)
## R 5일차
1. 데이터 전처리
    1. left_join
        1. 두 데이터 프레임을 동일한 열을 기준으로 열 병합
        2. left_join(기준데이터프레임,병합데이터프레임,by='기준 열이름')
        3. 기준이될 열이름과 동일한 열이름 필요
        4. 한번에 2개의 데이터 프레임만 병합 가능
        5. cbind는 열의 길이(데이터 개수)만 동일하면 합쳐지지만 left_join은 기준 열을 제외한 열들이 기준 열의 위치에 맞춰서 병합
        6. 기준 열과 일치하는 데이터가 있다면 두 프레임의 행 개수가 다르더라도 병합 가능
        7. 동일 집합이 아니어도 병합가능, 없는 데이터는 NA 결측치 처리
    2. distinct
        1. 데이터 중복 제거
        2. distinct(데이터프레임,중복제거열,...)
        3. 중복 제거열에 있는 중복된 데이터 삭제
    3. row_number
        1. 행에 번호 매기기
        2. row_number(데이터프레임)
        3. 행에 번호를 매기는 파생변수에 유용
        4. group_by와 사용시 그룹별 순서 매기기 가능
    4. tally
        1. 행 개수 세기
        2. tally(데이터 프레임)
        3. 전체 데이터의 개수를 구할때 유용
2. 데이터 정제
    1. NA(결측치)
        1. 데이터가 없는 결측치
        2. is.na(벡터)를 이용하여 결측치는 T 아니면 F로 통계
        3. table(is.na(벡터))를 이용하여 결측치 개수 체크 가능
        4. summarise 통계 함수에서 na.rm=T를 이용하여 결측치 제외 계산 가능 단, 결측치가 의미가 있는경우가 있으므로 주의
        5. na.omit(데이터프레임) - 결측치가 한개 이상 있는 행을 제거하는 기능
    2. 이상치
        1. 데이터의 범위를 벗어난 데이터
        2. ifelse를 이용하여 벗어난 데이터를 NA(결측치) 처리
        3. ifelse(조건, NA, 원본)
        4. 의도된 또는 상황변화에 의한 이상치가 나올 수 있으므로 유의
2. 데이터 샘플링
    1. 무작위 데이터 추출
    2. sample(x,size,replace,prob)
    3. x는 추출할 데이터 벡터
    4. size는 추출할 데이터 총 개수
    5. replace는 T,F로 데이터 추출 후 복원할지 여부(복원 안할시 중복 불가)
    6. prob은 x와 동일한 크기의 벡터, 각 데이터의 확률 분포
## R 6일차
1. 그래프
    1. plot
        1. 두개의 숫자 벡터를 이용하여 점 그래프
        2. plot(x축,y축,type,xlim,ylim,xlab,ylab,main,sub,bg,col)
        3. type으로 그래프 모양 지정(p,l,b,o,h,s)
        4. xlim,ylim으로 상한,하한 지정
        5. main,sub으로 메인 서브 제목 지정
        6. bg,col으로 배경, 그래프 색상 지정
        7. par(mfrow=c(x,y))로 여러개의 그래프를 한 화면에 표시 가능
    2. abline
        1. 그래프 겹쳐 그리기
        2. 그래프에 직선 추가
        3. abline(a,b) - 절편 a, 기울기 b 직선
        4. abline(h=y) - 수평선
        5. abline(v=x) - 수직선
        6. abline(lm(x~y)) - 회귀 분석 결과선
    3. dotchart
        1. 한개의 벡터 데이터를 진행 상황별로 그리는 점 그래프
        2. dotchart(벡터,labels,cex,main)
        3. labels에 데이터 개수와 동일한 이름을 넣어 각 데이터의 이름 설정
        4. cex를 이용하여 그래프의 폰트 조정
        5. 그 외에는 plot과 동일
    4. barplot
        1. 한개의 데이터를 막대로 표현하는 그래프
        2. barplot(데이터, horiz=T,...)
        3. horiz를 통해 세로 막대를 가로 막대로 변경 가능
        4. names.arg를 이용하여 각 데이터의 이름 부여 가능
        5. 데이터가 벡터가 아닌 여러행의 데이터일 경우 누적 막대 그래프로 변경
        6. beside=T 를 이용하여 그룹 막대 그래프로 변경 가능
        7. legend=rownames(데이터) 를 이용하여 각 데이터 그룹의 명칭 지정 가능
        8. 그외 에는 plot과 동일
    5. pie
        1. 벡터 데이터의 비율을 구하는 원 차트
        2. pie(벡터,labels=이름)
## R 7일차
1. 텍스트 마이닝
    1. 무작위한 문장들 사이에서 유의미한 단어를 찾는 기술
    2. 영어 패키지 tm, NLP, stringr 사용
        1. paste(문장들, collapse='공백') - 문장 합치기
        2. gsub(patter='\\\\W',replace='공백',문장) - 구두점 제거
        3. tolower(문장) - 데이터 소문자화
        4. stopwords - 불용어(단어가 아닌 접속사 등)
        5. removeWords(문장,불용어벡터) - 특정 문자 제거
        6. stripWhitespace(문장) - 공란 제거
        7. str_split(문장,pattern='\\\\s+') - 문장을 단어의 조각으로 나열 및 "" 뒤 공백 띄우기
        8. unlist(리스트) - 리스트를 벡터로
    3. setwd('위치') R의 경로 변경
    4. list.files() 현재 위치의 파일 목록 벡터로 반환
    5. readLines('파일') 내용을 행단위로 읽어 벡터로 반환
    6. apply
        1. 집합 데이터의 각 데이터 별 함수 적용 결과
        2. apply - array(or matrix)형 데이터를 넣으면 array를 반환
        3. lapply - list or vector형 데이터를 넣으면 list를 반환
        4. sapply - list or vector형 데이터를 넣으면 vector를 반환
    7. 전처리
        1. 원하는 단어 추가
        2. dplyr::filter(데이터셋)을 이용하여 필요한 데이터만 추출
        3. gsub - 불용어 처리
            1. gsub(find,replace,데이터셋) - 단어를 찾아서 변경 ('')로 변경시 단어 제거 가능
            2. 정규표현식을 이용한 제거 가능
            3. '[~!@#$%^&()_+=?<>]' 를 이용한 제거
            4. '\\\\[' 를 이용한 제거
            5. '[ㄱ-ㅎ]'를 이용한 제거
            6. '(ㅜ|ㅠ)' 제거
            7. '\\\\d+' 숫자 삭제
2. 워드 클라우드
    1. 단어의 빈도수에 따라 크기별 구름으로 그려주는 다이어그램
    2. wordcloud 패키지 사용
    3. RColorBrewer 패키지 사용(R의 기본 원색이 아닌 추가 색 사용)
        1. display.brewer.all() - 전체 색상
        2. brewer.pal(개수, 세트이름)
        3. windowsFonts(font=windowsFont('폰트명'))
    4. wordcloud(단어벡터,빈도벡터,...) 으로 사용
        1. scale=c(10,1) 최고빈도 폰트와 최소빈도 폰트
        2. minfreq=n 출력될 최소빈도 수
        3. maxwords=n 출력될 최대빈도 수(inf:무제한)
        4. random.order=T,F 무작위로 넣을지, 아니면 순서대로 할지
        5. random.color=T,F 무작위로 넣을지, 아니면 빈도순으로 할지
        6. rot.per=n 회전각도로 출력되는 비율
        7. colors=c(색,...) 가장 작은 빈도부터 가장 큰 빈도까지 단어 색상
        8. family=폰트 폰트 지정
## R 8일차
1. Linear Regression - 선형 회귀 분석
    1. 벡터 데이터 2개 이상 있을시 서로의 데이터가 영향을 주는지 분석하는 방법
    2. Y(종속) = b0 + b1 x X(독립) + e 방식으로 단순 선형 회귀 분석 가능
    3. lm함수로 선형 회귀 분석 데이터 추출
    4. lm(y ~ x, data=) 방식으로 제작
        1. lm(y ~ ., data= 데이터셋)으로 여러개의 데이터를 가진 다중 선형 회귀 분석 가능
    5. 나오는 데이터의 coefficients의 intercept 부분이 b0(절편), 변수 부분이 b1(기울기)
        1. coef 함수로 회귀 계수 추출 가능
        2. fitted 함수로 계산된 종속 값 추출 가능
        3. residuals 함수로 잔차(오차값)을 추출 가능
        4. confint를 이용하여 신뢰 구간을 추출 가능
    6. predict.lm(모델, newdata=data.frame(독립변수명=데이터)) 로 예측 값 구하기 가능
        1. interval='confidence' 옵션을 넣어 상한과 하한을 포함한 신뢰구간 테스트 가능
        2. interval='prediction' 옵션을 넣어 오차를 포함한 상한과 하한을 테스트 가능
    7. summary를 통해 모델 평가 가능
        1. Residuals로 잔차 통계
        2. Coefficients로 계수의 통계적 유의성
            1. Pr이 0.05보다 작다면 유의미 하지만 아니라면 통계적으로 0으로 봐야함
            2. *이 붙어있으면 0.05보다 작고 아니면 의미가 없음
        3. F-statistic으로 모델이 얼마나 의미있는지
            1. p-value가 0.05보다 작으면 의미가 있는 모델
    8. plot으로 모델 진단 그래프 추출 가능
        1. par(mfrow=c(2,2))로 한눈에 모든 데이터 파악
## R 9일차
1. Decision Tree - 의사 결정 나무
    1. 데이터를 독립변수의 범위별로 구분하여 구분 예측하는 분류법
        1. 연속성이 있는 데이터가 아닌 선택이 가능한 데이터셋중 독립변수의 영향을 체크하여 예상되는 데이터를 선택하는 기법
        2. 부모 노드와 자식 노드로 구분
        3. 부모 노드에서 독립변수에 의하여 구분될때 구분되는 기준이 분기기준
        4. 종속변수의 분포가 잘 구분되면 순수도가 높음 낮으면 불순도가 높음
        5. 자식노드로 진행시 순수도가 높아져야 함
        6. 분리기준은 카이제곱, 지니지수 등 여러 지표로 생성
        7. 정지 규칙을 이용하여 순수도를 높이기 위해 자식이 많이 생성되는 과적합 방지
        8. 순수도를 높이기 위해 가지치기
    2. rpart 패키지 이용
        1. iris 데이터셋 이용
        2. rpart.plot 함수를 이용하여 의사 결정 나무 모델 출력
    3. rpart 사용법
        1. rpart(formula, data, method) 방식으로 간결 사용
        2. weights, subset, na.action, model, x, y, params, control, cost 등의 옵션은 따로 연구
        3. formula는 선형 회귀법에 사용했던 종속 ~ 독립 방식으로 제작
        4. formula는 종속 ~ . 으로 전체 데이터 이용 가능
        5. data에 전체 데이터가 들어있는 데이터 프레임 추가
        6. method에 평가 방식 선정
            1. anova,poisson,class,exp,dist,mrt,user
    4. rpart.plot 사용법
        1. rpart.plot(모델) 방식으로 출력
        2. summary(모델) 방식으로 모델 데이터 출력
            1. 모델 데이터중 complexity param은 복잡도(cp)
                1. cp는 복잡도로 0.01보다 작으면 더이상 분기가 불가능
            2. predicted class를 통하여 이 노드에 도착한 데이터의 분류 확인 가능
            3. class counts를 이용하여 학습 데이터가 이 노드에서 어떠한 분포를 가졌는지 확인 가능
            4. expected loss를 이용하여 현재 선택에서 잘못된 데이터의 분포 확인 가능
            5. P(node)를 이용하여 현재 노드에 들어온 데이터가 전체 데이터의 분포 확인 가능
            6. probabilities를 이용하여 현재 노드에 들어온 데이터의 분포 확인 가능
            7. left son, right son을 이용하여 노드의 분기에서 나뉘는 데이터 개수 확인 가능
    5. printcp 사용법
        1. 학습된 모델의 복잡도를 확인하는 기능
        2. printcp(모델)
            1. plotcp(모델) 로 cp구조를 그래프화 가능
        3. xerror가 가장 적은것이 최적의 cp
        4. plotcp의 점선(xerror 최하 + 표준편차 xstd를 MIN + 1SE)이하는 비슷한 cp라고 가정
    6. prune 사용법
        1. 학습된 모델을 기준 복잡도로 다시 학습
        2. prune(모델, cp=기준복잡도)를 이용하여 다시 학습
    7. predict 사용법
        1. 학습된 모델을 기준으로 데이터의 예측
        2. predict(모델, 데이터, type='분류방식')으로 예측
            1. 데이터는 총데이터에서 sample로 학습 데이터를 잘라서 가져왔을 경우 총데이터[-학습데이터] 방식으로 예측 데이터를 추출 가능
        3. table을 이용하여 정오분류표 작성 가능
            1. table(예측데이터정답, 예측값)을 이용하여 정분류 체크 가능
            2. 대각 원소가 정분류 데이터이며 그외에는 오분류로 체크
            3. 총데이터$예측열[-학습데이터] 방식으로 정답 추출 가능
            4. sum(정오분류표[row(정오분류표)==col(정오분류표)])/sum(정오분류표)를 이용하여 정분류율 확인 가능
            5. 1-정분류율을 이용하여 오분류율 확인 가능
## R 10일차
1. Clustering - 군집 분석 (K-Means)
    1. 데이터의 군집을 분석하여 분류 예측하는 방식
    2. 데이터간의 거리를 계산하여 거리가 가까운 데이터끼리 군집을 묶어 그룹화 하는 기법
        1. A - B는 B 에서 A에 도달하기 위한 거리데이터
        2. 차원이 많아져도 동일하게 거리 구하기 가능
        3. a^2 + b^2 = c^2 의 거리 구하기 기능을 이용하여 다 차원 거리 구하기 가능
    3. 군집 분석은 독립변수의 척도에 매우 민감하므로 표준화 후 사용
        1. scale로 표준화(데이터의 평균을 기준으로 데이터 조정)
        2. scale(데이터,center=T,scale=T)로 사용
        3. center는 데이터의 거리를 구한 후 평균 값을 빼서 중앙을 0으로 초기화
        4. scale옵션은 center가 F일 경우 생략되며 사용될 경우 평균을 뺀 후에 표준편차로 나눔
        5. data.frame(scale(데이터셋))
    4. 군집 분석에는 여러가지 방법이 있지만 k-means 방식으로 제작
        1. means -> 평균거리를 이용한 군집 분석
        2. k -> 군집 개수
    5. 군집분석 해석을 위해 군집의 중심 좌표 분석
        1. kmeans(데이터,centers=k개수)
        2. 군집분석모델$centers로 중심좌표 확인 가능
        3. centers로 나온 중심좌표는 표준화 한 후의 데이터의 중심 좌표
        4. cluster값으로 각 데이터 행의 군집 그룹 번호 데이터 확인 가능(벡터)
        5. dplyr패키지의 group_by로 cluster별 그룹화 후 mean 평균을 원본 데이터에서 구하면 원본 데이터의 중심 좌표 확인 가능
    6. 군집도 독립변수별 평행 좌표 그래프 통계
        1. 여러개의 데이터로 군집분석을 했을때 각 독립변수들의 관측치가 군집별로 어떻게 구성되는지 파악하는 그래프
        2. GGally 패키지 이용
        3. ggparcoord함수 이용
        4. ggparcoord(data=데이터셋,columns=c(1:독립변수개수),groupColumn='그룹화할열이름',scale='std')로 사용
        5. ggparcoord에 넣는 데이터 셋은 오리지널 데이터에 as.factor로 분류화한 kmeans 결과물의 cluster를 추가한 데이터셋을 이용
            1. origin$cluster <- kmeans()$cluster
        6. groupColumn은 군집 분석용인 cluster로 고정
        7. scale은 표준화 한 이후 데이터일 경우 안적어도 되지만 표준화가 안된 데이터의 경우 'std'를 넣으면 자동으로 표준화
    7. 군집별 산점도를 통한 군집 통계
        1. 2차원 데이터로 축소 후 통계
        2. factoextra 패키지의 fviz_cluster함수를 이용한 방법
            1. fviz_cluster 함수는 군집 데이터 통계 그래프 함수
            2. fviz_cluster(모델,원본스케일한데이터, ellipse.type='norm') 으로 사용
            3. dim1, dim2는 각 방향이 차지하는 분산 데이터의 양