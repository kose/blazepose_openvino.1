# blazepose_openvino が期待通りの動作にならないので。

segmentation fault するので input_name_pd, input_name_lm, oname_pd[] と oname_lm[] をモデルから取得しています。

## model

```
cd /tmp
git clone https://github.com/PINTO0309/PINTO_model_zoo

cd /tmp/PINTO_model_zoo/053_BlazePose/01_pose_detection
sh download.sh

cd /tmp/PINTO_model_zoo/053_BlazePose/03_pose_landmark_full_body
sh download.sh
```

## C++

```
cd /tmp
git clone https://github.com/yas-sim/blazepose_openvino.git

cd blazepose_openvino
patch --backup --verbose < diff

mkdir build
cd build

cmake ..
make
```

## 実行

```
./blazenet
```

![result](result.png)

検出結果がおかしいんです。なんでですかね。


## environment

- maxOS: openvino-2021.4.1
- Ubuntu: openvino-2021.3

の両方ともです。



