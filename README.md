# Kubeflow Weekly

## April 2, 2018 - April 8, 2018

Edited by: [@gaocegege][]

### Updates from Kubeflow

- [sidecar for envoy pod to keep IAP up to date](https://github.com/kubeflow/kubeflow/pull/552)

### Updates from tf-operator

- [Enable teardown cluster in CI](https://github.com/kubeflow/tf-operator/pull/520)

### Updates from Community

- :tada: [Repository about hyperparameter tuning](https://github.com/kubeflow/hp-tuning)
- :tada: [New demo: MNIST example using S3 for Training, Serving, and Tensorboard monitoring](https://github.com/kubeflow/examples/blob/master/mnist)

## March 26, 2018 - April 1, 2018

Edited by: [@gaocegege][]

### Updates from Kubeflow

- [Fixed a bug about tf-operator dashboard](https://github.com/kubeflow/kubeflow/pull/381)
> The frontend is now using hashRouter instead of browserRouter, meaning the location of the UI is determined only by the portion of the url after the # (similar to k8s dashboard).
>
> Request to the backend are also properly routed now.
The backend request are sent to the portion of the url until the first occurence of tfjobs + /api
i.e:
http://127.0.0.1:8001/api/v1/namespaces/kubeflow/services/ambassador:80/proxy/tfjobs/ui/#/new
will translate into: http://127.0.0.1:8001/api/v1/namespaces/kubeflow/services/ambassador:80/proxy/tfjobs/api
>
> This means this would break if we decide to route the dashboard with ambassador on /dashboard instead of /tfjob, so the route should be part of a dashboard config at some point.
- [Update images for our 0.1 release](https://github.com/kubeflow/kubeflow/pull/508)
- [Upgrade ks version to 0.9.2](https://github.com/kubeflow/kubeflow/pull/515)
- [Add parameter to mount path for notebook PVC](https://github.com/kubeflow/kubeflow/pull/469)
- [Add Central UI](https://github.com/kubeflow/kubeflow/pull/525)
- [Add TfJob dashboard to ksonnet](https://github.com/kubeflow/kubeflow/pull/548)

### Updates from tf-operator

- [**v1alpha1: Fix e2e test failures**](https://github.com/kubeflow/tf-operator/pull/501)
- [v1alpha1: Support testing on minikube](https://github.com/kubeflow/tf-operator/pull/485)
- [v1alpha1: Add proxying to front-end development server](https://github.com/kubeflow/tf-operator/pull/442)
- [v1alpha1: Add a hack to create example TFJob config](https://github.com/kubeflow/tf-operator/pull/509)
- [**v1alpha1: Don't leave pods running when a job completes**](https://github.com/kubeflow/tf-operator/pull/512)
- [**v1alpha2: Support condition in TFJobStatus and add corresponding test cases**](https://github.com/kubeflow/tf-operator/pull/504)
- [v1alpha2: Check running status more gracefully](https://github.com/kubeflow/tf-operator/pull/507)
- Add [@mitake][] as reviewer :tada:

### Updates from Community

- [A coming proposal for Kubeflow cli](https://github.com/kubeflow/kubeflow/issues/522)
- [Demo show: Reinforcement Learning with tensorflow/agents](https://github.com/kubeflow/examples/tree/master/agents)
- [Discussion about Kubeflow logo](https://github.com/kubeflow/kubeflow/issues/187)

[@gaocegege]: https://github.com/gaocegege
[@mitake]: https://github.com/mitake
