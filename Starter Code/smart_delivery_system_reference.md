# Smart Delivery System - Freelance Roadmap

خطة تنفيذ المشروع خطوة بخطوة كأنه مشروع حقيقي لعميل

---

## 0. الهدف من الملف

الملف ده هو الخريطة العملية لتنفيذ مشروع:

```text
Smart Delivery Locker System
```

كأنك شغال فريلانس مع عميل حقيقي.

الفكرة مش إنك تبدأ كود مباشرة. الفكرة إنك تمشي بمراحل واضحة:

```text
فهم -> توثيق -> تصميم -> تنفيذ -> اختبار -> تسليم -> صيانة
```

كل مرحلة في الملف فيها:

- الهدف من المرحلة.
- تعمل إيه بالضبط.
- تسلم إيه في نهاية المرحلة.
- إمتى تعتبر المرحلة خلصت.
- أخطاء لازم تتجنبها.

---

## 1. ملخص المشروع

المشروع عبارة عن نظام خزائن ذكية لاستلام طلبات المتاجر الإلكترونية.

العميل يطلب order من تطبيق موبايل، والمندوب يضع الطلب داخل درج مقفول في ماكينة تشبه ATM، وبعدها العميل يستلم QR Code ويفتح الدرج الخاص به فقط.

المشروع يتكون من:

```text
Mobile App
Backend API
Admin Dashboard
Smart Locker Machine
QR Code Security
Database
Testing
Deployment
```

---

## 2. طريقة التفكير كفريلانسر

أنت مش بتبيع كود فقط.

أنت بتبيع حل لمشكلة.

العميل لا يهتم إنك استخدمت Django أو Flutter فقط. العميل يهتم أن:

- الطلبات تتسجل.
- المندوب يعرف يودع الطلب.
- العميل يعرف يستلم الطلب.
- الدرج الصحيح يفتح.
- البيانات آمنة.
- النظام واضح وسهل الاستخدام.
- في حالة مشكلة، يعرف يتابعها من dashboard.

لذلك لازم تفكر بهذه الطريقة:

```text
Problem -> Solution -> Workflow -> System -> Code
```

مش:

```text
Code -> Features -> نحاول نفهم بعدين
```

---

## 3. الصورة الكبيرة للمراحل

المشروع يمشي بالمراحل التالية:

```text
Phase 1: Client Discovery
Phase 2: Scope & MVP
Phase 3: Requirements Documentation
Phase 4: System Design
Phase 5: Contract, Timeline, and Pricing
Phase 6: Project Setup
Phase 7: Backend Development
Phase 8: Mobile App Development
Phase 9: Locker Hardware or Simulation
Phase 10: Integration
Phase 11: Testing
Phase 12: User Acceptance Testing
Phase 13: Deployment
Phase 14: Handover
Phase 15: Maintenance and Future Work
```

---

# Phase 1: Client Discovery

## الهدف

تفهم العميل عايز إيه، والمشكلة الحقيقية فين، ومن هم المستخدمون، وما النتيجة التي يتوقعها.

في مشروعك، العميل ممكن يكون:

- صاحب متجر إلكتروني.
- براند ساعات.
- شركة عندها طلبات كثيرة.
- جامعة أو كومباوند يريد نظام استلام ذكي.

## تعمل إيه؟

تعمل meeting أو جلسة أسئلة مع العميل.

تسأله:

- ما نوع المنتجات التي سيتم بيعها؟
- من المستخدم النهائي؟
- هل العميل يطلب من التطبيق أم من موقع؟
- هل يوجد مندوبون تابعون للشركة؟
- أين سيتم وضع الماكينة؟
- كم درج في الماكينة؟
- هل هناك أحجام مختلفة للطلبات؟
- هل الدفع مطلوب في النسخة الأولى؟
- هل يريد تطبيق للعميل فقط أم للعميل والمندوب؟
- هل يريد dashboard للأدمن؟
- هل المطلوب hardware حقيقي أم simulation؟
- ما موعد التسليم؟
- ما أهم 3 features بالنسبة له؟

