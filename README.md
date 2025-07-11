# 課程介紹

本專案示範如何在Spring應用中配置並使用單一數據源，重點涵蓋JDBC操作與Spring Boot自動配置的使用方式。透過實戰範例，展示如何快速搭建數據庫連接，並執行基本的SQL查詢。

本課程適合希望掌握Spring數據源配置與JDBC操作的Java後端工程師，幫助你理解Spring Boot自動配置的原理與手動配置的差異，提升開發效率與靈活性。

## 專案介紹

- 使用 [start.spring.io](https://start.spring.io/) 生成的Spring Boot專案骨架。
- 集成H2內存數據庫，方便快速測試與開發。
- 演示Spring Boot自動配置DataSource、Transaction Manager與JdbcTemplate。
- 提供非Spring Boot環境下手動配置數據源的示例。
- 支持通過`schema.sql`與`data.sql`初始化數據庫結構與數據。
- 使用Spring Boot Actuator查看自動配置的Bean。

## 專案結構

- `src/main/java`：Java程式碼，包括入口類與數據源配置。
- `src/main/resources`：配置文件及SQL初始化腳本。
- `pom.xml`：Maven專案配置文件。

## 快速開始

1. 克隆專案：
    
    ```
    # 自動配置數據源專案
    git clone https://github.com/SpringMicroservicesCourse/datasource-demo
    cd datasource-demo
    # 手動配置數據源專案
    git clone https://github.com/SpringMicroservicesCourse/pure-spring-datasource-demo
    cd pure-spring-datasource-demo
    ```
    
2. 編譯並打包：
    
    ```
    mvn clean package -DskipTests
    ```
    
3. 運行應用：
    
    ```
    java -jar target/datasource-demo-0.0.1-SNAPSHOT.jar
    ```
    
4. 訪問Actuator端點查看Bean：  
    打開瀏覽器，訪問 [http://localhost:8080/actuator/beans](http://localhost:8080/actuator/beans)
    
5. 查看日誌輸出，確認JdbcTemplate查詢結果。
    

## 進階說明

- Spring Boot自動配置會根據依賴自動創建DataSource、Transaction Manager與JdbcTemplate。
- 支持自動執行`schema.sql`與`data.sql`初始化數據庫。
- 手動配置示例展示如何在非Spring Boot環境下使用DBCP2連接池與Spring JDBC。
- Lombok插件需在IDE中安裝並啟用Annotation Processing。
- H2資料庫建表語法需使用`GENERATED BY DEFAULT AS IDENTITY`或`GENERATED ALWAYS AS IDENTITY`，避免啟動錯誤。

## 參考資源

- [Spring Boot 官方網站](https://spring.io/projects/spring-boot)
- [start.spring.io](https://start.spring.io/)
- [Spring Boot Actuator](https://docs.spring.io/spring-boot/docs/current/reference/html/actuator.html)

## 授權說明

本專案採用 MIT 授權條款，詳見 LICENSE 檔案。 

## 關於我們

我們主要專注在敏捷專案管理、物聯網（IoT）應用開發和領域驅動設計（DDD）。喜歡把先進技術和實務經驗結合，打造好用又靈活的軟體解決方案。近來也積極結合 AI 技術，推動自動化工作流，讓開發與運維更有效率、更智慧。持續學習與分享，希望能一起推動軟體開發的創新和進步。

## 聯繫我們

若有任何問題、合作或想了解更多，歡迎透過以下管道與我們聯繫：

- FB 粉絲頁：[風清雲談 | Facebook](https://www.facebook.com/profile.php?id=61576838896062)
- LinkedIn：[linkedin.com/in/chu-kuo-lung](https://www.linkedin.com/in/chu-kuo-lung)
- YouTube 頻道：[雲談風清 - YouTube](https://www.youtube.com/channel/UCXDqLTdCMiCJ1j8xGRfwEig)
- 風清雲談 部落格：[風清雲談](https://blog.fengqing.tw/)
- 電子郵件：[fengqing.tw@gmail.com](mailto:fengqing.tw@gmail.com)