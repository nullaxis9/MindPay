# FR-1 Transaction Management · จดรายการ

**ผู้รับผิดชอบ:** พัชระพรชัย ค้าไป (@GitHub-newseoome-cymk)



## FR นี้แก้ปัญหาอะไร
ในฐานะผู้ใช้งาน เราต้องการสร้าง แก้ไข จัดหมวดหมู่ และ ลบ เพื่อให้ธุรกรรมการเงินของเรา
ถูกต้องและเป็นระเบียบ


## Requirement และเกณฑ์ผ่าน (Acceptance criteria)

*Requirement FR-1*

  ผู้ใช้เพิ่ม แก้ไข จัดหมวด และลบธุรกรรมของตนได้
  
  *Acceptance criteria*
  
  1.จํานวนเงินต้องมากกว่า 0 และมีทศนิยมไม่เกิน 2 ตําแหน่ง
  
  2.เก็บเงินเปนสตางค์ ผลรวมถูกต้อง 
  
  3.เลือกหมวดได้ และแนะนําหมวดจากชือร้าน
  
  4.เพิ่มเงินเข้าเองได้ง่าย: ปุ่ม "เพิ่มเงินเข้า" เปิดฟอร์มเป็นรายรับพร้อม
    จํานวนลัด (+฿100/500/1,000/5,000) เพราะเงินเข้ามักไม่มีสลิป
    
  5.รายการประจํารายเดือน (ค่าหอ ค่าเน็ต ค่าขนม): หาจากรายการเอง
    บอกวันครบกําหนดถัดไป
    
  6.เวลาลบต้องยืนยันก่อน และสามารถกดเลิกทําได้ 
  
  7.ผู้ใช้เห็นเฉพาะรายการของตัวเอง
  
  8.ช่องเงินเป็นเลขไทย ทศนิยมแบบลูกน้ำ คอมมา
    คั่นหลักพัน เพดาน ฿1,000,000,000 
    วันที่ / เวลาที่พิมพ์ บนเว็บแอปต้องถูกต้องก่อนบันทึก 


   

## ไฟล์ที่ฉันรับผิดชอบ

| [`src/domain/money.ts`](../../src/domain/money.ts) 
| [`src/domain/categories.ts`](../../src/domain/categories.ts) | 
| [`src/domain/recurring.ts`](../../src/domain/recurring.ts) | 
| [`src/domain/types.ts`](../../src/domain/types.ts) | 
| [`src/domain/__tests__/recurring.test.ts`](../../src/domain/__tests__/recurring.test.ts) | 
| [`src/data/repo.ts`](../../src/data/repo.ts) | 
| [`supabase/migrations/20260927000000_init.sql`](../../supabase/migrations/20260927000000_init.sql) | 
| [`supabase/migrations/20260927000100_harden.sql`](../../supabase/migrations/20260927000100_harden.sql) | 
| [`src/app/(tabs)/transactions.tsx`](../../src/app/%28tabs%29/transactions.tsx) |
| [`src/app/transaction.tsx`](../../src/app/transaction.tsx) | 
| [`src/ui/TxRow.tsx`](../../src/ui/TxRow.tsx) | 
| [`src/ui/inputs.tsx`](../../src/ui/inputs.tsx) | 
| [`src/ui/feedback.tsx`](../../src/ui/feedback.tsx) | 

## ทำงานยังไง

1. ตรวจจํานวนเงิน (parseBahtToSatang)
2. เดาหมวดจากชื่อ (suggestCategory)  
3. วันและเวลาแบบไทย

## การทดสอบ

Unit test: เงินและหมวด (domain.test.ts) 

Unit test: เงินทีผู้ใช้พิมพ์ (audit.test.ts TC-79) 

Unit test: รายการประจํา (recurring.test.ts TC-72) 

E2E: เพิ่ม แก้ ลบ เลิกทํา ในเบราว์เซอร์จริง 

เช็กลิสต์ทดสอบเองบนมือถือ (MT ในเอกสาร TRACEABILITY) 

## ข้อจำกัดและงานต่อไป


| ข้อจำกัด | ผลกระทบ | แก้ไขยังไง |
|---|---|---|
|recurring.ts ยังไม่ถูกแสดงใน | หน้าจอใด | ผู้ใช้ยังไม่เห็น "ค่าหอ อีก 2 วัน" (ตรรกะและเทสต์พร้อมแล้ว) | เพิ่มการ์ดบนหน้าหลักทีเรียกfindRecurring + upcomingRecurring |
