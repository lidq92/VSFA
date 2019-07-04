# Quality Assessment of In-the-Wild Videos
## Description
VSFA code for the following papers:

- Li, Dingquan, Tingting Jiang, and Ming Jiang. "Quality Assessment of In-the-Wild Videos", ACM MM 2019.
### Requirement
```bash
pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
```
- PyTorch 1.1.0
- TensorboardX 1.2, TensorFlow-TensorBoard
- [pytorch/ignite](https://github.com/pytorch/ignite)

### Feature Extraction

```
CUDA_VISIBLE_DEVICES=0 python CNNfeatures.py --database=KoNViD-1k --frame_batch_size=64
```

You need to specify the `database` and change the corresponding `videos_dir`.

### Quality Prediction
#### intra-database experiments

```
CUDA_VISIBLE_DEVICES=0 python VSFA.py --database=KoNViD-1k --exp_id=0
```

You need to specify the `database` and `exp_id`.

#### test demo

```
python test_demo.py --video_path=test.mp4
```

### Contact
Dingquan Li, dingquanli AT pku DOT edu DOT cn.