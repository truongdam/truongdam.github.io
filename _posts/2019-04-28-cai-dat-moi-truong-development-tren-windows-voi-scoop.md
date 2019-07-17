## Cài đặt Scoop cho môi trường development trên windows

#### Tại sao phải sử dụng scoop
* Nếu bạn hay sử dụng hệ điều hành Unix, có lẽ tính hiệu quả của ternimal trên Unix là điều khác biệt nhất so với Windows.
* Bạn dễ dàng cài đặt Java, NodeJs, Yarn, Npm, Python chỉ bằng một vài command line trên Unix, trong khi Windows thì không thể với bash - power shell.
* Scoop.sh được tạo ra với mục đích, dễ dàng cài đặt môi trường dev cho Windows dễ dàng như Unix. Bạn có thể cài đặt Java, NodeJs chỉ bằng một vài command line mà không phải download file ```exe```.

#### Cách cài đặt
* Mở power shell, và run command line dưới đây
```
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```
Vậy là xong. Đã cài đặt scoop.sh thành công. Các bạn có thể check bằng command line ```scoop ```

#### Cài đặt một tools mà bạn dùng bằng scoop
* Dễ dàng cài đặt curl, git, nodejs, java bằng command line sau
```
scoop install curl
scoop install git
scoop install nodejs
```

#### Check tất cả các tools đã cài đặt
```
scoop list
```

#### Tìm hiểu thêm về scoop, về commands scoop
```
scoop
scoop help
```

Reference: [Scoop.sh](https://scoop.sh/)
