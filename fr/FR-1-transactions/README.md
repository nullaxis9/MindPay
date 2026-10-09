# FR-1 Transaction Management · จดรายการ

**ผู้รับผิดชอบ:** ✏️ ชื่อ-นามสกุล (@GitHub-username)
**ชุดงาน:** ชุดที่ 1

> ✏️ = ช่องที่ต้องเขียนเองด้วยคำของตัวเอง ลบเครื่องหมาย ✏️ ออกเมื่อเขียนเสร็จ
> อ่านประกอบ: หนังสือ `MindPay-FR1-Transaction-Management.pdf`

## FR นี้แก้ปัญหาอะไร

✏️ 3–5 บรรทัด: ผู้ใช้เจอปัญหาอะไร และ FR นี้ช่วยได้ยังไง

## Requirement และเกณฑ์ผ่าน (Acceptance criteria)

✏️ เขียนเป็นข้อ ๆ ว่าต้องทำอะไรได้บ้างจึงถือว่า FR นี้ผ่าน

## ไฟล์ที่ฉันรับผิดชอบ

| ไฟล์ | หน้าที่ (เขียนเอง 1 บรรทัด) |
|---|---|
| [`src/domain/money.ts`](../../src/domain/money.ts) | ✏️ |
| [`src/domain/categories.ts`](../../src/domain/categories.ts) | ✏️ |
| [`src/domain/recurring.ts`](../../src/domain/recurring.ts) | ✏️ |
| [`src/domain/types.ts`](../../src/domain/types.ts) | ✏️ |
| [`src/domain/__tests__/recurring.test.ts`](../../src/domain/__tests__/recurring.test.ts) | ✏️ |
| [`src/data/repo.ts`](../../src/data/repo.ts) | ✏️ |
| [`supabase/migrations/20260927000000_init.sql`](../../supabase/migrations/20260927000000_init.sql) | ✏️ |
| [`supabase/migrations/20260927000100_harden.sql`](../../supabase/migrations/20260927000100_harden.sql) | ✏️ |
| [`src/app/(tabs)/transactions.tsx`](../../src/app/%28tabs%29/transactions.tsx) | ✏️ |
| [`src/app/transaction.tsx`](../../src/app/transaction.tsx) | ✏️ |
| [`src/ui/TxRow.tsx`](../../src/ui/TxRow.tsx) | ✏️ |
| [`src/ui/inputs.tsx`](../../src/ui/inputs.tsx) | ✏️ |
| [`src/ui/feedback.tsx`](../../src/ui/feedback.tsx) | ✏️ |

## ทำงานยังไง

✏️ เล่าตั้งแต่ผู้ใช้กดปุ่ม จนถึงเห็นผลบนจอ ว่าข้อมูลผ่านไฟล์ไหนบ้าง

## การทดสอบ

✏️ เทสต์ไหนตรวจอะไร และรันยังไง (เช่น `npm test`)

## ข้อจำกัดและงานต่อไป

✏️ สิ่งที่ยังไม่ดี และสิ่งที่อยากทำต่อ (ดูไอเดียได้จากบท "ข้อจำกัด" ในหนังสือ)
