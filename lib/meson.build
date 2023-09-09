treesitter_sources = [
    'src/lib.c',
]

treesitter_includes = include_directories(
    'include',
)

treesitter_lib = library(
    meson.project_name(),
    treesitter_sources,
    include_directories: treesitter_includes,
)

treesitter_dep = declare_dependency(
    link_with: treesitter_lib,
    include_directories: treesitter_includes,
    version: meson.project_version(),
)

pkgconfig = import('pkgconfig')
pkgconfig.generate(
    treesitter_lib,
    name: meson.project_name(),
    version: meson.project_version(),
    description: 'An incremental parsing system for programming tools ',
)



