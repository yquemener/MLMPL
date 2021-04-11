What
====
This is a license designed to apply to pre-trained machine learning models. It allows to share a model in a copyleft fashion: allowing modification and reuse but guaranteeing that the model remains open.

Why
===
Existing open source license assume you are releasing something that can have a binary form and a source code form. These notions are not directly applicable to the machine learning world. This license disambiguates a few things.

How
===
I took the Affero GPLv3 license, added a "machine learning model" definition in section 0, obligations in section 1, and restrictions in the basic permissions in section 2. I modified the rest to mention "models" and "weights" when appropriate instead of source code or object code.

TLDR
====
1. If you release a model under the MLMPL, in addition to providing the trained weights, you also have to publish and license the training and inference programs under the AGPLv3 (or later).
2. If you derive a model (e.g. by fine-tuning) from a MLMPL model, then your derived model has to be under the MLMPL
3. If you produce media (defined as 'non model outputs') with a MLMPL model, you have to:
  - put a notice indicating which model was used
  - allow people to download this model or a more recent one.

Judgement calls
===============
I read a lot of discussions and advice, both about the legality and practicability of solutions, before writing this license. I had to make two decisions to write this license. I suppose different decisions on those could lead to a different license:

1. **You don't need to publish the full training dataset**.

    Datasets can be huge, private, can be generated on-line and not saved, can include privacy-sensitive data. We want it easy to release models that can be improved by the community. Of course, open datasets are a very good thing, but mandating them for open models is an unnecessary barrier. You still need to specify the type and volume of data used for the training.

2. **When you publish a MLMPL-model output, you don't have to link to the specific model used but you can link to a better one instead**.

  This takes into account the case of constantly-training models. It would be impractical to keep a backup of all training iterations, especially for big models, so it is considered acceptable to link to the most up-to-date model. The exact wording is "it is acceptable, [..] to provide a later version of the machine learning model that exhibits similar or better performance on the objective metrics relevant to the task at hand."
