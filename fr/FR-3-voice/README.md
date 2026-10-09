# FR-3 Voice Entry · พูดจด

**ผู้รับผิดชอบ:** ✏️ ชื่อ-นามสกุล (@GitHub-username)
**ชุดงาน:** ชุดที่ 2

> ✏️ = ช่องที่ต้องเขียนเองด้วยคำของตัวเอง ลบเครื่องหมาย ✏️ ออกเมื่อเขียนเสร็จ
> อ่านประกอบ: หนังสือ `MindPay-FR3-Voice-Entry.pdf`

## FR นี้แก้ปัญหาอะไร

✏️ 3–5 บรรทัด: ผู้ใช้เจอปัญหาอะไร และ FR นี้ช่วยได้ยังไง

## Requirement และเกณฑ์ผ่าน (Acceptance criteria)

✏️ เขียนเป็นข้อ ๆ ว่าต้องทำอะไรได้บ้างจึงถือว่า FR นี้ผ่าน

## ไฟล์ที่ฉันรับผิดชอบ

| ไฟล์ | หน้าที่ (เขียนเอง 1 บรรทัด) |
|---|---|
| [`src/domain/voice.ts`](../../src/domain/voice.ts) | ✏️ |
| [`src/domain/__tests__/voice.test.ts`](../../src/domain/__tests__/voice.test.ts) | ✏️ |
| [`src/services/speech.ts`](../../src/services/speech.ts) | ✏️ |
| [`src/services/speech.web.ts`](../../src/services/speech.web.ts) | ✏️ |
| [`src/app/voice.tsx`](../../src/app/voice.tsx) | ✏️ |

### ส่วนกลางที่ฉันดูแลเพิ่ม (ไม่ใช่ของ FR นี้โดยตรง)

- **ชุดเทสต์ตรวจบั๊กทั้งแอป (TC-79 ถึง TC-89)** (1 ไฟล์): `src/domain/__tests__/audit.test.ts`
- **ระบบบัญชีผู้ใช้** (14 ไฟล์): `src/domain/auth.ts`, `src/domain/__tests__/auth.test.ts`, `src/data/authLinks.ts`, `src/data/supabase.ts`, `src/data/storage.ts`, `src/data/storage.web.ts`, `src/data/sessionStorageSetup.ts`, `src/data/sessionStorageSetup.web.ts`, `src/app/welcome.tsx`, `src/app/onboarding.tsx`, `src/ui/AuthNotice.tsx`, `src/ui/StepDots.tsx`, `src/ui/LaunchIntro.tsx`, `docs/SUPABASE_AUTH_SETUP.md`
- **Design System** (9 ไฟล์): `src/ui/theme.ts`, `src/ui/themeMode.ts`, `src/ui/components.tsx`, `src/ui/effects.tsx`, `src/ui/motion.ts`, `src/ui/nav.ts`, `src/ui/ThemePicker.tsx`, `src/ui/__tests__/theme.test.ts`, `docs/DESIGN_SYSTEM.md`

## ทำงานยังไง

✏️ เล่าตั้งแต่ผู้ใช้กดปุ่ม จนถึงเห็นผลบนจอ ว่าข้อมูลผ่านไฟล์ไหนบ้าง

## การทดสอบ

✏️ เทสต์ไหนตรวจอะไร และรันยังไง (เช่น `npm test`)

## ข้อจำกัดและงานต่อไป

✏️ สิ่งที่ยังไม่ดี และสิ่งที่อยากทำต่อ (ดูไอเดียได้จากบท "ข้อจำกัด" ในหนังสือ)
