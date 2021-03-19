https://hub.docker.com/r/airsplay/bottom-up-attention
```
docker pull airsplay/bottom-up-attention
```
```
sudo docker run --gpus all -v /home/gaowen/videocaption/mscoco_dataset:/workspace/images:ro -v $(pwd)/data/mscoco_imgfeat:/workspace/features --rm -it airsplay/bottom-up-attention bash

cd/workspace/features

CUDA_VISIBILE_DEVICES=0 python extract_coco_image.py --split valid
```
```
exit

sudo docker start -i container_name

apt-get update

```

Or
```
sudo nvidia-docker run -it -v $(pwd):/workspace --name attention airsplay/bottom-up-attention bash

cd \opt\btud

python ./tools/generate_tsv.py --gpu 1 --cfg /opt/butd/experiments/cfgs/faster_rcnn_end2end_resnet.yml --def /opt/butd/models/vg/ResNet-101/faster_rcnn_end2end_final/test.prototxt --out /workspace/bottom-up-attention/test2014_resnet101_faster_rcnn_liu.tsv --net /workspace/bottom-up-attention/data/faster_rcnn_models/resnet101_faster_rcnn_final.caffemodel --split coco_test2014
```
