# model-training-sim

A fake model-training screen. `train.py` prints made-up CUDA logs, progress bars and a loss that slowly goes down, so a terminal looks like a long training run is going. Nothing is trained and it never touches the GPU.

## Run it

```bash
python3 train.py
```

Or with [uv](https://docs.astral.sh/uv/), which picks up Python 3.12 and `tqdm` from `uv.lock`:

```bash
uv run train.py
```

`tqdm` is optional. Without it you get plain text instead of progress bars. Press Ctrl-C to stop.

## Layout

- `train.py` – the simulator. It loops forever.
- `main.py` – placeholder that prints a greeting.
- `QLoRA/`, `ViT/`, `diffusion-model/` – each holds a `console.txt` of sample console output.

## Notes

- Everything shown (GPU names, memory, checkpoints, accuracy) is invented.
- Python 3.12 or newer.
