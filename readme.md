# ☁ AWS Elastic Block Store (EBS) → Snapshots
## 🚀 Steps:
#### 1. Launch Instance In N. Virginia Region:
![](/img/1%20(2).png)


#### 2. Connect EC2 Using SSH:
![](/img/3%20(2).png)
 Make A Folder And Files Inside Project Folder:
 ![](/img/4%20(2).png)


#### 3. Create & Attach Volume EBS:
![](/img/5%20(2).png)
![](/img/6%20(2).png)
![](/img/7%20(2).png)
![](/img/8%20(2).png)

##### 3.1 See The List All Block Storage Devices:
    lsblk

![](/img/9%20(2).png)
    
##### 3.2 Make Disk Partitions:
![](/img/10%20(2).png)
##### 3.3 Check List All Block Storage Devices:
    lsblk
![](/img/11%20(2).png)

##### 3.4 Created A Filesystem (XFS) On Your Partition Disk Is Ready ToStore Data:
    sudo mkfs.xfs /dev/nvme1n1p1
![](/img/12%20(2).png)
##### 3.5 Edit The System’s Filesystem Table:
    sudo vim /etc/fstab
![](/img/14.png)
##### 3.6 Now Mount EBS And Create A Folder:
![](/img/15%20(2).png)

#### 4.Launch New Instance In Mumbai Region:
![](/img/17%20(2).png)
![](/img/16%20(2).png)
![](/img/18%20(2).png)

#### 5. Go To Volume And Create Snapshot:

##### 5.1 Action → Create Snapshot:
![](/img/19%20(2).png)

##### 5.2 Go To Snapshots:
![](/img/20.png)

##### 5.3 Now Copy This Snapshot To Mumbai Region:
![](/img/21.png)

##### 5.4 Check snapshopt in mumbai region:
![](/img/21.png)

##### 5.5 Create Volume From Snapshot. Action → Create Volume FromSnapshot:
![](/img/22.png)

##### 5.5 Check In Volumes & Attach:
![](/img/23.png)
![](/img/24.png)
##### 5.6Check List Block Storage:
    lsblk
![](/img/25.png)

##### 5.7 Edit The System’s Filesystem Table:
![](/img/26.png)

##### 5.8 Make Project Folder:
![](/img/27.png)

##### 5.9 Mount EBS Volume:
    sudo mount /home/ec2-user/project
![](/img/29.png)
#### 6.Check The Files:
![](/img/30.png)