## أسئلة خاصة بمشروع Smart Delivery

- هل العميل يختار locker بنفسه؟
- هل النظام يقترح أقرب locker؟
- كم مدة بقاء الطلب في الدرج؟
- ماذا يحدث لو العميل لم يستلم؟
- هل المندوب يفتح الدرج باستخدام QR؟
- هل العميل يفتح الدرج باستخدام QR؟
- هل نحتاج إثبات استلام؟
- هل نحتاج emergency unlock؟
- هل نحتاج logs لكل عملية فتح درج؟

## المخرجات

تطلع من المرحلة دي بوثيقة قصيرة اسمها:

```text
Project Brief
```

محتواها:

- وصف المشكلة.
- وصف الحل.
- المستخدمون.
- أهم features.
- القيود.
- توقعات العميل.

## إمتى تعتبر المرحلة خلصت؟

لما تقدر تشرح المشروع لشخص آخر في دقيقتين بدون لخبطة.

## أخطاء تتجنبها

- تبدأ كود قبل ما تفهم المشكلة.
- تفترض features من دماغك بدون تأكيد.
- توافق على كل حاجة يقولها العميل بدون تحديد scope.
- تنسى تسأل عن الهاردوير والدفع والصلاحيات.

---

# Phase 2: Scope & MVP

## الهدف

تحدد ما الذي سيتم تنفيذه في أول نسخة، وما الذي سيتم تأجيله.

دي أهم مرحلة في الفريلانس، لأنها تمنع جملة:

```text
طب ممكن نزود حاجة صغيرة؟
```

التي تتحول غالبًا إلى شغل كبير بدون مقابل.

## الـ MVP الخاص بمشروعك

النسخة الأولى يجب أن تثبت الفلو الأساسي:

```text
Customer Order -> Courier Deposit -> Locker Storage -> Customer Pickup
```

## Features داخل الـ MVP

### Authentication

- تسجيل دخول.
- JWT.
- أدوار المستخدمين:

```text
customer
courier
admin
locker_device
```

### Products

- عرض المنتجات.
- تفاصيل المنتج.
- إدارة المنتجات من الأدمن.

### Orders

- العميل يعمل order.
- العميل يرى طلباته فقط.
- حالة الطلب تتغير عبر مراحل واضحة.

### Locker

- اختيار locker.
- أدراج بأحجام:

```text
small
medium
large
```

- معرفة الدرج الفاضي والمشغول.

### QR

- QR للمندوب لإيداع الطلب.
- QR للعميل للاستلام.
- QR له صلاحية.
- QR يستخدم مرة واحدة.

### Courier

- يرى الطلبات المخصصة له.
- يودع الطلب في درج.
- يؤكد الإيداع.

### Customer Pickup

- يحصل على pickup QR.
- يعمل scan على الماكينة.
- الدرج الصحيح يفتح.

### Admin Dashboard

- إدارة المنتجات.
- إدارة الطلبات.
- إدارة الماكينات.
- إدارة الأدراج.
- رؤية logs.
- emergency unlock.

### Testing

- اختبارات للصلاحيات.
- اختبارات للـ QR.
- اختبارات لحالات الطلب.

## خارج الـ MVP

لا تنفذ في أول نسخة:

- Payment gateway حقيقي.
- AI recommendations.
- كاميرا proof image.
- شركات شحن خارجية.
- تطبيق iOS production كامل لو الوقت ضيق.
- Offline locker mode.
- multi-vendor marketplace.
- خرائط متقدمة.

## المخرجات

ملف اسمه:

```text
MVP Scope Document
```

فيه:

- داخل النطاق.
- خارج النطاق.
- assumptions.
- constraints.

## إمتى تعتبر المرحلة خلصت؟

لما يكون عندك قائمة features محددة والعميل موافق عليها.

## أخطاء تتجنبها

- تخلي المشروع واسع جدًا.
- تدخل AI بدري.
- تدخل payment حقيقي قبل ما الفلو الأساسي يشتغل.
- تبدأ hardware قبل ما الـ backend flow يبقى واضح.

---

