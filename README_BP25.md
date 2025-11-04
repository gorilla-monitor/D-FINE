## TRAIN

SPAC data

```{bash}
export model=n
python train.py -c configs/dfine/custom/dfine_hgnetv2_${model}_custom.yml --use-amp --seed=0
```


COCO data

```
export model=n
python train.py -c configs/dfine/dfine_hgnetv2_${model}_coco.yml --use-amp --seed=0
```


## INFERENCE

```
export model=n
python tools/inference/torch_inf.py -c configs/dfine/custom/dfine_hgnetv2_${model}_custom.yml -r /workspace/models/detection/dfine/dfine_hgnetv2_n_spac/best_stg1.pth --input /workspace/datasets/spac_coco_formatted/test/M002_20220912_216_54.png --device cuda:0
```

