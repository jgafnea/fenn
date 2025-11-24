Introduction
============

SMLE is a lightweight Python framework that automates the "boring stuff" in Machine Learning projects so you can focus on the model. It handles configuration parsing, logging setup, and experiment tracking in a minimal, opinionated way.

Why SMLE?
---------

* **Auto-Configuration:** ``yaml`` files are automatically parsed and injected into your entrypoint, so you avoid hardcoded hyperparameters.
* **Instant Logging:** All print statements and configurations are captured to local logs and compatible remote trackers.
* **Remote Monitoring:** Native integration with `Weights & Biases (WandB) <https://wandb.ai/>`_ lets you monitor experiments from anywhere.

Security & WandB Configuration
------------------------------

When using the ``wandb`` section for remote logging, the API key is read from ``smle.yaml``. To avoid exposing credentials, do not commit ``smle.yaml`` or log files with real keys to any public repository.

* Add ``smle.yaml`` and ``*.log`` to ``.gitignore``.
* Remove the ``wandb`` section entirely if remote logging is not required.

Contributing
------------

Contributions are welcome. Fork the repository, create a feature branch, commit your changes, push the branch, and open a pull request with a clear description of the improvement.

Roadmap
-------

High-priority goals include richer documentation, safer key management (for example, through ``.env`` support), and multiple or layered YAML configurations.

Planned features include ML project templates, model utilities, notification tools, data exploration helpers, analysis utilities (such as confusion matrices), additional integrations like TensorBoard, and comprehensive testing support.