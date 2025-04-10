# soft-roce installation
sudo dnf install libibverbs libibverbs-utils librdmacm rdma-core perftest
sudo modprobe rdma_rxe // or permannently added in modules-load.d/rdma.conf

# create rdma device
sudo rdma link add rxe0 type rxe netdev enp1s0

