project('hello-wayland', 'c')

wl_dep = dependency('wayland-client')
wl_mod = import('unstable-wayland')

xml = wl_mod.find_protocol('xdg-shell')
xdg_shell = wl_mod.scan_xml(xml)

executable('hello-wayland', 'main.c', 'shm.c', xdg_shell, dependencies : [wl_dep])
