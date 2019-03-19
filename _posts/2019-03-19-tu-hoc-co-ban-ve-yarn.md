#### Hướng dẫn sử dụng cơ bản yarn
- yarn là gì: yarn là một module quản lí các package đã được đăng kí từ NpmJS hoặc Bower.
- Ưu điểm :
    - Tốc độ nhanh hơn npm
    - Cấu trúc các dependencies bằng phẳng hơn so với cấu trúc lồng nhau của npm

##### Cách cài đặt yarn:
- Cài đặt thông qua npm:
```
npm install -g yarn
```
- Cài đặt thông qua bản download từ trang chủ [Yarn](https://yarnpkg.com/en/docs/install#debian-stable)

#### Install package
Yarn sử dụng file ```packake.json``` để cài đặt các package mong muốn.
Sử dụng lệnh ``` yarn install``` để cài đặt.
Khai báo file ```package.json``` như sau:

```
{
  "name": "vue_demo",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "serve": "vue-cli-service serve --port 8080",
    "build": "vue-cli-service build",
    "lint": "vue-cli-service lint"
  },
  "dependencies": {
    "moment": "^2.24.0",
    "vue": "^2.5.21",
    "vue-router": "^3.0.1",
    "vuex": "^3.0.1"
  },
  "devDependencies": {
    "@vue/cli-plugin-babel": "^3.3.0",
    "@vue/cli-service": "^3.3.0",
    "webpack-bundle-tracker": "^0.4.2-beta",
  }
}
```

##### Thêm, xóa các dependencies:
```
yarn add [package-name] # Thêm 1 dependencies
yarn add [package-name]@[version] # Thêm 1 dependencies với version
yarn upgrade [package-name]@[version] # Upgrade version
yarn remove [package-name] # Xóa package mong muốn
```

##### Yarn lock file
- Sau khi nâng cấp, thêm, xóa các package, yarn luôn update lên file yarn.lock để quản lí chính xác các packge version được cài đặt trong ``` node-modules```