# Phase 3: Requirements Documentation

## الهدف

تحويل الكلام إلى متطلبات مكتوبة.

الوثيقة دي اسمها:

```text
SRS - Software Requirements Specification
```

## تعمل إيه؟

تكتب كل شيء يجب أن يفعله النظام.

## أقسام الـ SRS

### 1. مقدمة

- اسم المشروع.
- الهدف.
- المشكلة.
- الحل.

### 2. المستخدمون

```text
Customer
Courier
Admin
Locker Machine
```

### 3. Functional Requirements

أمثلة:

```text
FR-001: Customer can register and login.
FR-002: Customer can view products.
FR-003: Customer can create an order.
FR-004: Customer can view only his own orders.
FR-005: Courier can view assigned orders only.
FR-006: Admin can manage lockers and drawers.
FR-007: Locker machine can validate QR token with backend.
FR-008: System opens only the drawer assigned to the order.
```

### 4. Non-Functional Requirements

أمثلة:

```text
NFR-001: QR token must expire after 48 hours.
NFR-002: QR token must be single-use.
NFR-003: All drawer open events must be logged.
NFR-004: System must return API response within reasonable time.
NFR-005: Production environment must use HTTPS.
```

### 5. User Stories

أمثلة:

```text
As a customer, I want to choose a locker, so I can pick up my order from a convenient location.
```

```text
As a courier, I want to scan a deposit QR, so I can open the correct drawer and store the order.
```

```text
As an admin, I want to see drawer logs, so I can investigate support issues.
```

### 6. Acceptance Criteria

مثال:

Feature: Customer pickup

```text
Given the order is Ready_For_Pickup
And the pickup QR is valid
When the customer scans the QR
Then the correct drawer opens
And the order status becomes Picked_Up
And an event log is created
```

## المخرجات

ملف:

```text
SRS.md
```

أو:

```text
SRS.pdf
```

## إمتى تعتبر المرحلة خلصت؟

لما كل feature لها وصف واضح ومين يستخدمها وشروط نجاحها.

## أخطاء تتجنبها

- تكتب requirements عامة جدًا.
- تنسى حالات الفشل.
- تنسى صلاحيات كل مستخدم.
- تنسى توثيق QR expiration وsingle-use.

---

# Phase 4: System Design

## الهدف

تصمم النظام قبل كتابة الكود.

هنا بتجاوب على:

```text
مين بيكلم مين؟
الداتا شكلها إيه؟
الـ API هتكون إيه؟
الـ QR بيتولد إمتى؟
الدرج يفتح بناء على إيه؟
```

## 4.1 Architecture Design

التصميم العام:

```text
Mobile App
    |
    v
Backend API (Django + DRF)
    |
    v
PostgreSQL Database
    |
    v
Admin Dashboard

Locker Machine
    |
    v
Backend API
    |
    v
Open Drawer Command
```

## 4.2 Database Design

تعمل ERD فيه الجداول الأساسية:

```text
User
Product
Order
OrderItem
LockerStation
Drawer
QRToken
LockerEventLog
```

## 4.3 Order Status Flow

تحدد دورة حياة الطلب:

```text
Pending
Confirmed
Preparing
Assigned_To_Courier
In_Transit_To_Locker
Stored_In_Locker
Ready_For_Pickup
Picked_Up
Expired
Returned
Cancelled
```

## 4.4 API Design

تكتب endpoints قبل التنفيذ.

مثال:

```http
POST /api/token/
GET /api/products/
POST /api/orders/
GET /api/orders/my/
GET /api/courier/orders/
POST /api/locker/scan/
POST /api/admin/drawers/{id}/emergency-open/
```

## 4.5 Permission Matrix

تعمل جدول يوضح مين يقدر يعمل إيه.

مثال:

```text
Customer:
- View products
- Create order
- View own orders
- Generate pickup QR for own order

Courier:
- View assigned orders
- Deposit assigned orders

Admin:
- Manage everything

Locker Machine:
- Validate QR
- Report drawer status
```

## 4.6 QR Security Design

تحدد:

