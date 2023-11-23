```bash
python create_lmdb_dataset.py --inputPath data_augmen/ --gtFile data_augmen/gt.txt --outputPath result_augment
```

```bash
set CUDA_VISIBLE_DEVICES=0 & python train.py --train_data result --valid_data result --select_data / --batch_ratio 0.5 --character "0123456789abcdefghijlkmnopqrstuvwxyz" --num_iter 10000 --Transformation TPS --FeatureExtraction ResNet --SequenceModeling BiLSTM --Prediction Attn --workers 0 --valInterval 500
```

```bash
set CUDA_VISIBLE_DEVICES=0 & python demo.py --Transformation TPS --FeatureExtraction ResNet --SequenceModeling BiLSTM --Prediction Attn --image_folder data_test/test --saved_model =....
```
