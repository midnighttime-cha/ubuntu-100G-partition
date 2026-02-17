# Ubuntu Partition for CIS
| Header 1 | Header 2 | Header 3 |
|---|---|---|
| Row 1, Col 1 | Row 1, Col 2 | Row 1, Col 3 |
| Row 2, Col 1 | Row 2, Col 2 | Row 2, Col 3 |
```
Partition	Mount Point	ขนาดแนะนำ	CIS Mount Options	ความสำคัญ
/	Root	20 GB	defaults	เก็บไฟล์ระบบหลัก
/boot	Boot	1 GB	defaults	แยกไฟล์ Kernel ออกมา
/home	User Data	15 GB	nodev	กันข้อมูลผู้ใช้เต็มแล้วระบบพัง
/var	Variable	15 GB	defaults	เก็บฐานข้อมูล/ไฟล์ที่เปลี่ยนแปลงบ่อย
/var/log	Logs	10 GB	defaults	สำคัญมาก: กัน Log เต็มจนระบบหยุดทำงาน
/var/log/audit	Audit Logs	5 GB	defaults	แยก Log ความปลอดภัยตามมาตรฐาน CIS
/tmp	Temp	5 GB	nodev,nosuid,noexec	ป้องกันการรัน Script อันตรายในโฟลเดอร์ชั่วคราว
/var/tmp	Var Temp	5 GB	nodev,nosuid,noexec	คล้าย /tmp แต่เก็บไฟล์นานกว่า
/dev/shm	Shared Mem	(RAM)	nodev,nosuid,noexec	ปรับแต่งผ่าน /etc/fstab
Free Space	LVM Free	~24 GB	-	เหลือไว้เผื่อขยาย (LVM Extend)
```