- هل QR عبارة عن random token أم JWT؟
- مدة الصلاحية.
- هل يستخدم مرة واحدة؟
- أين يخزن؟
- ماذا يحدث بعد استخدامه؟

القرار المفضل:

```text
QR contains secure random token, backend validates it, then decides drawer.
```

## 4.7 Hardware Protocol

تحدد شكل request من الماكينة للـ backend:

```http
POST /api/locker/scan/
```

```json
{
  "machine_id": "LOCKER-001",
  "qr_token": "abc123"
}
```

والرد:

```json
{
  "action": "open_drawer",
  "drawer_number": 3,
  "message": "Valid pickup token"
}
```

## المخرجات

- Architecture diagram.
- ERD.
- API list.
- Permission matrix.
- Order status diagram.
- QR security rules.

## إمتى تعتبر المرحلة خلصت؟

لما تقدر تبدأ coding وأنت عارف بالضبط كل model وendpoint وpermission.

## أخطاء تتجنبها

- تبدأ models بدون ERD.
- تعمل QR فيه drawer number واضح.
- تخلي الماكينة تقرر تفتح درج من نفسها.
- تنسى logs.

---

# Phase 5: Contract, Timeline, and Pricing

## الهدف

تتعامل كفريلانسر حقيقي.

حتى لو المشروع للتخرج، اتعلم تعمل حساب الوقت والفلوس والتسليم.

## تعمل إيه؟

تكتب proposal للعميل فيه:

- وصف المشروع.
- نطاق العمل.
- مدة التنفيذ.
- السعر.
- طريقة الدفع.
- عدد التعديلات.
- ما لا يشمله المشروع.
- فترة الدعم بعد التسليم.

## تقسيم milestones

اقتراح:

```text
Milestone 1: Documentation and Design
Milestone 2: Backend MVP
Milestone 3: Mobile App MVP
Milestone 4: Locker Simulation/Hardware Integration
Milestone 5: Testing, Deployment, and Handover
```

## تقسيم الدفع

مثال:

```text
30% قبل البداية
25% بعد backend MVP
20% بعد mobile MVP
15% بعد hardware integration
10% بعد التسليم النهائي
```

## إمتى تعتبر المرحلة خلصت؟

لما يكون العميل موافق كتابيًا على scope والمدة والدفع.

## أخطاء تتجنبها

- تبدأ بدون عربون.
- توافق على تعديلات مفتوحة.
- لا تحدد عدد revisions.
- لا تكتب خارج النطاق.

---

# Phase 6: Project Setup

## الهدف

تجهز بيئة العمل بشكل منظم.

## تعمل إيه؟

### GitHub

تعمل repo:

```text
smart-delivery-system
```

### Folder Structure

اقتراح:

```text
smart-delivery-system/
  backend/
  mobile/
  hardware/
  docs/
  diagrams/
  api-requests/
```

### Branches

```text
main
develop
feature/auth
feature/orders
feature/locker
feature/mobile-auth
```

### Backend Setup

```text
Django
Django REST Framework
Simple JWT
PostgreSQL
python-dotenv
pytest or Django TestCase
```

### Mobile Setup

```text
Flutter project
API service layer
Auth storage
QR scanner package
```

### Environment Files

تعمل:

```text
.env.example
```

ولا ترفع:

```text
.env
```

## المخرجات

- GitHub repo.
- Backend project initialized.
- Mobile project initialized.
- docs folder.
- README مبدئي.
- .gitignore.
- .env.example.

## إمتى تعتبر المرحلة خلصت؟

لما أي شخص يقدر يعمل clone ويشغل المشروع من التعليمات.

## أخطاء تتجنبها

- ترفع secrets على GitHub.
- تشتغل بدون Git.
- تكتب كل حاجة في branch واحدة بدون تنظيم.
- لا تعمل README.

---

# Phase 7: Backend Development

## الهدف

بناء قلب النظام.

ابدأ بالـ backend لأنه هو الذي يمسك:

- المستخدمين.
- الطلبات.
- الأدراج.
- QR.
- الصلاحيات.
- logs.

## ترتيب التنفيذ

