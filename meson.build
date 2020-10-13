
project('MesonLinkBoostBug', ['d', 'cpp'])

src = ['main.d', 'external.cpp']

boost_dep = dependency('boost', modules : ['thread', 'system'], required : false)
if not boost_dep.found()
  message('MESON_SKIP_TEST boost is required.')
endif

app = executable('app', src, dependencies: boost_dep)

test('valid value', app, args : ['0'])
test('valid failing value', app, args : ['7'], should_fail : true)
test('invalid value', app, args : ['twenty'])