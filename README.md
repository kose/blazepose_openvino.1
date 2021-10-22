# blazepose_openvino が動いたよ。

input_name_pd, input_name_lm, oname_pd[] と oname_lm[] をモデルから取得しています。

## model

```
cd /tmp
git clone https://github.com/PINTO0309/PINTO_model_zoo

cd /tmp/PINTO_model_zoo/053_BlazePose
git checkout f6939876a075f0c88254ffb6875c16da0f387a03

cd /tmp/PINTO_model_zoo/053_BlazePose/07_openvino
sh download.sh

cd /tmp/PINTO_model_zoo/058_BlazePose_Full_Keypoints/01_Accurate/07_openvino
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

## environment

- maxOS: openvino-2021.4.1
- Ubuntu: openvino-2021.3




