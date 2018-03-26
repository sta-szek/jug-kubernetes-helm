## kubernetes + helm

---

## what is helm

- helm -- package manager for kubernetes |
- chart -- template for kubernetes resources |
- release -- installed chart |
- values -- environment specific properties |
- helm client -- command line tool |
- tiller server -- in-cluster deployment, communicate with k8s api |

---

## key concepts

- configurable and repeatable releases |
- one manifest for all deployment environments |
- preconfigured charts |
- manage release cycle of charts |

---

## how to install

```bash
https://raw.githubusercontent.com/kubernetes/helm/master/scripts/get | bash
helm init
```

---

## first chart

`helm create first-chart`

---?code=sample/first-chart&lang=bash

@[1-9](Main chart directory, contains chart description, default values, .helmignore)
@[6]
@[7]
@[9]
@[5,8]
@[11-14](Charts we depend on)
@[16-24](Templates (kubernetes resources), notes, helper functions)
@[20,22,24]
@[21]
@[23]

---?code=sample/first-chart-env&lang=bash

@[5-7]

---
## overriding template defaults

- helm install --values=path/to/values.yaml |
- helm install --set key1=value1,key2=value2 |

---

## debug chart

- helm lint |
- helm install --dry-run --debug |
- helm get manifest |

---

## oneliner

```bash
helm upgrade --install \
             --values=values.yaml \ 
             chart-name \
             path/to/chart-name
```
---

## misc

- [docs.helm.sh @fa[external-link fa-pad-left]](https://docs.helm.sh)
- [docs.helm.sh/related @fa[external-link fa-pad-left]](https://docs.helm.sh/related)
- [hub.kubeapps.com @fa[external-link fa-pad-left]](https://hub.kubeapps.com)
- [gitkube.sh @fa[external-link fa-pad-left]](https://gitkube.sh)
- [github.com/gitpitch/gitpitch/wiki @fa[external-link fa-pad-left]](https://github.com/gitpitch/gitpitch/wiki)

---?image=assets/image/gitpitch-audience.jpg&opacity=100

### Questions?

@fa[github](github.com/sta-szek)

@fa[envelope](p.jonski@pojo.pl)

@fa[slack](jvm-poland.slack.com >> pojo)
