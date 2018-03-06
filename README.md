# wine-pba

A set of patches to allocate dynamic wined3d_buffers from a single persistently mapped buffer managed by a heap allocator, reducing the need for command stream synchronization.

**This patchset is prototype-quality at the moment. If `ARB_buffer_storage` is not present, you're not going to have a good time.**

Currently, these patches are based off wine-staging 3.3.

[Details can be found here.](https://comminos.com/posts/2018-02-21-wined3d-profiling.html)
