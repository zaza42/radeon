# radeon
for [Radeon HD 6400M/7400M Series]


Allow 10% frequency variance between non-DP monitors.

Most real-world monitors have a little tolerance to non-quite-right input
frequencies, so we can take advantage of this for heterogeneous multi-head
setups.

Kernels prior to 3.6 (I think) did this by accident, and it was useful, so
this patch reintroduces the "bug" as a feature, in a slightly more limited
way.

Monitors that do not support the variance should simply display "Input
frequency out of range", or whatever, these days. In any case, the kernel
has been doing this for years and I've not heard of fried hardware.

Signed-off-by: Andrew Stubbs <ams@codesourcery.com>