### Step 1: Users and Auth

تعمل:

- JWT login.
- roles:

```text
customer
courier
admin
locker_device
```

- permissions مبدئية.

تختبر:

- login يرجع access و refresh.
- endpoint محمي يرجع 401 بدون token.

### Step 2: Products

تعمل:

- Product model.
- Product serializer.
- Product list endpoint.
- Admin create/update/delete.

تختبر:

- أي مستخدم يقدر يشوف المنتجات.
- admin فقط يقدر يضيف منتج.

### Step 3: Orders

تعمل:

- Order.
- OrderItem.
- create order.
- my orders endpoint.
- order details.

تختبر:

- customer يرى orders الخاصة به فقط.
- customer لا يرى orders مستخدم آخر.

### Step 4: Locker and Drawers

تعمل:

- LockerStation model.
- Drawer model.
- drawer status.
- drawer size.
- available drawer logic.

تختبر:

- النظام لا يختار drawer مشغول.
- النظام يختار drawer مناسب لحجم الطلب.

### Step 5: QR Tokens

تعمل:

- QRToken model.
- generate deposit token.
- generate pickup token.
- expiry.
- used_at.
- token type.

تختبر:

- token صالح يشتغل.
- token منتهي لا يشتغل.
- token مستخدم قبل كده لا يشتغل.

### Step 6: Courier APIs

تعمل:

- assigned orders endpoint.
- generate deposit QR.
- confirm deposit.

تختبر:

- courier يرى طلباته فقط.
- courier لا يودع order غير مخصص له.

### Step 7: Locker Machine APIs

تعمل:

```http
POST /api/locker/scan/
POST /api/locker/drawer-closed/
POST /api/locker/heartbeat/
```

تختبر:

- scan deposit QR يفتح درج للإيداع.
- scan pickup QR يفتح درج الاستلام.
- invalid QR يترفض.

### Step 8: Logs

تعمل:

- LockerEventLog.
- log لكل حدث مهم.

أحداث مهمة:

```text
deposit_qr_generated
pickup_qr_generated
qr_scanned
drawer_opened
drawer_closed
order_stored
order_picked_up
invalid_qr
expired_qr
emergency_open
```

### Step 9: Admin Dashboard

تستخدم Django Admin كبداية.

تضيف:

- Product admin.
- Order admin.
- Locker admin.
- Drawer admin.
- Event logs.

### Step 10: Backend Tests

لا تؤجل الاختبارات للنهاية.

اكتب tests لكل feature مهمة.

## المخرجات

- Backend API شغال.
- Postman أو `.http` requests.
- Tests.
- Admin dashboard.
- API docs مبدئية.

## إمتى تعتبر المرحلة خلصت؟

لما تقدر تعمل flow كامل من backend فقط:

```text
Create order -> assign courier -> deposit -> pickup
```

## أخطاء تتجنبها

- تكتب views بدون permissions.
- تخلي customer يقدر يشوف كل orders.
- تنسى QR single-use.
- تنسى event logs.
- تخلط business logic داخل views بشكل عشوائي.

---

# Phase 8: Mobile App Development

## الهدف

بناء التطبيق الذي يستخدمه العميل والمندوب.

ممكن تعمل تطبيق واحد فيه role-based UI.

يعني:

- لو customer يدخل، يرى شاشات العميل.
- لو courier يدخل، يرى شاشات المندوب.

## Customer Screens

### Login

- username/password.
- حفظ access token.
- refresh token flow لاحقًا.

### Products

- عرض المنتجات.
- تفاصيل المنتج.

### Create Order

- اختيار المنتج.
- اختيار locker.
- تأكيد الطلب.

### My Orders

- عرض orders الخاصة بالمستخدم.
- حالة كل order.

### Pickup QR

- يظهر فقط لو order status:

```text
Ready_For_Pickup
```

## Courier Screens

### Courier Orders

- الطلبات المخصصة للمندوب.

### Order Details

- معلومات الطلب.
- locker المطلوب.
- drawer إن كان محدد.

### Deposit QR

