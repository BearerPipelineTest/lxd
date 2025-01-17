# How to run

To run all tests, including the Go tests, run from repository root:

    sudo -E make check

To run only the integration tests, run from the test directory:

    sudo -E ./main.sh

# Environment variables

Name                            | Default                   | Description
:--                             | :---                      | :----------
LXD\_BACKEND                    | dir                       | What backend to test against (btrfs, ceph, dir, lvm, zfs, or random)
LXD\_CEPH\_CLUSTER              | ceph                      | The name of the ceph cluster to create osd pools in
LXD\_CEPH\_CEPHFS               | ""                        | The cephfs filesystem to use for `cephfs` pools.
LXD\_CEPH\_CEPHOBJECT\_RADOSGW  | ""                        | The radosgw HTTP endpoint to use for `cephobject` pools.
LXD\_CONCURRENT                 | 0                         | Run concurrency tests, very CPU intensive
LXD\_DEBUG                      | 0                         | Run lxd, lxc and the shell in debug mode (very verbose)
LXD\_INSPECT                    | 0                         | Don't teardown the test environment on failure
LXD\_LOGS                       | ""                        | Path to a directory to copy all the LXD logs to
LXD\_OFFLINE                    | 0                         | Skip anything that requires network access
LXD\_SKIP\_STATIC               | ""                        | Skip static analysis tests
LXD\_TEST\_IMAGE                | "" (busybox test image)   | Path to an image tarball to use instead of the default busybox image
LXD\_TMPFS                      | 0                         | Sets up a tmpfs for the whole testsuite to run on (fast but needs memory)
LXD\_NIC\_SRIOV\_PARENT         | ""                        | Enables SR-IOV NIC tests using the specified parent device
LXD\_IB\_PHYSICAL\_PARENT       | ""                        | Enables Infiniband physical tests using the specified parent device
LXD\_IB\_SRIOV\_PARENT          | ""                        | Enables Infiniband SR-IOV tests using the specified parent device
LXD\_NIC\_BRIDGED\_DRIVER       | ""                        | Specifies bridged NIC driver for tests (either native or openvswitch, defaults to native)

