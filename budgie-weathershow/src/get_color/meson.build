#configurationData = configuration_data()
#configurationData.set('PACKAGE_NAME', meson.project_name())
#configurationData.set('LOCALE_DIR', LOCALE_DIR)
#configure_file(input: 'config.h.in', output: 'config.h', configuration: configurationData)

#install_data('WeatherShow.plugin', install_dir: LIB_INSTALL_DIR)

GetColorSources = [
'get_color.vala'
]

GetColorDependencies = [
dependency('gtk+-3.0'),
dependency('gee-0.8'),
meson.get_compiler('c').find_library('m', required: false)
]

GetColorValaArgs = [
'--pkg=config',
'--vapidir=' + VAPI_DIR,
'--target-glib=2.38',
]

GetColorCArgs = [
'-include',
'config.h',
'-lm'
]

#GetColorCArgs = [
#'-lm'
#]

#shared_library(
#    'weathershow',
#    WeatherShowSources,
#    dependencies: WeatherShowDependencies,
#    vala_args: WeatherShowValaArgs,
#    c_args: WeatherShowCArgs,
#    install: true,
#    install_dir: LIB_INSTALL_DIR
#)


executable(
    'get_color', GetColorSources,
    dependencies: GetColorDependencies,
    install: true,
    vala_args: GetColorValaArgs,
    c_args: GetColorCArgs,
    install_dir: LIB_INSTALL_DIR,
)



