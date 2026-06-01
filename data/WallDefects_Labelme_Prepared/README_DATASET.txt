Dataset prepared from Labelme annotations.

Main layout:
  train/images, train/masks, train/vis
  val/images, val/masks, val/vis
  test/images, test/masks, test/vis

UltraSeg-compatible layout:
  for_ultraseg/train/images
  for_ultraseg/train/masks
  for_ultraseg/train/points_boundary2
  for_ultraseg/test/images   (mapped from val split)
  for_ultraseg/test/masks    (mapped from val split)

Notes:
- Masks are binary PNG (0 background, 255 defect).
- You can train with:
  python train.py --dataset WallDefects --data_root "<dst_root>/for_ultraseg" --algo ultraseg108
