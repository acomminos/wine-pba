# wine-pba

A set of patches to allocate dynamic wined3d_buffers from a single persistently mapped buffer (via `ARB_buffer_storage`) managed by a heap allocator, reducing the need for command stream synchronization.

Several related changes are included in the patchset as well:

- `ARB_multi_bind` is used to speed up UBO updates
    - This vastly improves constant buffer performance as PBA causes much more frequent rebinds.

**This patchset is prototype-quality at the moment. If `ARB_buffer_storage` is not present, you're not going to have a good time.**

Currently, these patches are based off wine-staging 3.4.

[Details can be found here.](https://comminos.com/posts/2018-02-21-wined3d-profiling.html)
