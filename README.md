# 2017-104Hackathon-Recommendation

104為國內最大工作媒合平台，求職媒合一直是104的服務核心!  
請參賽者利用求職應徵紀錄及工作內容，預測求職者可能會喜歡的工作。
## 主題說明
主辦單位於賽前提供參賽者一段特定時間區間內去識別化的行為記錄（user Log），以及千大企業刊登的工作內容做為 Training Data，讓參賽隊伍從中進行學習以找尋出使用者瀏覽應徵模式，以預測求職者可能會喜歡的工作。  
比賽當天，將備有 Testing Data，讓參賽隊伍能夠藉由從 Training Data 得到的瀏覽應徵來預測，主辦單位將會透過計分綱址來告知參賽者推算結果之準確率(Precision, Recall)，作為評分標準。
## 資料集說明
* 104求職者去識別化行為記錄
    + File: user_log.csv
    + Description：求職者在104網站上瀏覽應徵職缺時的行為log
    + Date: 2016-04 ~ 2017-03
    + [Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/user_log_schema.md)
    + [Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/user_log_sample.csv) 
* 公司與職缺資料
    + 上市櫃公司與五百大企業
        - File: companies.csv 
        - Decription: 台灣所有上市櫃公司與資本額前五百大企業，共有1147間公司
        - [Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/companies_schema.md)
        - [Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/companies_sample.md)
    + 職缺資料
        - File: job_structured_info.csv, job_description.csv
        - Description: 對每一筆職缺結構化的欄位資料與該職缺的文字描述
        - Date: 2017/03/29
        - [Job Description Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/job_description.md)
        - [Job Structured Info Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/job_structured_info.md)
        - [Job Description Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/job_description_sample.csv)
        - [Job Structured Info Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/job_structured_info_sample.csv)
    + 職缺異動歷史資料
        - File: job_structured_info_{yyyymm}.csv, job_description_{yyyymm}.csv
        - Description: 對每一筆職缺結構化的欄位資料與該職缺文字描述的修改歷程
        - Date: 2014/03 - 2017/03/31 
        - [Job Description History Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/job_description_history_schema.md)
        - [Job Structured Info History Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/job_structured_info_history_schema.md)
        - [Job Description History Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/job_description_2014_sample.csv)
        - [Job Structured Info History Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/job_structured_info_2014_sample.csv)
    + 類目資料
        - File:
            - department.csv
            - district.csv
            - industry.csv
            - job_category.csv
        - Description: 在職缺結構化欄位中的類目對照

## 評分標準
* 推薦結果 70%
* 設計方法 30%（包含簡報內容、演算法設計、資料闡釋與分析等）

## 104開放資料授權條款 
