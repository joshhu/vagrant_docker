# 中原大學Docker課程

## 單機環境設定

### 將Ubuntu 16.04更新到最新

```
sudo apt-get update
sudo apt-get upgrade
```
### 安裝 Docker

使用最方便的script方式，這是Ubuntu的優勢。之後將使用者加入docker群組。

```
curl -fsSL get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker $USER
sudo apt-get update
sudo apt-get upgrade
```
