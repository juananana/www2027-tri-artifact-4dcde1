# WWW 2027 TRI anonymous artifact

This repository hosts the anonymous review artifact for the submitted paper. Download `anonymous_artifact.zip`, verify its SHA-256 checksum, extract it, and run the offline entry point:

```bash
shasum -a 256 -c SHA256SUMS
unzip anonymous_artifact.zip
cd anonymous_artifact
python3 -m pip install -r requirements.txt
python3 -B scripts/recompute_all.py
```

Expected archive checksum:

```text
4dcde1a575d53d84e28e8a70ae4087e010c14d247806180c8f2e1f62073c4af7  anonymous_artifact.zip
```

The ZIP is 5,022,016 bytes. It contains retained evaluation instances, model outputs (including format and connection failures), execution evidence, scoring code, protocols, configurations and third-party notices. It does not contain the manuscript source/PDF, repository history, credentials, model weights, service databases or private reader responses.

The offline scripts do not call a model, paid API or native service. They reproduce the principal counts, state checks and fixed-seed interleaved statistics from the retained evidence. Fresh hosted-model or native-service runs are external replications and are not required for offline verification.
