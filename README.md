# Training data and benchmarks

Static page at `https://jxb1st.github.io/data-bench-collection/`: one representative example per task
type, with its annotation as released, for the training datasets (VidChapters-7M, Ego4D,
LLaVA-Video-178K) and benchmarks (StreamingBench, OVO-Bench, Video-MME, LongVideoBench, MLVU, LVBench,
CG-Bench, MVBench, VideoMemBench) used by the project, plus per-dataset statistics.

- `index.html`: the page. `style.css` is the shared stylesheet of the experiment panel; `collection.css`
  adds the example cards.
- `clips/<dataset>/`: short excerpts re-encoded at 480p H.264 with a poster frame; VidChapters examples
  also carry a frame strip with one frame per chapter start.
- `data/samples.json`: the selected examples with their annotation fields. `data/stats.json`: the
  statistics shown on the page, computed from the released annotation files where available.

How examples were chosen: for each dataset, every task type (or category) gets one example, picked
deterministically from the released annotations with a preference for short questions and short
videos, so that the clip can be served from a Pages repository. Where the videos are not available
from this cluster (LVBench and CG-Bench are YouTube or gated archives, Ego4D is licensed), the example
is annotation only and the page says so. Annotation text is verbatim; nothing is paraphrased.
