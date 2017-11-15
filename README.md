# rpi-server
rpi-server implementation in C (Experimental)

- Run `make` to build and test the program.

## APIs
- `pthread_t ems_run_server(int port_server, void (*handler)(char *, int))` - Runs a server that listens to incoming connections on `port_server`. `handler` is invoked when there is an incoming packet.
- `int ems_send(struct rpi_i *p)` - Used to send a packet on all TCP sockets created via the server.
- `int ems_destroy(pthread_t s)` - To release resources and terminate the server.
- `ems_send2()`, `ems_test_run_client()` - Used for unit testing.

See `server.h` and `server.c` for more details.