- QR خاص بالإيداع.
- أو زر يبدأ deposit flow.

### Confirm Deposit

- تأكيد أن الطلب تم وضعه في الدرج.

## Shared Features

- API client.
- token storage.
- loading states.
- error messages.
- logout.

## المخرجات

- APK أو running app.
- Screens للعميل.
- Screens للمندوب.
- اتصال حقيقي بالـ backend.

## إمتى تعتبر المرحلة خلصت؟

لما customer يقدر يعمل order من التطبيق، والمندوب يقدر يشوف الطلب ويتعامل معه.

## أخطاء تتجنبها

- تبدأ mobile قبل API ثابت.
- تخزن token بطريقة غير آمنة في production.
- لا تعرض errors واضحة.
- تخلي UI واحد لكل roles بدون تنظيم.

---

# Phase 9: Locker Hardware or Simulation

## الهدف

إثبات أن QR يؤدي إلى فتح درج.

## أفضل اختيار للتخرج

```text
Real mini prototype + simulation backup
```

## Prototype الحقيقي

مكونات:

- Raspberry Pi أو ESP32.
- QR scanner أو camera.
- Relay module.
- Solenoid lock.
- 3 أو 4 أدراج.
- اتصال إنترنت.

## Flow الهاردوير

```text
Scan QR
Send token to backend
Backend validates
Backend returns drawer number
Device opens relay
Drawer opens
Device sends event back
```

## Simulation Backup

تعمل صفحة أو dashboard بسيطة:

- تعرض الأدراج.
- عند scan أو إدخال token، الدرج يظهر opened.
- تستخدمها لو الهاردوير تعطل يوم العرض.

## المخرجات

- hardware script.
- API integration.
- drawer open demo.
- simulation backup.

## إمتى تعتبر المرحلة خلصت؟

لما QR صالح يفتح الدرج الصحيح، وQR غير صالح لا يفتح أي درج.

## أخطاء تتجنبها

- تخلي الدرج يفتح بدون backend validation.
- تعتمد على الهاردوير فقط بدون simulation backup.
- لا تسجل event عند فتح الدرج.

---

# Phase 10: Integration

## الهدف

ربط كل الأجزاء مع بعض.

هنا المشروع يتحول من أجزاء منفصلة إلى نظام واحد.

## تعمل إيه؟

تجرب السيناريو الكامل:

```text
Customer login
View products
Create order
Admin assigns courier
Courier deposits order
Locker opens drawer
Customer receives QR
Customer scans QR
Locker opens drawer
Order becomes Picked_Up
Admin sees logs
```

## Checklist

- mobile يتصل بالـ backend.
- backend يتصل بالـ database.
- locker يتصل بالـ backend.
- كل status بيتغير صح.
- logs بتتسجل.
- errors واضحة.

## المخرجات

- integrated demo.
- bug list.
- fixed critical bugs.

## إمتى تعتبر المرحلة خلصت؟

لما تعمل demo كامل 3 مرات متتالية بدون كسر.

## أخطاء تتجنبها

- تختبر كل جزء منفصل فقط.
- تكتشف مشاكل integration قبل التسليم بيوم.
- تنسى حالات الفشل.

---

# Phase 11: Testing

## الهدف

تتأكد إن النظام آمن ومستقر.

## أنواع الاختبارات

### Backend Tests

- auth tests.
- permission tests.
- order tests.
- QR tests.
- locker scan tests.

### Mobile Tests

- login works.
- token saved.
- order created.
- QR displayed.
- errors displayed.

### Hardware Tests

- valid QR opens drawer.
- invalid QR does not open drawer.
- drawer closed event works.

### Security Tests

اختبر:

- customer لا يرى orders غيره.
- courier لا يرى orders غيره.
- QR لا يستخدم مرتين.
- expired QR لا يعمل.
- admin فقط يعمل emergency unlock.

## أهم test cases لمشروعك

```text
TC-001: Unauthenticated user cannot access my orders.
TC-002: Customer can view own orders only.
TC-003: Courier can view assigned orders only.
TC-004: Pickup QR opens correct drawer.
TC-005: Used QR cannot be reused.
TC-006: Expired QR is rejected.
TC-007: Full locker cannot be selected.
TC-008: Admin emergency unlock creates event log.
```

