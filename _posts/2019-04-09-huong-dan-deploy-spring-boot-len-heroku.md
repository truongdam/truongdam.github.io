## Hướng dẫn tạo ứng dụng SpringBoot và deploy ứng dụng lên Heroku

SpringBoot là framework java dùng để phát triển các hệ thống lớn, đang được sử dụng rộng rãi.

Heroku là clould app miễn phí cho phép bạn deploy các ứng dụng web, api của bạn với sự hỗ trợ nhiều ngôn ngữ như: Java, NodeJS, Ruby ...

Bài viết sau mình sẽ hướng dẫn tóm tắt các tạo ứng dụng SpringBoot và deploy lên Heroku

#### Các bước tạo ứng dụng SpringBoot deploy lên Heroku:

* Bước 1: Tạo project SpringBoot

    * Đơn giản là bạn có thể generate một ứng dụng SpringBoot thông qua [start.spring.io](https://start.spring.io/)

    * Download source và giải nén

    * Mở source bằng IDE (có thể sử dụng IntelIJ ...). Import các  dependency và library cần thiết

* Bước 2: Tạo repository trên github, và đưa source code hiện tại lên repository

    * Setup git cho project
    ```
    git init
    git remote add origin [repository]
    git pull origin master
    ```
    * Setup gitignore cho project
    ```
    cd [project]
    touch .gitignore    // then edit file
    git rm -r --cached .
    git add .
    git commit -m "init file"
    ```
    * Push source lên github
    ```
    git push origin master
    ```
* Bước 3: Tạo ứng dụng trên heroku và connect đến repository github

    * Vào website [Heroku](heroku.com) đăng kí account. Sau đó vào . Chọn New > Create new app. Đặt tên cho app, sau đó chọn Create App.

    * Sau khi tạọ, chúng ta vào App vừa tạo, Chọn tab Deyploy. 

    * Deployment method: chọn GitHub

    * App connected to GitHub: chọn repository cần deploy

    * Chọn Auto Deploy và Deyploy Branch

Chờ Build Successfully. Và xem kết quả.
