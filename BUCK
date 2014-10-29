include_defs('//bucklets/gerrit_plugin.bucklet')

gerrit_plugin(
  name = 'gerritScore',
  srcs = glob(['src/main/java/**/*.java']),
  resources = glob(['src/main/resources/**/*']),
  manifest_entries = [
    'Gerrit-PluginName: gerritScore',
    'Gerrit-ApiType: plugin',
    'Gerrit-ApiVersion: 2.10-rc0',
    'Gerrit-Module: com.googlesource.gerrit.plugins.testplugin.Module',
    'Gerrit-SshModule: com.googlesource.gerrit.plugins.testplugin.SshModule',
    'Gerrit-HttpModule: com.googlesource.gerrit.plugins.testplugin.HttpModule',
  ],
)

# this is required for bucklets/tools/eclipse/project.py to work
java_library(
  name = 'classpath',
  deps = [':gerritScore__plugin'],
)

