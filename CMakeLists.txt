cmake_minimum_required(VERSION 3.6.0)

project(asteroid-gps-test
	VERSION 0.0.1
	DESCRIPTION "A gps test app for AsteroidOS")

find_package(ECM REQUIRED NO_MODULE)
find_package(AsteroidApp REQUIRED)

set(CMAKE_MODULE_PATH ${ECM_MODULE_PATH} ${ASTEROID_MODULE_PATH})

include(FeatureSummary)
include(GNUInstallDirs)
include(ECMQMLModules)
include(AsteroidCMakeSettings)
include(AsteroidTranslations)

add_subdirectory(src)

generate_desktop(${CMAKE_SOURCE_DIR} asteroid-gps-test)

feature_summary(WHAT ALL FATAL_ON_MISSING_REQUIRED_PACKAGES)
