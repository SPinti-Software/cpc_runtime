set(runtime_srcs
	runtime.c
)

add_library(cpc_runtime SHARED ${runtime_srcs})
add_library(cpc_runtime-static STATIC ${runtime_srcs})
