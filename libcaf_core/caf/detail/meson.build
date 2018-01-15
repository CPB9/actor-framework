conf_data = configuration_data()

conf_data.set('CAF_LOG_LEVEL', 0)
conf_data.set('CAF_LOG_LEVEL_INT', -1)
conf_data.set('CAF_NO_EXCEPTIONS_INT', -1)
conf_data.set('CAF_NO_MEM_MANAGEMENT_INT', -1)
conf_data.set('CAF_ENABLE_RUNTIME_CHECKS_INT', -1)
conf_data.set('CAF_USE_ASIO_INT', -1)

configure_file(
  input : 'build_config.hpp.in',
  output : 'build_config.hpp',
  configuration : conf_data
)

