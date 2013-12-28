#
# Copyright (c) 2013 Juniper Networks, Inc. All rights reserved.
#

# -*- mode: python; -*-

env = DefaultEnvironment().Clone()

sources = [
    'nova_contrail_vif/__init__.py',
    'nova_contrail_vif/contrailvif.py',
    'setup.py',
]

sources += env.ThriftGenPy(
    '#controller/src/vnsw/agent/openstack/instance_service.thrift',
    'nova_contrail_vif')

sdist_gen = env.Command('dist', sources, 'python setup.py sdist', chdir=1)
env.Default(sdist_gen)
env.Alias('nova-contrail-vif', sdist_gen)
