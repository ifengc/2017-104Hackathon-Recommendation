# 2017-104Hackathon-Recommendation

104為國內最大工作媒合平台，求職媒合一直是104的服務核心!  
請參賽者利用求職應徵紀錄及工作內容，預測求職者可能會喜歡的工作。
## 活動網址
https://www.104.com.tw/2017hackathon/
## 主題說明
主辦單位於賽前提供參賽者一段特定時間區間內去識別化的行為記錄（user Log），以及千大企業刊登的工作內容做為 Training Data，讓參賽隊伍從中進行學習以找尋出使用者瀏覽應徵模式，以預測求職者可能會喜歡的工作。  
比賽當天，將備有 Testing Data，讓參賽隊伍能夠藉由從 Training Data 得到的瀏覽應徵來預測，主辦單位將會透過計分網址來告知參賽者推算結果之準確率(Precision, Recall, F-measure)，作為評分標準。
## 資料集說明
* 104求職者去識別化行為記錄
    + File: user_log.csv
    + Description：求職者在104網站上瀏覽應徵職務時的行為log
    + Date: 2016-04 ~ 2017-03
    + [Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/user_log_schema.md)
    + [Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/user_log_sample.csv) 
    + 訓練資料集將在賽前以Email通知參賽者
* 公司與職務資料
    + 上市櫃公司與五百大企業
        - File: companies.csv 
        - Decription: 台灣所有上市櫃公司與資本額前五百大企業，共有1147間公司
        - [Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/companies_schema.md)
        - [Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/companies_sample.csv)
        - 訓練資料集將在賽前以Email通知參賽者
    + 職務資料
        - File: job_structured_info.csv, job_description.csv
        - Description: 對每一筆職務結構化的欄位資料與該職務的文字描述
        - Date: 2017/03/29
        - [Job Description Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/job_description_schema.md)
        - [Job Structured Info Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/job_structured_info_schema.md)
        - [Job Description Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/job_description_sample.csv)
        - [Job Structured Info Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/job_structured_info_sample.csv)
        - 訓練資料集將在賽前以Email通知參賽者
    + 職務異動歷史資料
        - File: job_structured_info_{yyyymm}.csv, job_description_{yyyymm}.csv
        - Description: 對每一筆職務結構化的欄位資料與該職務文字描述的修改歷程
        - Date: 2014/03 - 2017/03/31 
        - [Job Description History Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/job_description_history_schema.md)
        - [Job Structured Info History Schema](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/data-schema/job_structured_info_history_schema.md)
        - [Job Description History Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/job_description_2014_sample.csv)
        - [Job Structured Info History Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/job_structured_info_2014_sample.csv)
        - 訓練資料集將在賽前以Email通知參賽者
    + 類目資料
        - File:
            - department.csv [Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/department_sample.csv)
            - district.csv [Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/district_sample.csv)
            - industry.csv [Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/industry_sample.csv)
            - job_category.csv [Sample](https://github.com/104corp/2017-104Hackathon-Recommendation/blob/master/sample-data/job_category_sample.csv)
        - Description: 在職務結構化欄位中的類目對照
        - 訓練資料集將在賽前以Email通知參賽者

## 上傳預測結果
* 預測testing set中求職者對職務是否有apply行為
* 上傳範例：TBA
* 上傳網址：TBA
* Leader Board：TBA

## 評分標準
* 推薦結果 70%
    + 使用F-measure作為評價推薦結果的指標
        - 引用Wiki對Precision和Recall在分類問題上的定義 [Link](https://en.wikipedia.org/wiki/Precision_and_recall)
            + Condition Positive和Condition Negative表示測試資料集中 __實際上__ 使用者對職缺是否有apply行為
            + Prediction Positive和Prediction Negative表示參賽者的模型 __預測__ 使用者對職缺是否有apply行為

        	|                        | Prediction Positive | Prediction Negative |
        	| :--------------------: | :-----------------: | :-----------------: |
        	| __Condition Positive__ | True Positive (TP)  | False Negative (FN) |
        	| __Condition Negative__ | False Positive (FP) | True Negative (TN)  |

            + Precision = TP / (TP + FP)
            + Recall = TP / (TP + FN)
            + F = 2 * Precision * Recall / (Precision + Recall)
* 設計方法 30%（包含簡報內容、演算法設計、資料闡釋與分析等）

## 104開放資料授權條款 
【2017-104-hackathon-dataset】是 2017年104資訊科技Hackathon活動中開放的資料集。當您使用104提供之【2017-104-hackathon-dataset】資料集時，即表示您已閱讀、瞭解並同意接受本授權條款所訂定之所有內容。本授權條款得隨時修訂並公告於本頁面上，修訂後之內容自公告時起生效，授權說明如下：

* 使用者權利：
    + 使用者得自由應用104提供的資料集，產生新的程式、文件、圖表等著作，使用者亦可自由修改104提供的資料集，衍生新的資料集，使用者基於本活動目的範圍的任何使用方式，無須104再為授權。
* 使用者義務：
    + 使用者必須在您的著作或衍生資料集明確標示【2017年104資訊科技Hackathon】為資料來源，與此份說明文件的連結。
    + 使用者違反前項標示義務，視為自始未取得104開放資料之授權，須負擔所有相關之法律責任。
* 使用者規範：
    1. 使用者不可使用可能造成104會員混淆或困擾的商標或名稱，或為任何違反104會員服務條款或本活動授權規範之行為。
    2. 使用者不可違反中華民國法令，或造成第三人發生違反中華民國法令的行為。
    3. 使用者保證不可另為提供他人資料集下載，意即，使用者不得複製一份資料集到您自己的網路服務上供他人下載，但您可以提供他人此份說明文件的連結。使用者同意且了解，若您利用104提供的資料集，開發任何妨礙善良風俗之違法服務或程式工具，104並不為此負擔任何法律連帶責任。
    4. 使用者不得意圖或為任何可能損害104商譽或侵害104資料之任何行為或聲明。
    5. 謝絕競業使用，作任何商業營利或非商業研究分析之用。
    6. 本條款之解釋、效力、履行及其他未盡事宜，以中華民國法律為準據法。
