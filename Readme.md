# Quality Assessment of In-the-Wild Videos
## Description
VSFA code for the following papers:

- Dingquan Li, Tingting Jiang, and Ming Jiang. Quality Assessment of In-the-Wild Videos. In Proceedings of the 27th ACM International Conference on Multimedia (MM ’19), October 21-25, 2019, Nice, France.
![Framework](Framework.jpg)
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