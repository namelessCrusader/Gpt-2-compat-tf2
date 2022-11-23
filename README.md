**Status:** Archive (code is provided as-is, no updates expected)

# gpt-2

Code and models from the paper ["Language Models are Unsupervised Multitask Learners"](https://d4mucfpksywv.cloudfront.net/better-language-models/language-models.pdf).

You can read about GPT-2 and its staged release in [original blog post](https://blog.openai.com/better-language-models/), [6 month follow-up post](https://openai.com/blog/gpt-2-6-month-follow-up/), and [final post](https://www.openai.com/blog/gpt-2-1-5b-release/).

They have also [released a dataset](https://github.com/openai/gpt-2-output-dataset) for researchers to study their behaviors.

## Usage

This repository is meant to be a starting point for researchers and engineers to experiment with GPT-2.
This repository adds compatibility for GPT-2 for tensorflow 2.0 and above.

For basic information, see our [model card](./model_card.md).

### Some caveats

- GPT-2 models' robustness and worst case behaviors are not well-understood.  As with any machine-learned model, carefully evaluate GPT-2 for your use case, especially if used without fine-tuning or in safety-critical applications where reliability is important.
- The dataset our GPT-2 models were trained on contains many texts with [biases](https://twitter.com/TomerUllman/status/1101485289720242177) and factual inaccuracies, and thus GPT-2 models are likely to be biased and inaccurate as well.
- To avoid having samples mistaken as human-written, we recommend clearly labeling samples as synthetic before wide dissemination.  Our models are often incoherent or inaccurate in subtle ways, which takes more than a quick read for a human to notice.

## Installation
0. git clone https://github.com/namelessCrusader/Gpt-2-compat-tf2/edit/master/

1. python/python3 download_model.py 117M/335M/etc.

2. pip install tensorflow(if you don't have V2.0, this package add compatibility for Tensorflow 2.0)

3. pip install -r requirements.txt

4. cd src

5. python/python3 generate_unconditional_samples.py/interactive_conditional_samples.py

## Contributors

See [CONTRIBUTORS.md](./CONTRIBUTORS.md)

## Citation

Please use the following bibtex entry:
```
@article{radford2019language,
  title={Language Models are Unsupervised Multitask Learners},
  author={Radford, Alec and Wu, Jeff and Child, Rewon and Luan, David and Amodei, Dario and Sutskever, Ilya},
  year={2019}
}
```

## License

[Modified MIT](./LICENSE)
