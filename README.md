e implement magnitude-based
unstructured and structured pruning with lay-
erwise sensitivity scans and a per-layer sparsity
schedule that hits ∼70% overall sparsity while
tracking accuracy, MACs, parameter bits, storage,
and measured latency. We compare Grad-CAM
maps before and after pruning to show where
feature localization shifts as sparsity rises. In-
tuitively, pruning removes excess capacity and
quantization adds controlled noise; together they
let us “pay” with parameters or precision to buy
speed and memory, and we map where that cost
is gentlest for VGG-11. For quantization, we will
use PTQ and QAT across {fp16, bf16, int8, int4}
and report scaling trends; for distillation, a VGG–
16/19 teacher transfers to a VGG-11 student with
logit/hint/contrastive variants to test whether big-
ger teachers actually help.
