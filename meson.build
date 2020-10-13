project('MesonLinkBoostBug', ['d', 'cpp'])

src = ['main.d', 'external.cpp']

boost_dep = dependency('boost', modules: 'thread')

executable('app', src, dependencies: boost_dep)