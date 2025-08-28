# Differential Gaussian Rasterization
参考自3DGS官方
修改2处内容（已经改好了）
```
// Eq. (3) from 3D Gaussian splatting paper.
            for (int ch = 0; ch < CHANNELS; ch++)
                C[ch] += alpha * T;
```
```
            if(invdepth)
            expected_invdepth += (depths[collected_id[j]]) * alpha * T;
```
## 安装noramldepth_acca_diff-gaussian-rasterization
进入终端
```
pip uninstall diff-gaussian-rasterization
cd path\to\submodules\diff-gaussian-rasterization
python setup.py develop
```
看到安装成果提示即可，这样原本的diff-gaussian-rasterization就返回累积不透明度+推理的深度