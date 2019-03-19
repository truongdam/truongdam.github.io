#### Cải thiện tốc độ load website với Uglifyjs
##### Tại sao sử dụng uglifyjs
- Giả sử bạn đang phát triển một website hoặc một page với những công nghệ liên qua đến javascript, một page có chứa quá nhiều file ```*.js```, việc include nhiều file ```js``` vậy, làm ảnh hưởng đến tốc độ load trang, hay website.
- Bạn cần tối ưu page hay website, cụ thể là nén các file ```*.js``` lại với nhau thành một file, bạn có thể tham khảo Uglifyjs. Bài sau đây, mình sẽ hướng dẫn cách sử dụng cơ bản UglifyJs

##### Step by step:
- Tạo project:
```
    mkdir uglify-demo
    
    yarn init
```
- Xem qua [cách sử dụng yarn](https://truongdam.github.io/2019/03/19/tu-hoc-co-ban-ve-yarn/) nếu chưa biết, nhập các thông tin cần thiết, ta có file ```package.json``` chứa nội dung sau :

```
{
  "name": "Devent",
  "version": "1.0.1",
  "description": "lib manage event (dispatchers and listeners)",
  "main": "index.js",
  "repository": "https://github.com/truongDam",
  "author": "truongdam",
  "license": "MIT",
  "private": true,
  "dependencies": {}
  }
```
- Install package Uglifyjs bằng cách:
```
    yarn add uglify-js --dev
```
- Tạo thư mục ```src``` và ```lib``` trong project:
```
mkdir src
mkdir lib
```
- Tạo 2 file ```one.js``` và ```second.js``` trong thư mục ```src```. Chỉnh sửa nội dụng 2 file như bên dưới

```
// one.js
var One = function() {
    console.log("file one");
}

// second.js
console.log("file second");

```
- Mở file package.json và thêm vào:
```
"scripts": {
    "build": "uglifyjs ./src/*.js -o ./lib/devent.min.js"
}
```
- Run command để build:
```
yarn build
```
- Kết quả, tạo được file ```devent.min.js``` bằng cách nén nhiều file ```js``` lại với nhau như: ```one.js``` ```second.js```

##### Kết luận
- Có thể sử dụng lib trên để tăng tốc độ page tối ưu các file script.
