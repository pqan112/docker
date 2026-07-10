# Tạo thư mục và tạo file trong folder app trên bash terminal

```
mkdir folder1
touch index.html
```

`mkdir [folder name]` là make directory với tên folder
`touch` dùng để tạo file

đây là tạo file bên trong thư mục app của container do đó khi run 1 container các folder và file sẽ biến mất

nếu mỗi lần sửa phải thêm code -> build lại image và run container mới thì rất mất thời gian

```
RUN mkdir folder1
RUN touch index.html
```

-> volume mapping

```
run -v ./mapping:/app -it my-app bash
```

nó sẽ map folder mapping ở local và app trong container, thêm folder và file trong container sẽ mapping về local, mỗi lần tạo 1 container mới thì run với -v (`volume`) thì container sẽ có các thư mục giống như ở local kể cả chỉnh sửa file

```
mkdir folder1
touch index.html
```
