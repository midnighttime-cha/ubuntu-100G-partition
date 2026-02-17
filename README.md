# ตัวอย่างการแบ่ง Partition สำหรับ Ubuntu อ้างอิงขนาด HDD 100GB
| Partition	| Mount Point | ขนาดแนะนำ | CIS Mount Options | ความสำคัญ |
|---|---|---|---|---|
| / |	Root | 20GB | defaults | เก็บไฟล์ระบบหลัก |
| /boot | Boot | 2GB | defaults | แยกไฟล์ Kernel ออกมา |
| /home | User Data | 15GB | nodev | กันข้อมูลผู้ใช้เต็มแล้วระบบพัง |
| /var | Variable | 15GB | defaults | เก็บฐานข้อมูล/ไฟล์ที่เปลี่ยนแปลงบ่อย |
| /var/log | Logs | 10GB | defaults | สำคัญมาก: กัน Log เต็มจนระบบหยุดทำงาน |
| /var/log/audit | Audit Logs | 5GB | defaults | แยก Log ความปลอดภัยตามมาตรฐาน CIS |
| /tmp | Temp | 5GB | nodev,nosuid,noexec | ป้องกันการรัน Script อันตรายในโฟลเดอร์ชั่วคราว |
| /var/tmp | Var Temp | 5GB | nodev,nosuid,noexec | คล้าย /tmp แต่เก็บไฟล์นานกว่า |
| /dev/shm | Shared Mem |	(RAM) | nodev,nosuid,noexec | ปรับแต่งผ่าน /etc/fstab |
| Free Space | LVM Free	| ~24 GB | - | เหลือไว้เผื่อขยาย (LVM Extend) |
