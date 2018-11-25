# ai-distillery

Automatically modelling and distilling knowledge within AI. In other words,
summarise the arxiv firehose. Map, categorise, quantify, qualify, filter,
search, browse, reduce, digest, compress, summarise and model all knowledge
within ML/DL/RL/AI/DS/CS/Stats. And, always for the community. 

We are showing our results at [AI Distillery Heroku web server](https://ai-distiller.herokuapp.com/) 

## Reproducibility

### Installation

Please consider using a virtual environment as shown below.
This way, the scripts won't pollute your global `$PATH`.

```sh
git clone https://github.com/ai-distillery
cd ai-distillery
virtualenv venv && source venv/bin/activate # STRONGLY RECOMMENDED
pip install -e .
```

The package will install the following executables:

- `embed_doc2vec`
- `embed_lsa`
- `embed_word2vec`
- `harvest_semanticscholar`
- `extract_entities`

The commands link the respective executable scripts in `bin/`.

### Fetching Data

We maintain [a fork](https://github.com/beduffy/arxiv-sanity-preserver) of
[Karpathy's Arxiv Sanity Preserver](https://github.com/karpathy/arxiv-sanity-preserver) to harvest
structured meta-data as well as full-text data from [ArXiV](https://arxiv.org).

We assume in the following that the `data/db.p` holds the database of
structured metadata. The directory `data/txt` contains the raw
`<arxiv_Id>.pdf.txt` full-text files.

For convenience we have registered our fork of arxiv-sanity-preserver as a submodule.
To clone the submodule, issue the following command.

```sh
git submodule update --init
```

Then follow the [guide by Karpathy](https://github.com/karpathy/arxiv-sanity-preserver) to run the code.

### Executing the scripts

Please consult `-h` for more information on how to run one of the executables.

### Developing

Make sure to install the aidistillery  package by `pip install -e .` or `python3 setup.py develop`.
This way, any changes are taken into account without the need to reinstall.
We look forward to receiving your pull requests.

