**Container Lifecycle**

* `docker run -d -p <host_port>:<container_port> --name <name> <image>` : สร้างและรัน Container ในเบื้องหลัง (Background Mode)
* `docker run -it <image> /bin/bash` : รัน Container และเปิด Interactive Terminal เข้าไปควบคุมด้านในทันที
* `docker ps` : ดูเฉพาะ Container ที่กำลังทำงานอยู่
* `docker ps -a` : ดู Container ทั้งหมด (รวมตัวที่หยุดทำงานแล้ว)
* `docker start <container>` : สั่งให้ Container เริ่มทำงาน
* `docker stop <container>` : สั่งหยุดการทำงานของ Container
* `docker restart <container>` : รีสตาร์ต Container
* `docker rm <container>` : ลบ Container (ต้อง stop ก่อน)
* `docker rm -f <container>` : บังคับลบ Container ทันทีแม้กำลังทำงานอยู่
* `docker exec -it <container> sh` : รีโมตเปิด Shell เข้าไปทำงานภายใน Container ที่กำลังรันอยู่

**Image Management**

* `docker images` : ดูรายชื่อ Image ทั้งหมดที่มีในเครื่อง
* `docker pull <image>:<tag>` : ดาวน์โหลด Image มาจาก Docker Hub
* `docker build -t <name>:<tag> .` : สั่ง Build Image จากไฟล์ `Dockerfile` ในโฟลเดอร์ปัจจุบัน
* `docker rmi <image>` : ลบ Image ออกจากเครื่อง
* `docker tag <source_image> <target_image>` : ตั้งชื่อหรือสร้าง Tag ใหม่ให้ Image

**Logs & Monitoring**

* `docker logs <container>` : แสดงประวัติ Log ทั้งหมดของ Container
* `docker logs -f <container>` : แสดง Log แบบเรียลไทม์ (Follow mode)
* `docker stats` : แสดงการใช้ทรัพยากร (CPU, RAM, Network I/O) ของทุก Container แบบเรียลไทม์
* `docker top <container>` : แสดง Process ที่กำลังทำงานอยู่ภายใน Container
* `docker inspect <container/image>` : ดูข้อมูลคอนฟิกและ IP Address แบบละเอียดในรูปแบบ JSON

**Volumes & Networks**

* `docker volume ls` : แสดง Volume สำหรับเก็บข้อมูลทั้งหมด
* `docker volume create <name>` : สร้าง Volume ใหม่
* `docker volume rm <name>` : ลบ Volume
* `docker network ls` : แสดง Network ภายใน Docker
* `docker network create <name>` : สร้าง Virtual Bridge Network ใหม่
* `docker network connect <network> <container>` : นำ Container เข้าไปเชื่อมต่อกับ Network ที่ระบุ

**System Cleanup**

* `docker system df` : ตรวจสอบพื้นที่ฮาร์ดดิสก์ที่ Docker ใช้งานทั้งหมด
* `docker container prune -f` : ลบ Container ที่หยุดทำงานทั้งหมดทิ้งทันที
* `docker image prune -a -f` : ลบ Image ที่ไม่ได้ถูกเรียกใช้งานทั้งหมด
* `docker system prune -a --volumes -f` : ล้างขยะระบบทั้งหมด (Container ที่หยุด, Image ที่ไม่ได้ใช้ และ Volume ตกค้าง)

**Docker Compose**

* `docker compose up -d` : อ่านไฟล์ `docker-compose.yml` และรันทุก Service ในเบื้องหลัง
* `docker compose down` : สั่งหยุดและลบ Container รวมถึง Network ของโปรเจกต์ออก
* `docker compose ps` : ดูสถานะ Service ทั้งหมดในไฟล์ Compose
* `docker compose logs -f` : ดู Log รวมของทุก Service แบบเรียลไทม์