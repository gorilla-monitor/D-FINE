## Commands to train on SPAC data

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

