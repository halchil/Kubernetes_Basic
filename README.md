# Kubernetes_Basic

[Kunbernetes Document](https://kubernetes.io/docs/setup/production-environment/container-runtimes/)

以下のようにドキュメントに移動する。
![fig](./img/fig1.png)


# ストリーム基礎

## control-plane と workerの基礎を記述できるか？
参照 Udemy Kunbernetes基礎

Desired State app.yaml等の状態とKubernetesクラスタの概要を記述する。

## Kubernetes Architecture

### Worker Node
kubelet
kube proxy

### Control plane
kube-apiserver
etcd
kube-scheduler
kube-control-manager
kube-cloud-manage

その他
kubectl

# Configについて


$HOME/.kube/configに記載されている
Kubernetes の kubectl コマンドが「どのクラスタに、どのユーザーで、どの認証情報を使って接続するか」を知るための設定ファイル

なんで別のユーザーになるの？
Kubernetesは、OSユーザーとは無関係にクラスタ内部のアクセス制御（RBAC）をしているから。


kubectl における「ユーザー」とは？

Linuxのログインユーザー（たとえば mainte）とは別物で、
Kubernetesクラスタ内で使う「認証ユーザー（kubernetes-adminなど）」のこと。


主に3つの領域 culuster user 両方

less .kube/config | less
mainte@kube-control-plane:~$ kubectl config current-context
kubernetes-admin@kubernetes


# kubectlについて

https://kubernetes.io/docs/reference/kubectl/

# api-resources

# 出力フォーマット
wide
yaml
name
json