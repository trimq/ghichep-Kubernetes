# Hiểu về Kubernetes

## Kubernetes là gì?

Kubernetes hay còn gọi là K8S là một phần trong hệ sinh thái container là một hệ thống mã nguồn mở để tự động hóa việc deploy, scalling và manage các ứng dụng chứa trong container. Kubernetes còn được hiểu là Container orchestration platform.

## Kubernetes nằm ở đâu trong hệ sinh thái container.

<img src="">

- Kubernetes là Container Orchestration Tool thuộc layer 4 trong hệ sinh thái container, các sản phẩm tương đương là Docker Swarm và Mesos

- Trong hệ sinh thái container, kubernetes nằm ở phía trên các container có nhiệm vụ điều phối các container.


## Một số keyword cần biết khi tìm hiểu:

- Container: Container là một process chạy trên VM, cho phép đóng gói các ứng dụng và triển khai các ứng dụng một cách nhanh chóng, hiệu quả hơn do không phụ thuộc nhiều vào phần cứng. Khác với ảo hóa của các VM, Container sẽ thực hiện ảo hóa phía trên OS thay vì ảo hóa phần cứng.

- Orchestration: Chỉ chung các nền tảng điều phối, cấu hình, quản lý phần mềm. Kubernetes là nền tảng Orchestration phổ biến nhất để quản lý container.

- Micro-services: Micro-services là kiến trúc chia nhỏ ứng dụng ra thành nhóm các services tương tác với nhau. Kiến trúc micro-services đối lập với kiến trúc triển khai ứng dụng một cách nguyên khối.

## Các thành phần của cụm Kubernetes

Một cụm Kubernetes gồm 2 thành phần chính

- Control Plane: Là thành phần điều khiển, điều phối lập lịch. Control plan thường sẽ chạy trên các node gọi là master node, lưu trữ dữ liệu trong etcd (key-value database). Bên cạnh etcd còn có các thành phần khác như kube-api server, kube-scheduler, kube-controller-manager, cloud-controller-manager.

- Worker Plane: Hay còn gọi là worker node là nơi để triển khai các ứng dụng, phần mềm. Worker node bao gồm các thành phần như kubelet, kube-proxy và Container Runtime (Docker)


## Một số thông tin thêm

- Kubernetes không phải là một ngôn ngữ lập trình hay một bộ ứng dụng. Kubernetes là cụm nơi các ứng dụng sẽ được triển khai trên đó.

- Kubernetes không phải là gói phần mềm hay file binary. Đó là một tập hợp các thành phần được cài đặt trên các node gọi là master node và worker node.

- Kubernetes cung cấp một số công cụ như kubeadm hay kubespray để thực thi các câu lệnh điều khiển cụm kubernetes.

- Cụm kubernetes có thể cài đặt trên on-premises server hoặc trên VM, trên bất kì cụm cloud nào của các provider. Google’s GKE, EKS by AWS, Azure Kubernetes Service là những cụm kubernetes được sử dụng rộng rãi nhất.

- Kubernetes được điều khiển bằng các câu lệnh kubectl. Kubectl sẽ thông qua các API giao tiếp với control plane để thực hiện các thay đổi trên cluster K8S. Kubectl có thể chạy trên Windows, Linux, MacOS. Kubectl sử dụng file kubeconfig để xác thực quyền điều khiển.

- Hiện nay một số công cụ như Rancher, RedHat OpenShift cung cấp giao diện UI đề điều khiển K8S.

- Để chạy được các ứng dụng cụm K8S, các ứng dụng đó cần phải được đóng gói thành các docker image. Các object của cụm kubernetes được khai báo trong file yaml.


## Các kiến thức cần chuẩn bị để làm việc với Kubernetes

### Linux:

- Quản lý file, phân quyền.

- Cấu trúc thư mục trong linux

- Các lệnh sao chép, sửa xóa file

- Các lệnh quản lý package, services, process.

- Một số lệnh khác: tar, curl ,wget,..


### Docker:

- Docker container, docker image.

- Các lệnh điều khiển container (docker run, stop, start, restart, exec, cp)

- Networking trong container.

- Tạo docker image với docker file

- Container registry

- Push và pull image từ container registry

### YAML: 

- Cần hiểu cú pháp yaml, array, maps.

### Kubernetes:

- Các thành phần trong Kubernetes.

- Nắm được các khái niệm: Pod, Deployment, Service, ingress, Volumes, PVC.

- Viết được các cú pháp yaml để tạo pods, deployments, services.

- Expose service ra bên ngoài (Ingress, Ingress controller)


## Cài đặt cluster Kubernetes

Một số cách cài đặt phổ biến:

- Cài đặt kubernetes qua kubeadm

- Cài đặt kubernetes qua kops chủ yếu là trên AWS.

- Cài đặt kubernetes bằng Kubespray dựa trên Ansible.

- OpenShift 





















