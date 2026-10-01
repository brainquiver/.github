# Welcome to Brainquiver

Brainquiver is rethinking where language models run. We design efficient architectures that fit on microcontrollers smaller than a fingernail, bringing real intelligence to the edge. The result is AI that answers faster, keeps data private, and uses a fraction of the energy and none of the water that a data center needs.

## Models

AURI is a family of language models small enough to run on a single chip, and capable enough to feel like more. Each moment calls on only the part of the model it needs, the way stars light up to form a constellation. No cloud, no in-flight data, no waiting. Just a mind that lives on the device and answers the instant you ask.

Models are still in development. They will be available in the chat on our website and through our API, and some versions will also come with open weights.

## Datasets

Our public datasets live on [Hugging Face](https://huggingface.co/brainquiver), and the rest are used to train our specialised models. More of them will join the open set over time.

### Pretraining

* [general-master-en-202608](https://huggingface.co/datasets/Brainquiver/general-master-en-202608)
* [general-web-it-202608](https://huggingface.co/datasets/Brainquiver/general-web-it-202608)
* [general-web-fr-202608](https://huggingface.co/datasets/Brainquiver/general-web-fr-202608)
* [generate-narrate-tinystories-pretrain](https://huggingface.co/datasets/Brainquiver/generate-narrate-tinystories-pretrain)

### Post-training

* [reason-qa-biology-finetune-preview](https://huggingface.co/datasets/Brainquiver/reason-qa-biology-finetune-preview)

## Tools

We build our own tools for the work behind the models, with many released as open source under the MIT licence:

* [open-knowledge-format-graph](https://github.com/brainquiver/open-knowledge-format-graph)
* [parquet-viewer](https://github.com/brainquiver/parquet-viewer)
* [lightweight-parquet-reader](https://github.com/brainquiver/lightweight-parquet-reader)
* [cloudflare-r2](https://github.com/brainquiver/cloudflare-r2)
* [jsonl-shuffle](https://github.com/brainquiver/jsonl-shuffle)
* [rp2350-as-debugger](https://github.com/brainquiver/rp2350-as-debugger)

## MCP Servers

Our MCP servers give AI agents the tools to work inside the services we use every day. They are open source under the MIT licence:

* [trello-mcp](https://github.com/brainquiver/trello-mcp)
