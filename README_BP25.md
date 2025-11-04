## TRAIN

SPAC data

```{bash}
export model=n
python train.py -c configs/dfine/spac/dfine_hgnetv2_${model}_spac.yml --use-amp --seed=0
```


COCO data

```
export model=n
python train.py -c configs/dfine/dfine_hgnetv2_${model}_coco.yml --use-amp --seed=0
```


## INFERENCE

```
export model=n
python tools/inference/torch_inf.py -c configs/dfine/spac/dfine_hgnetv2_${model}_spac.yml --resume /workspace/models/detection/dfine/dfine-hgnetv2-n_spac/best_stg1.pth --input /workspace/datasets/spac_coco_formatted/test/M002_20220912_216_54.png --device cuda:0
```

