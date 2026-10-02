# Welcome to Brainquiver

[Brainquiver](https://brainquiver.ai) is rethinking where language models run. We design efficient architectures that fit on microcontrollers smaller than a fingernail, bringing real intelligence to the edge. The result is AI that answers faster, keeps data private, and uses a fraction of the energy and none of the water that a data center needs.

## Models

AURI is a family of language models small enough to run on a single chip, and capable enough to feel like more. Each moment calls on only the part of the model it needs, the way stars light up to form a constellation. No cloud, no in-flight data, no waiting. Just a mind that lives on the device and answers the instant you ask.

Models are still in development. They will be available in the chat on our website and through our API, and some versions will also come with open weights.

## Datasets

Our public datasets live on [Hugging Face](https://huggingface.co/brainquiver), and the rest are used to train our specialized models. More of them will join the open set over time.

### Pretraining

* [general-master-en-202608](https://huggingface.co/datasets/Brainquiver/general-master-en-202608): English pretraining text from three public sources, cleaned and filtered for repetition: 109 million documents and 468 billion characters.
* [general-web-it-202608](https://huggingface.co/datasets/Brainquiver/general-web-it-202608): Italian pretraining text from the Italian part of FineWeb2-HQ, cleaned and filtered for repetition: 21 million documents and 66 billion characters.
* [general-web-fr-202608](https://huggingface.co/datasets/Brainquiver/general-web-fr-202608): French pretraining text from the French part of FineWeb2-HQ, cleaned and filtered for repetition: 32 million documents and 118 billion characters.
* [generate-narrate-tinystories-pretrain](https://huggingface.co/datasets/Brainquiver/generate-narrate-tinystories-pretrain): Microsoft's TinyStories V2, GPT-4 stories only, cleaned and repackaged as Parquet with source and model metadata on every row: 2.7 million stories and 441 million words.

### Post-training

* [reason-qa-biology-finetune-preview](https://huggingface.co/datasets/Brainquiver/reason-qa-biology-finetune-preview): A preview of a larger biology reasoning corpus, generated with gpt-oss-20b in a simple three-field format: about 31,500 examples.

## Tools

We build our own tools for the work behind the models, with many released as open source under the MIT license:

* [OKF Map](https://github.com/brainquiver/open-knowledge-format-map): Offline map view of the Open Knowledge Format frontmatter and relations in MD documents present in a given directory.
* [Parquet Viewer](https://github.com/brainquiver/parquet-viewer): Offline single-page viewer for Parquet files and sharded datasets.
* [Lightweight Parquet Reader](https://github.com/brainquiver/lightweight-parquet-reader): C99 reader for Parquet string columns, with libzstd as its only dependency.
* [Cloudflare R2](https://github.com/brainquiver/cloudflare-r2): Dependency-free Python tools to list, upload and delete Cloudflare R2 objects.
* [JSONL Shuffle](https://github.com/brainquiver/jsonl-shuffle): Rust based JSONL shuffler with multithreading that reproduces Python's random.shuffle order for a given seed.
* [RP2350 as a Debugger](https://github.com/brainquiver/rp2350-as-debugger): Guide to using an RP2350 board as a CMSIS-DAP SWD probe for other microcontrollers.

## MCP Servers

Our MCP servers give AI agents the tools to work inside the services we use every day. They are open source under the MIT license:

* [Trello MCP](https://github.com/brainquiver/trello-mcp): An MCP server that gives an agent 52 Trello tools, with trimmed replies, duplicate-safe batches, a workspace guard and a reason for every refusal.
