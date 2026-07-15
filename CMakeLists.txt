cmake_minimum_required(VERSION 3.24)
project(AltbaseModule_litecoinii VERSION 0.1.5 LANGUAGES CXX)

if(NOT COMMAND altbase_register_node_coin)
  message(FATAL_ERROR "Load the Altbase native-core SDK before this module")
endif()
altbase_register_node_coin(litecoinii LitecoinII)
altbase_register_utxo_coin(litecoinii LitecoinII)
