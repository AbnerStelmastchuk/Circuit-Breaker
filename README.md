# Circuit-Breaker

Steps (
    step 1(
        Create any example web server
    )
    step 2(
        Create a Dockerfile and build this image
    )
    step 3(
        Using kubenertes with Rancher
        Create a k3d cluster
        https://www.suse.com/c/rancher_blog/set-up-k3s-in-high-availability-using-k3d/
    )
    step 4(
        Create Istio & kiali: https://istio.io/latest/docs/setup/getting-started/
    )
    step 5(
        Create Istio Fortio: https://istio.io/latest/docs/tasks/traffic-management/circuit-breaking/
    )
    step 6(
        Commands: kubectl exec <Your-Pod-Name-Fortio> -c fortio -- /usr/bin/fortio load -c 3 -qps 0 -n 2000 -loglevel Warning http://Your-Service

        My Commands: kubectl exec fortio-deploy-5669d4866b-kwl7d -c fortio -- /usr/bin/fortio load -c 3 -qps 0 -n 2000 -loglevel Warning http://servicex-service
    )
)
