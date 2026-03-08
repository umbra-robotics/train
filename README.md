# train

Colab notebook for training a **Diffusion Policy** on the SO-101 robot arm using [LeRobot](https://github.com/huggingface/lerobot).

## What's in here

`train_diffusion_so101.ipynb` — end-to-end training pipeline that:

1. Installs LeRobot + dependencies on a Colab GPU runtime
2. Loads the `lerobot/svla_so101_pickplace` dataset (50 episodes, dual-camera)
3. Trains a diffusion policy for pick-and-place with WandB logging
4. Uploads the trained checkpoint to Hugging Face Hub

Works on a free T4 (~10h for 100k steps) or an A100 (~3h).

## Quick start

Open the notebook in Google Colab, set your `HF_TOKEN`, `HF_USER`, and `WANDB_API_KEY` secrets, and run all cells.

## References

- [Diffusion Policy paper](https://arxiv.org/abs/2303.04137)
- [LeRobot docs](https://huggingface.co/docs/lerobot)
- [SO-101 pick-place dataset](https://huggingface.co/datasets/lerobot/svla_so101_pickplace)
