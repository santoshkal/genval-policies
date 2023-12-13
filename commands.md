
# Test Commands

# Dockerfile URL
```shell
go run ./cmd/main.go --mode container --reqinput https://raw.githubusercontent.com/santoshkal/genval-policies/main/inputs/dockerfile_input/clang_input.json \
--output ./Dockerfile \
--inputpolicy https://raw.githubusercontent.com/santoshkal/genval-policies/main/default-policies/rego/inputfile_policies.rego \
--outputpolicy https://raw.githubusercontent.com/santoshkal/genval-policies/main/default-policies/rego/dockerfile_policies.rego
```

# Dockerfile Local FS
```shell
go run ./cmd/main.go --mode container --reqinput ./templates/inputs/dockerfile_input/clang_input.json \
--output ./Dockerfile-test \
--inputpolicy ./templates/defaultpolicies/rego/inputfile_policies.rego \
--outputpolicy ./templates/defaultpolicies/rego/dockerfile_policies.rego
```

# CUE URL Single policy
```shell
go run ./cmd/main.go --mode cue --reqinput https://raw.githubusercontent.com/santoshkal/genval-policies/main/inputs/cue/deploy.json \
--resource Deployment \
--policy https://raw.githubusercontent.com/santoshkal/genval-policies/main/default-policies/cue/deployment.cue \
--policy https://raw.githubusercontent.com/santoshkal/genval-policies/main/default-policies/cue/metadata.cue 
```

# CUE Local FS Single **policy**
```shell
go run ./cmd/main.go --mode cue --reqinput ./templates/inputs/cue/deploy.json \
--resource Deployment \
--policy ./templates/defaultpolicies/cue/deployment.cue
```

# CUE URL with multiple input and Multiple policies
```shell
go run ./cmd/main.go --mode cue --reqinput https://raw.githubusercontent.com/santoshkal/genval-policies/main/inputs/cue/k8s \
--resource Deployment \
--policy https://raw.githubusercontent.com/santoshkal/genval-policies/main/default-policies/cue/deployment.cue \
--policy https://raw.githubusercontent.com/santoshkal/genval-policies/main/default-policies/cue/metadata.cue
```

# CUE with Local FS multiple inputs and multiple policies
```shell
go run ./cmd/main.go --mode cue --reqinput ./templates/inputs/cue/deploy.json \
--resource Deployment \
--policy ./templates/defaultpolicies/cue/deployment.cue \
--policy ./templates/defaultpolicies/cue/metadata.cue
```
# Terraform with URL
```shell
go run ./cmd/main.go --mode tf --reqinput https://raw.githubusercontent.com/santoshkal/genval-policies/main/inputs/terraform/sec_group.tf \
--policy https://raw.githubusercontent.com/santoshkal/genval-policies/main/default-policies/rego/terraform.rego
```


# Terraform with Local FS
```shell
go run ./cmd/main.go --mode tf --reqinput ./templates/inputs/terraform/sec_group.tf \
--policy ./templates/defaultpolicies/rego/terraform.rego
```

# Kubernetes manifests with URL
```shell
go run ./cmd/main.go --mode k8s --reqinput https://raw.githubusercontent.com/santoshkal/genval-policies/main/inputs/k8s/deployment.json \
--policy https://raw.githubusercontent.com/santoshkal/genval-policies/main/default-policies/rego/k8s.rego
```

# Kubernetes manifests with Local FS
```shell
go run ./cmd/main.go --mode k8s --reqinput ./templates/inputs/k8s/deployment.json \
--policy ./templates/defaultpolicies/rego/k8s.rego
```

# CEL with URL
```shell
go run ./cmd/main.go --mode cel --reqinput https://raw.githubusercontent.com/santoshkal/genval-policies/main/inputs/k8s/deployment.json \
--policy https://raw.githubusercontent.com/santoshkal/genval-policies/main/default-policies/cel/cel_policies
```

# CEL with Local FS
```shell
go run ./cmd/main.go --mode cel --reqinput ./templates/inputs/k8s/deployment.json \
--policy ./templates/defaultpolicies/cel/cel_policies
```

# ShowJSON Helper with URL
```shell
go run ./cmd/main.go --mode showjson --reqinput https://raw.githubusercontent.com/santoshkal/genval-policies/main/inputs/terraform/sec_group.tf
```
# ShowJSON Helper with Local FS
```shell
go run ./cmd/main.go --mode showjson --reqinput ./templates/inputs/terraform/sec_group.tf
```
