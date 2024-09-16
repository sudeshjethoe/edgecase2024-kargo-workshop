FROM mcr.microsoft.com/devcontainers/base:debian

COPY --from=ghcr.io/charmbracelet/gum /usr/local/bin/gum /usr/local/bin/gum

RUN curl -L -o kargo https://github.com/akuity/kargo/releases/download/v0.8.5/kargo-linux-amd64
RUN chmod +x kargo
RUN mv kargo /usr/local/bin/kargo

RUN git clone https://github.com/ahmetb/kubectx /opt/kubectx
RUN ln -s /opt/kubectx/kubectx /usr/local/bin/kubectx
RUN ln -s /opt/kubectx/kubens /usr/local/bin/kubens

ENV CERT_MANAGER_VERSION="1.15.3"
ENV ARGOCD_VERSION="7.4.4"
ENV ARGO_ROLLOUTS_VERSION="2.37.5"
ENV KARGO_VERSION="0.8.7"
ENV GITOPS_REPO_URL="https://github.com/basbremer/kargo-demo.git"