## المخرجات

- test report.
- passing tests.
- bugs fixed.

## إمتى تعتبر المرحلة خلصت؟

لما critical flows شغالة وكل tests الأساسية تعدي.

## أخطاء تتجنبها

- تختبر happy path فقط.
- لا تختبر permissions.
- لا تختبر QR reuse.
- تعتبر أن "اشتغل مرة" يعني جاهز.

---

# Phase 12: User Acceptance Testing

## الهدف

تخلي العميل أو الدكتور أو شخص غيرك يجرب المشروع كأنه مستخدم حقيقي.

اسم المرحلة:

```text
UAT - User Acceptance Testing
```

## تعمل إيه؟

تجهز سيناريوهات:

### Scenario 1: Customer Order

- login.
- browse products.
- create order.
- choose locker.

### Scenario 2: Courier Deposit

- courier login.
- view assigned order.
- scan/deposit.
- drawer opens.

### Scenario 3: Customer Pickup

- customer sees QR.
- scan QR.
- drawer opens.
- order status changes.

### Scenario 4: Admin Review

- admin sees orders.
- admin sees logs.
- admin sees drawer status.

## المخرجات

- feedback list.
- accepted features.
- requested changes.

## إمتى تعتبر المرحلة خلصت؟

لما العميل يوافق أن الـ MVP يعمل المطلوب.

## أخطاء تتجنبها

- تترك العميل يجرب بدون سيناريو.
- توافق على تغييرات كبيرة كأنها bugs.
- لا تفرق بين bug وnew feature.

## الفرق بين Bug وChange Request

Bug:

```text
شيء متفق عليه لا يعمل.
```

Change Request:

```text
شيء جديد لم يكن داخل الاتفاق.
```

مثال:

لو pickup QR لا يفتح الدرج، ده bug.

لو العميل طلب إضافة payment gateway بعد الاتفاق، ده change request.

---

# Phase 13: Deployment

## الهدف

تشغيل المشروع في بيئة يمكن للعميل أو اللجنة تجربتها.

## Backend Deployment

اختيارات:

```text
Render
Railway
VPS
DigitalOcean
```

## Production Requirements

- PostgreSQL.
- environment variables.
- HTTPS.
- DEBUG=False.
- secure secret key.
- allowed hosts.
- static files.
- database backup.

## Mobile Delivery

- APK.
- أو تشغيل على جهاز demo.

## Hardware Deployment

- device متصل بنفس backend.
- machine_id واضح.
- device token أو API key.

## المخرجات

- live backend URL.
- APK أو mobile demo.
- hardware connected.
- deployment guide.

## إمتى تعتبر المرحلة خلصت؟

لما المشروع يعمل خارج جهازك المحلي.

## أخطاء تتجنبها

- تسلم مشروع يعمل على جهازك فقط.
- تترك DEBUG=True.
- لا تستخدم HTTPS.
- تضع secrets في الكود.

---

# Phase 14: Handover

## الهدف

تسليم المشروع بشكل احترافي.

## تسلم إيه؟

### Code

- GitHub repo.
- Backend code.
- Mobile code.
- Hardware code.

### Documentation

- README.
- Setup guide.
- API documentation.
- Database schema.
- User manual.
- Admin manual.

### Credentials

Demo accounts:

```text
admin
customer
courier
locker_device
```

### Demo Material

- demo video.
- screenshots.
- presentation.
- test report.

## Handover Checklist

```text
[ ] Source code delivered
[ ] README completed
[ ] .env.example included
[ ] API docs included
[ ] Database schema included
[ ] Admin account provided
[ ] Demo accounts provided
[ ] APK provided
[ ] Hardware instructions included
[ ] Known limitations documented
[ ] Future work documented
```

## إمتى تعتبر المرحلة خلصت؟

لما شخص آخر يقدر يشغل المشروع ويفهمه من غير ما يسألك في كل خطوة.

