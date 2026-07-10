# Tương tác với terminal, build custom image

docker run -it ubuntu:22.04 bash

-it
i: interactive -> cho phép gõ lệnh
t: tty -> tạo terminal ảo
bash: 1 kiểu terminal (bash/sh)

1. check image `ubuntu:22.04` is existing?
   if in local -> run
   else pull the image from dockerhub -> run

Lưu ý: nếu cài tools trong terminal này thì chỉ đang cài trên container thôi, thoát ra,
mở 1 terminal khác thì sẽ không còn các tools này nữa
Để giải quyết vấn đề này cần tạo 1 image chạy OS `ubuntu:22.04` và cài sẵn `nano`
-> tạo Dockerfile -> build ra 1 custom image -> run

2. Build 1 custom image

```
docker build -t my-linux .
```

`docker build` là command dùng để build (tạo) Docker image từ một Dockerfile
`-t my-linux` viết tắt của tag là `-t`, tên image là `my-linux`
`.` là build context, docker sẽ lấy toàn bộ file trong thư mục hiện tại để build
