# SynthuxAI

![Twitter Cover](https://pbs.twimg.com/profile_banners/1871028784734060544/1734923209/1500x500)

[SynthuxAI](https://synthuxai.com) is an AI-powered music creation engine redefining how artists and creators compose, produce, and innovate. With SynthuxAI, explore endless musical possibilities and unleash your creativity effortlessly.

Follow us on [Twitter](https://x.com/SynthuxAI) for updates and inspiration.

## Features

- **AI-Driven Music Generation**: Compose polyphonic music and experiment with multi-track arrangements effortlessly.
- **User-Friendly Interface**: Designed for creators of all skill levels, from beginners to professionals.
- **Customizable Settings**: Fine-tune every aspect of your music to align with your creative vision.
- **Integration Ready**: Seamlessly works with your existing music production tools.

## Getting Started

### Prerequisites

Make sure you have the following installed:
- Python 3.8 or higher
- pip or pipenv for managing dependencies

### Install Dependencies

#### Using pipenv (recommended)
```sh
# Install the dependencies
pipenv install
# Activate the virtual environment
pipenv shell
```

#### Using pip
```sh
# Install the dependencies
pip install -r requirements.txt
```

### Prepare Training Data

SynthuxAI leverages training data from a variety of sources. To get started:

```sh
# Download the training data
./scripts/download_data.sh
# Process the training data
./scripts/process_data.sh
```

## Scripts

### Train a New Model

1. Set up a new experiment:
   ```sh
   ./scripts/setup_exp.sh "./exp/my_experiment/" "Experiment notes here"
   ```

2. Customize your configuration files.

3. Train the model:
   ```sh
   ./scripts/run_train.sh "./exp/my_experiment/" "0"
   ```

Or run a full experiment:
```sh
./scripts/run_exp.sh "./exp/my_experiment/" "0"
```

### Use Pretrained Models

1. Download pretrained models:
   ```sh
   ./scripts/download_models.sh
   ```

2. Perform inference:
   ```sh
   ./scripts/run_inference.sh "./exp/default/" "0"
   ```

## Outputs

Generated music is stored in the following formats by default:
- `.npy`: Raw numpy arrays
- `.png`: Visualization of music tracks
- `.npz`: Multi-track pianoroll files

Convert `.npz` to MIDI:
```python
from pypianoroll import Multitrack
m = Multitrack('./test.npz')
m.write('./test.mid')
```

## License

SynthuxAI is open-source. See the LICENSE file for details.

## Contact

For inquiries or support, visit [synthuxai.com](https://synthuxai.com) or reach out on [Twitter](https://x.com/SynthuxAI).
