# soft-roce installation
sudo dnf install libibverbs libibverbs-utils librdmacm rdma-core perftest
sudo modprobe rdma_rxe // or permannently added in modules-load.d/rdma.conf

# create rdma device
sudo rdma link add rxe0 type rxe netdev enp1s0

# rc pingpong test
Server: ibv_rc_pingpong -d rxe0 -g 0
Client: ibv_rc_pingpong -d rxe0 -g 0 192.168.124.162
