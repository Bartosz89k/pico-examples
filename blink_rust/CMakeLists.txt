add_executable(blink_rust
        blink.c
        )
#${CMAKE_SOURCE_DIR}/pico_w/wifi/blink_rust/rusty/target/thumbv6m-none-eabi/release/librusty.a
# pull in common dependencies
#target_link_libraries(blink_rust pico_stdlib /home/bk/src/pico/pico-examples/blink_rust/super-blank-rust-pico-project/target/thumbv6m-none-eabi/debug/libsuper_blank_project.a)
target_link_libraries(blink_rust pico_stdlib /home/bk/src/pico/pico-examples/blink_rust/super-blank-rust-pico-project/target/thumbv6m-none-eabi/release/libsuper_blank_project.a)

# create map/bin/hex file etc.
pico_add_extra_outputs(blink_rust)

# add url via pico_set_program_url
example_auto_set_url(blink_rust)
