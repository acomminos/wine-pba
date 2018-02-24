# wine-pba

A set of patches to allocate dynamic wined3d_buffers from a single persistently mapped buffer managed by a heap allocator, reducing the need for command stream synchronization.

Currently these patches are based off wine-staging 2.21.

[Details can be found here.](https://comminos.com/posts/2018-02-21-wined3d-profiling.html)