## أخطاء تتجنبها

- تسلم كود فقط.
- لا تكتب setup instructions.
- لا تذكر limitations.
- لا تعمل demo video.

---

# Phase 15: Maintenance and Future Work

## الهدف

تحدد ماذا يحدث بعد التسليم.

## Maintenance

بعد التسليم، ممكن يكون فيه:

- bug fixes.
- small improvements.
- server monitoring.
- backups.
- support.

## Future Work

Features لاحقة:

- online payment.
- AI locker recommendation.
- camera proof.
- external shipping company integration.
- offline mode.
- advanced analytics.
- SMS notifications.
- multi-vendor support.

## كفريلانسر

لازم تحدد:

```text
هل الدعم مجاني لمدة معينة؟
هل أي feature جديدة بسعر جديد؟
هل الصيانة شهرية؟
```

اقتراح:

```text
7 أيام bug fixing بعد التسليم
أي feature جديدة تعتبر change request
الصيانة الشهرية باتفاق منفصل
```

---

# Timeline مقترح للمشروع

لو شغال لوحدك ومبتدئ، خليك واقعي.

## نسخة تخرج قوية

```text
Week 1: Discovery + Scope + SRS
Week 2: System Design + ERD + API Plan
Week 3: Backend Auth + Products + Orders
Week 4: Lockers + Drawers + QR Tokens
Week 5: Courier APIs + Locker APIs + Admin
Week 6: Mobile App Customer Screens
Week 7: Mobile App Courier Screens + Integration
Week 8: Hardware Prototype or Simulation
Week 9: Testing + Bug Fixing
Week 10: Deployment + Documentation + Presentation
```

لو الوقت أقل، قلل features ولا تقلل quality.

---

# أول أسبوع تعمل فيه إيه؟

## Day 1

- اكتب Project Brief.
- حدد المشكلة والحل.
- حدد المستخدمين.

## Day 2

- حدد MVP.
- اكتب داخل النطاق وخارج النطاق.

## Day 3

- اكتب user stories.
- اكتب functional requirements.

## Day 4

- ارسم ERD مبدئي.
- حدد models.

## Day 5

- اكتب API endpoints.
- اكتب permission matrix.

## Day 6

- جهز GitHub repo.
- جهز Django project.

## Day 7

- ابدأ Auth + JWT.
- اكتب أول test.

---

# طريقة إدارة الشغل يوميًا

كل يوم قبل ما تبدأ:

```text
What will I build today?
What files/features will change?
How will I test it?
```

كل يوم بعد ما تخلص:

```text
What did I finish?
What is broken?
What is next?
```

استخدم board بسيط:

```text
Todo
In Progress
Testing
Done
```

مثال tasks:

```text
Todo:
- Create Order model
- Create Drawer model
- Add JWT login

In Progress:
- Product API

Testing:
- User orders endpoint

Done:
- Django project setup
```

---

# قواعد مهمة تمشي عليها

- لا تبدأ بالهاردوير قبل تصميم الـ backend flow.
- لا تعمل QR بسيط فيه order_id وdrawer_id.
- لا تترك endpoint بدون permission.
- لا تجعل العميل يرى بيانات غيره.
- لا تجعل الماكينة تفتح درج بدون الرجوع للـ backend.
- لا تؤجل tests للنهاية.
- لا تضيف AI قبل ما الـ MVP يشتغل.
- لا تكبر المشروع أكثر من اللازم.
- كل feature لازم يكون لها test أو demo واضح.

---

# تعريف النسخة الناجحة

المشروع ناجح إذا قدرت تعمل demo كامل:

```text
1. Customer logs in.
2. Customer creates order.
3. Admin or system assigns courier.
4. Courier deposits order in locker.
5. Drawer opens correctly.
6. Customer gets pickup QR.
7. Customer scans QR.
8. Correct drawer opens.
9. Order becomes Picked_Up.
10. Admin sees event logs.
11. Tests pass.
```

لو وصلت لهذا، أنت لا تملك مشروع تخرج فقط. أنت تملك case study قوي لأول شغل فريلانس.

