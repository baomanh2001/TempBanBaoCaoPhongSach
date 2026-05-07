# 📋 BẢN TÓM TẮT SO SÁNH 2 THIẾT KẾ R&D CLEANROOM FAB

---

## 🎯 KẾT LUẬN NHANH

| | **Design A (V3.2)** | **Design B (Linear)** |
|---|---|---|
| **Bản chất** | Fab Architecture chuyên nghiệp | Equipment Arrangement đơn giản |
| **Cấp độ** | Pilot fab / Advanced R&D | Teaching cleanroom / University lab |
| **Trạng thái** | Cần fix một số lỗi P0 | Cần redesign nhiều phần cốt lõi |
| **Phù hợp** | R&D fab nghiêm túc, sản xuất wafer | Lab học thuật, đào tạo, prototype |

> **Design A vượt trội về kỹ thuật cleanroom. Design B chỉ thắng về maintainability (utility tách ngoài) và scalability (modular).**

---

## ✅ TẠI SAO DESIGN A ỔN

| Tiêu chí | Lý do |
|---|---|
| **Contamination Control** | Có Contamination Barrier Wall, đầy đủ Airlock + Pass-box + Service Chase + ATP loop riêng + Chemical Operator Route riêng |
| **Personnel Flow** | One-way nghiêm ngặt (Entry → Pre-gown → Gowning → Airshower → CR → De-gowning → Exit), entry/exit tách biệt vật lý |
| **Pressure Cascade** | Định nghĩa chi tiết từng phòng (+20/+15/+10/+5/-5/-10/-15/-50 Pa), đúng nguyên tắc "sạch hơn = áp cao hơn" |
| **Material Flow** | Có Pass-box, Material Airlock, vật liệu đi đường riêng không trộn với người |
| **Chemical Safety** | Tách acid/solvent waste pipe, 3 stack riêng, có neutralization + carbon trap, Chemical Bunker ngoài trời |
| **Documentation** | Đủ thông số kỹ thuật (áp suất, ACH, FFU, ΔP), legend đầy đủ, đủ làm Schematic Design |

---

## ❌ TẠI SAO DESIGN B BẤT ỔN

| Tiêu chí | Lý do |
|---|---|
| **Contamination Control** | Tool đặt sát corridor, ISO 5 nằm giữa ISO 7 không có airlock, Litho ISO 6 sát Wet Bench ISO 7 → AMC risk cực cao |
| **Personnel Flow** | **Bi-directional flow** – mũi tên vào/ra qua cùng 1 cửa, **THIẾU Airshower**, **THIẾU De-gowning** → Gowning Room mất chức năng vùng đệm sạch |
| **Pressure Cascade** | **Hoàn toàn không thể hiện áp suất**, layout vật lý tự phá vỡ áp suất khi mở cửa |
| **Material Flow** | Material đi chung personnel aisle, không có pass-box, không có Material Airlock |
| **Chemical Safety** | Chỉ 1 "Chemical Store" gộp chung, không có waste segregation, không có Chemical Bunker, không có neutralization, Chemical Store nằm TRONG cleanroom sát ATP |
| **Maintenance** | Không có Service Chase đúng nghĩa → maintenance phải vào CR để sửa máy |
| **Documentation** | Chỉ có flow nhân sự, thiếu mọi thông số kỹ thuật, mới ở mức Concept Sketch |

---

## ⚖️ ĐIỂM CỘNG CỦA DESIGN B (Cần ghi nhận)

- ✅ **≥6 emergency exit** phân bổ đều (tuân thủ NFPA tốt hơn Design A)
- ✅ **Tách utility ra ngoài CR rõ ràng** (2 AHU, Vacuum, Scrubber, Gas, RO, CDA)
- ✅ **Phòng Gas H₂ ngoài CR** (an toàn cho khí dễ cháy)
- ✅ **Layout modular tuyến tính** dễ scale
- ✅ Có Control Room, CDA, RO – thực tế cho vận hành cơ bản

---

## 🔴 LỖI CẦN FIX

### Design A (lỗi P0):
- Chỉ 1 emergency exit (vi phạm NFPA)
- De-gown < ATP Reception → ngược dòng khí
- Airshower > Gowning → reverse flow
- Acid + Solvent bench cùng phòng
- Thiếu AMC filter cho Litho

### Design B (lỗi P0 – cần redesign):
- Thiếu Airshower
- Thiếu De-gowning room
- Bi-directional flow
- Không có Pressure Cascade
- Không có Pass-box / Material Airlock
- Không có Service Chase
- Không có waste segregation
- Không có Chemical Bunker

---

## 🚀 KHUYẾN NGHỊ

| Ngắn hạn | Dùng **Design A** làm cơ sở, fix Top P0 trước thi công |
| --- | --- |
| **Trung hạn** | Áp dụng **Hybrid Design V4.0** = Design A (cleanroom engineering) + Design B (utility tách ngoài + modular + multi-exit) |
| **Dài hạn** | Nâng cấp lên Industrial Fab với subfab, AMHS, AMC control, redundancy |

---

## 💡 MỘT CÂU KẾT LUẬN

> **Design A** giải quyết bài toán *"Zero Cross-Contamination"* bằng **layout one-way + pressure cascade + chemical engineering chuẩn fab**.
> **Design B** chỉ là *"bố trí thiết bị"* – tối ưu vận hành nhưng **hy sinh các tiêu chuẩn kiểm soát nhiễm chéo cơ bản** của cleanroom semiconductor.

# 📑 BẢN ĐÁNH GIÁ SO SÁNH HAI THIẾT KẾ R&D CLEANROOM FAB

**Tài liệu:** Comparative Design Assessment Report
**Phiên bản:** 2.0
**Đối tượng đánh giá:**
- **Design A:** R&D Cleanroom Fab – Master Floor Plan V3.2 (~550 m²) – "Zero Cross-Contamination Design"
- **Design B:** Personnel Flow Layout Drawing (~400–500 m²) – Linear Bay Layout

**Tiêu chuẩn tham chiếu:** ISO 14644-1/4, SEMI S2/S8, NFPA 101, ANSI Z358.1, QCVN 06:2022/BXD

---

## 1. EXECUTIVE SUMMARY

| Hạng mục | **Design A (V3.2)** | **Design B (Linear)** |
|---|---|---|
| **Triết lý thiết kế** | Engineering-driven Fab Architecture | Operations-driven Equipment Arrangement |
| **Cấp độ tương đương** | Pilot fab / Advanced R&D / MEMS line | Teaching cleanroom / University lab nhỏ |
| **Mức độ sẵn sàng vận hành** | Cần fix một số lỗi P0 trước thi công | Cần redesign nhiều phần cốt lõi |
| **Khuyến nghị sử dụng** | R&D fab nghiêm túc, sản xuất wafer | Lab học thuật / pilot nhỏ / đào tạo |

> **Kết luận chính:** Design A có nền tảng cleanroom engineering vững chắc, phù hợp cho fab vận hành thật. Design B mới ở mức "bố trí thiết bị", thiếu các thành phần cốt lõi của một cleanroom semiconductor đúng nghĩa.

---

## 2. PHÂN TÍCH CHI TIẾT THEO TIÊU CHÍ

---

### 2.1 CONTAMINATION CONTROL

#### ✅ **Design A – ỔN vì:**
- Có **Contamination Barrier Wall** vật lý chia tách rõ vùng sạch/bẩn
- Có **đầy đủ Airlock + Pass-box + Service Chase + ATP loop riêng + Chemical Operator Route riêng**
- Phân vùng ISO rõ ràng theo cấp độ: ISO 5/6 Litho – ISO 7 Process – ISO 8 Gowning – ISO 9 Pre-gown – Non-clean
- Lithography (vùng nhạy nhất) được **cô lập riêng biệt** trong bay độc lập – đúng tư duy fab thật
- ATP zone (sinh bụi từ dicing/wire bond) được **tách hoàn toàn** khỏi front-end
- Mọi đường đi của hóa chất, người, vật liệu đều được phân tách logic

#### ❌ **Design B – BẤT ỔN vì:**
- **Tool đặt sát corridor** (Hood lithography, Microscope, Metrology) → particle migration trực tiếp khi operator đi qua
- **ISO 5 (Hood) nằm xen giữa ISO 7** mà không có airlock thực sự, không có pressure staging → khí ISO 7 dễ tràn vào ISO 5
- **Litho ISO 6 chỉ cách Wet Bench ISO 7 qua 1 vách** → hơi acid/solvent thấm vào Litho gây resist poisoning, AMC contamination
- **Không có Contamination Barrier Wall** – mọi phòng đều "thông" qua corridor chung
- **Không có Pass-box** – vật liệu phải đi cùng đường với người
- Maintenance phải **đi vào trong cleanroom** để sửa máy (vs 70-90% nên làm từ subfab trong fab thật)

---

### 2.2 PERSONNEL FLOW

#### ✅ **Design A – ỔN vì:**
- Tuân thủ nghiêm ngặt nguyên tắc **một chiều (Unidirectional)**: Entry → Pre-gown → Gowning → Airshower → Main CR → De-gowning → Exit Corridor riêng
- **Lối vào và lối ra hoàn toàn tách biệt vật lý** – ngăn nhân viên về (mang bụi) gặp người vào ca
- Có **Hành lang Exit Corridor cách ly** với khu sạch, đảm bảo bụi từ de-gowning không quay ngược
- **Chemical operator có route riêng** từ bunker hóa chất – không chia sẻ đường với personnel chính
- **ATP có gowning + reception riêng** → tránh ATP contamination backflow
- Có đầy đủ 3 bậc gowning: Pre-gown (ISO 9) → Gowning (ISO 8) → Airshower → CR

#### ❌ **Design B – BẤT ỔN vì:**
- **Bi-directional flow nghiêm trọng**: mũi tên xanh (vào) và đỏ (ra) đan xen liên tục qua **cùng một cửa** ở mỗi phòng
- Tại Gowning Room: nhân viên vừa đi làm về (mang bụi dính áo) đi cùng không gian với người chuẩn bị vào ca → **phòng Gowning mất chức năng "vùng đệm sạch"**
- **THIẾU AIRSHOWER hoàn toàn** – đây là lỗi cơ bản nghiêm trọng; bụi/sợi vải từ áo gowning đi thẳng vào CR
- **THIẾU De-gowning room riêng** – không có cơ chế xả đồ bẩn trước khi ra
- Người gowning đi ngang Lithography, người maintenance đi ngang Wet Bench → **traffic chính cắt ngang critical tools**
- Entry/exit gần nhau ở mỗi phòng → tạo **turbulence + particle carry-back** khi mở cửa đồng thời
- Emergency exit cắt ngang process zone → khi panic event sẽ phá vỡ contamination logic

---

### 2.3 PRESSURE CASCADE

#### ✅ **Design A – ỔN vì:**
- **Định nghĩa chi tiết áp suất từng phòng**: ISO 5/6 Litho **+20 Pa**, Main Bay **+15 Pa**, Gowning **+10 Pa**, De-gown **+5 Pa**, Office **0 Pa**, Service Chase **−5 Pa**, Waste **−10 Pa**, Bunker **−15 Pa**, Hood **−50 Pa**
- Logic đúng nguyên tắc **"sạch hơn = áp cao hơn"** và **"nguy hiểm = áp âm"**
- Khu vực Litho (nhạy nhất) có áp **dương cao nhất** → đẩy khí từ trong ra, ngăn khí bẩn xâm nhập
- Khu vực hóa chất, waste, chase đều giữ **áp âm** → bẫy hơi độc, không cho rò ra phòng làm việc
- Có **vestibule / airlock** giữa các vùng chênh áp lớn (tuy chưa hoàn hảo)
- Có ý thức về Sink/Bubble concept ở Pass-box, Material Airlock

#### ❌ **Design B – BẤT ỔN vì:**
- **HOÀN TOÀN KHÔNG THỂ HIỆN áp suất** của bất kỳ phòng nào trên bản vẽ
- Không có pressure differential, không có pressure lock, không có pressure source/sink → **không thể đánh giá kiểm soát áp**
- **Layout vật lý tự phá vỡ pressure cascade**: cửa 2 chiều liên tục giữa các phòng khác cấp ISO mà không qua buffer/airlock
- Mỗi lần mở cửa giữa ISO 7 (corridor) ↔ ISO 5 (Hood area) sẽ gây **sụt áp tức thì** → hạt vi hạt trào ngược vào vùng lõi
- Wet bench áp âm (giả định) nằm gần corridor → khi exhaust imbalance, hơi solvent dễ drift ra
- Litho không được overpressure đủ mạnh để chống AMC từ Wet Bench liền kề
- Không có Service Chase áp âm → hơi hóa chất khuếch tán tự do qua trần/sàn

---

### 2.4 MATERIAL / WAFER FLOW

#### ✅ **Design A – ỔN vì:**
- Có **Material Airlock DA→DB** chuyên dụng cho vật tư đầu vào
- Có **Resist Pass-box, Wafer Out Pass-box** với interlock một chiều
- Wafer flow được định hướng rõ **LEFT → RIGHT** trong Process Tool Zone
- Hóa chất, vật liệu, rác thải có **đường đi riêng**, không chia sẻ corridor nhân sự
- Áp dụng đúng tư duy chuẩn fab: **"vật liệu không đi cùng người"**
- Có Chemical Pass-box riêng giữa Bunker và Acid Bench

#### ❌ **Design B – BẤT ỔN vì:**
- **Material flow đi chung personnel aisle hoàn toàn** – đây là lỗi phổ biến của academic cleanroom
- **Không có pass-box** ở bất kỳ vị trí nào → vật tư phải qua cùng cửa với người
- **Không có Material Airlock** → hóa chất từ Chemical Store đi thẳng vào CR không qua wipe-down
- Hóa chất, FOUP/wafer, rác thải, finished goods đều **cắt ngang luồng nhân sự** trong hành lang chính
- Không có Wafer Out path riêng → thành phẩm và bán thành phẩm dùng chung cửa
- Risk **bump contamination** + **chemical spill trong corridor người** rất cao

---

### 2.5 CHEMICAL SEGREGATION & WASTE HANDLING

#### ✅ **Design A – ỔN vì:**
- **Tách hoàn toàn đường ống acid waste và solvent waste** xuống tận trench → loại bỏ nguy cơ phản ứng trong ống
- **KHÔNG dùng common acid/solvent header** – đây là yêu cầu tối quan trọng trong fab thật
- **3 stack exhaust riêng biệt**: Stack 1 (Acid) – Stack 2 (VOC) – Stack 3 (General) → tránh re-entrainment hỗn hợp
- Có **acid neutralization tank + VOC carbon trap** trước khi xả stack
- **Chemical Bunker đặt ngoài trời + double-wall drain** + gas detection → cách ly nguy hiểm tối đa
- Có **Waste Management Room riêng** với áp âm (−10 Pa)
- Có Spill containment trays + chemical drain tại từng hood

#### ❌ **Design B – BẤT ỔN vì:**
- **Chỉ có 1 "Chemical Store" duy nhất** gộp chung mọi loại hóa chất (acid + solvent + base?) → nguy cơ phản ứng chéo
- **Không có acid/solvent waste segregation** – không thể hiện đường ống xả riêng
- **Không có acid neutralization, không có VOC carbon trap** → xả thẳng ra môi trường
- **Không có Chemical Bunker ngoài trời** – mọi hóa chất đều trữ trong cleanroom
- **Chemical Store nằm TRONG cleanroom + sát ATP Assembly** → nếu rò rỉ, hơi hóa chất tràn vào vùng assembly (epoxy, wire bond cần khô)
- Không có spill containment, không có double-wall drain
- Nguy cơ **acid/VOC mixing trong exhaust** + **unsafe exhaust interaction** rất cao

---

### 2.6 MAINTAINABILITY

#### ⚠️ **Design A – Có service chase nhưng còn hạn chế:**
- Có **Service Chase Loop** áp âm chạy toàn bộ phía sau – tốt cho cô lập maintenance
- Có Stack zoning rõ ràng – kỹ thuật viên biết utility chạy ở đâu
- **Tuy nhiên:** chỉ có single-side chase (fab lớn cần dual-side hoặc interstitial floor)
- Tool maintenance pull-space chưa thể hiện rõ
- Chase chứa **hỗn hợp acid + VOC + utility** → tech bảo trì có nguy cơ phơi nhiễm cao

#### ✅ **Design B – Tốt về tách utility nhưng yếu về subfab:**
- **Tách utility ra ngoài cleanroom rất rõ ràng**: 2 phòng AHU riêng biệt 2 đầu, Vacuum pump room, Scrubber room, phòng Gas (N₂+O₂+H₂+Mix), CDA, RO – đây là điểm cộng lớn
- Phòng Gas chứa H₂ (dễ cháy nổ) đặt **ngoài cleanroom** → an toàn theo SEMI S6
- AHU 2 đầu tạo **cấp khí cân bằng** từ 2 phía
- **Tuy nhiên:** **Không có Service Chase đúng nghĩa** – đây là lỗi cốt lõi
- Maintenance phải **đi vào CR để sửa máy** → mỗi lần bảo trì = nguồn contamination lớn
- Furnace + Deposition nằm giữa bay → khi thay equipment có thể phải **shutdown cả line**
- HEPA replacement không có access từ trên/sau → phải tháo từ trong CR

---

### 2.7 FAB REALISM (Tính thực tế khi vận hành)

#### ✅ **Design A – ỔN vì:**
Mang đầy đủ đặc điểm của fab thật:
- **Bay/chase architecture** (mô hình bay chuẩn semiconductor)
- Pressure zoning chi tiết
- Chemical segregation (acid/solvent split)
- Waste engineering (3 stack, neutralization, carbon trap)
- ATP segregation hoàn chỉnh
- Dedicated personnel/material/chemical flow
- Có đầy đủ Office, Meeting Room, Storage – hỗ trợ vận hành đa ca

→ Tương đương **Pilot fab / University semiconductor center / MEMS line / Advanced R&D fab**

#### ❌ **Design B – BẤT ỔN vì:**
- Mang đặc điểm của **research lab / university facility nhỏ / retrofit building** hơn là fab
- Có Control Room + CDA + RO – tốt cho vận hành cơ bản, **nhưng** thiếu các thành phần cốt lõi của fab semiconductor:
  - Không có chase, không có pass-box, không có barrier wall, không có cascade
- ATP Assembly đặt sát Chemical Store là **bố trí phi thực tế** trong fab thật (Assembly cần sạch, Chemical sinh hơi)
- Không phù hợp scale-up từ R&D lên pilot production

---

### 2.8 SCALABILITY (Khả năng mở rộng)

#### ⚠️ **Design A – Khó scale vì:**
- Layout phức tạp đa vùng → mở rộng phải **re-design toàn bộ pressure cascade và HVAC**
- Không có cấu trúc modular – mỗi zone phụ thuộc lẫn nhau qua Lane C
- Bottleneck cố định tại Airshower (4 m²) và De-gowning – không tăng được người vận hành
- Thêm tool mới phải xen vào Process Tool Zone → ảnh hưởng wafer flow LEFT→RIGHT

#### ✅ **Design B – Scale tốt vì:**
- **Layout tuyến tính 2 hàng song song** → dễ kéo dài thêm bay mới ở 2 đầu
- **Modular hóa cao**: mỗi phòng tương đối độc lập, có lối vào riêng → dễ thêm/bớt
- Future tool addition không phá vỡ flow tổng thể
- Capacity ramp-up không bị bottleneck cứng tại 1 điểm
- Phù hợp chiến lược R&D → pilot → scale-up từng giai đoạn

---

### 2.9 EHS (Environment, Health, Safety)

#### ✅ **Design A – Mạnh về chemical safety:**
- Có **Chemical Bunker** ngoài trời với gas detection, double-wall drain, spill containment
- **Segregated waste** (acid/solvent tách hoàn toàn)
- Có **Eyewash + Safety Shower** (dù chưa đủ coverage)
- Có **Emergency Path** (dù chỉ 1 lối)
- **Acid/VOC mixing risk được loại bỏ** nhờ tách stack và tách waste
- Có ý thức về spill containment, neutralization

**Tuy nhiên còn yếu:**
- Chỉ **1 emergency exit cho 550 m²** – vi phạm NFPA 101 / QCVN 06:2022 (cần ≥2 exit)
- Safety shower coverage không đạt ANSI Z358.1 (>15m từ acid hood)
- Gas detection chỉ có ở bunker, **thiếu tại điểm sử dụng** (Litho, Furnace)

#### ⚠️ **Design B – Tốt về egress, yếu về chemical EHS:**

**Điểm mạnh:**
- **≥6 emergency exit phân bổ đều** – tuân thủ NFPA tốt
- Phòng Gas (H₂ mix) đặt ngoài CR → an toàn cho khí dễ cháy
- AHU/Scrubber/Vacuum tách ngoài → dễ ứng cứu khi sự cố

**Điểm yếu nghiêm trọng:**
- **Không có Chemical Bunker** → toàn bộ hóa chất trữ trong CR
- **Không có acid segregation** → nguy cơ phản ứng chéo
- **Không có waste neutralization** → xả thẳng ra môi trường
- **Không có hazmat zoning** → không phân loại theo nguy hiểm
- **Không có toxic exhaust zoning** → acid và VOC có thể trộn trong exhaust chung
- **Không thể hiện safety shower, eyewash, gas detection** ở bất kỳ vị trí nào
- Chemical Store sát ATP → nếu rò → assembly nhiễm hơi acid

---

### 2.10 UTILITY ROUTING

#### ✅ **Design A – ỔN vì:**
- Có **Service Chase Loop closed** chạy toàn bộ phía Bắc → tập trung toàn bộ utility
- **3 Stack zoning rõ** (Acid – VOC – General) trên mái → tránh re-entrainment
- Routing logic theo nguyên tắc "dirty out → clean in" rõ ràng
- Có acid waste pipe + solvent waste pipe + chemical pass riêng

**Còn hạn chế:** Chase chứa hỗn hợp acid + VOC + utility chung – nên tách thành 3 chase riêng

#### ⚠️ **Design B – Tách ngoài tốt nhưng routing trong CR không rõ:**
- **Tách utility ra ngoài CR rất rõ**: AHU × 2, Vacuum, Scrubber, Gas, RO, CDA → đây là điểm cộng
- Bố trí AHU 2 đầu → cấp khí cân bằng tốt
- **Tuy nhiên:** routing utility từ ngoài vào tool trong CR **không thể hiện**
- Không có chase → utility chạy qua trần/sàn cleanroom → khó bảo trì, nguy cơ rò rỉ trong vùng sạch
- Không thấy đường acid waste, solvent waste

---

### 2.11 WASTE HANDLING

#### ✅ **Design A – ỔN vì:**
- Có **Waste Management Room riêng** ở góc Đông, áp âm −10 Pa
- **Tách trench thu acid/solvent hoàn toàn**
- Có acid neutralization tank + VOC carbon trap trước khi xả
- **Truck dock riêng** cho waste output → không lẫn với finished goods
- Có **berm 20cm** quanh khu waste để chống tràn
- Có acid/solvent waste inlet riêng với eyewash + shower

**Còn hạn chế:** Waste Room hơi sát Finished Goods – nên đẩy xa hơn

#### ❌ **Design B – BẤT ỔN vì:**
- **Không có Waste Management Room** thể hiện trên bản vẽ
- **Không có waste segregation** – chỉ có 1 Scrubber room chung
- Không có neutralization tank, không có carbon trap
- Không có truck dock cho chemical waste
- Không thấy đường thu chất thải lỏng (acid drain, solvent drain)
- Chemical waste có thể phải **mang ngược qua corridor** ra ngoài → contamination + safety risk

---

### 2.12 DOCUMENTATION QUALITY

#### ✅ **Design A – ỔN vì:**
- Bản vẽ thể hiện **đầy đủ thông số kỹ thuật**: áp suất từng phòng, ACH, ΔP, FFU coverage, ULPA class, temp/RH, particle counter
- **Legend đầy đủ**: màu zoning, mũi tên flow (personnel/material/chemical/waste/acid/solvent), ký hiệu (interlock door, emergency exit, hazard zone, critical feature)
- Có **dimension tổng thể và từng phòng**, có kích thước cụ thể (m², m)
- Có ghi chú kỹ thuật (chemical flow direction, waste routing, separate piping)
- **Đủ chi tiết để làm Schematic Design / Basic Design phase**
- Có scale 1:100, hướng Bắc rõ ràng

#### ❌ **Design B – BẤT ỔN vì:**
- Bản vẽ **chỉ thể hiện flow nhân sự** (mũi tên xanh/đỏ) – mọi thông số kỹ thuật khác đều thiếu
- **Không có áp suất, không có ACH, không có FFU spec, không có ΔP**
- Legend chỉ có "Personnel Entrance / Personnel Exit" – không có symbol cho material, chemical, waste, hazard
- **Chỉ có 1 dimension** là cao độ +19,800 mm (cốt sàn) – không có kích thước phòng
- Mới ở mức **Concept Design / Layout Sketch** – chưa đủ làm cơ sở thi công
- Thiếu thông tin về vật liệu sàn/vách/trần, không có chú thích kỹ thuật

---

## 3. TỔNG HỢP LỖI / RỦI RO CHÍNH

### 3.1 Lỗi của Design A – Cần fix nhưng nền tảng vẫn vững

| Mức độ | Lỗi |
|---|---|
| 🔴 P0 | Chỉ 1 emergency exit (vi phạm NFPA / QCVN 06:2022) |
| 🔴 P0 | De-gowning (+5 Pa) < ATP Reception (+8 Pa) → ngược dòng khí |
| 🔴 P0 | Airshower (+12 Pa) > Gowning (+10 Pa) → reverse flow |
| 🔴 P0 | Acid + Solvent bench cùng phòng → nguy cơ cháy/phản ứng |
| 🔴 P0 | Thiếu AMC chemical filter cho Litho |
| 🟠 P1 | Lane C "shared spine" – trộn người + wafer + tool access |
| 🟠 P1 | Furnace gần Metrology → vibration + thermal drift |
| 🟠 P1 | Service chase single-side, áp âm chưa đủ |
| 🟡 P2 | Resist pass-box dùng chung hóa chất + wafer (AMC risk) |
| 🟡 P2 | Khó scale, không modular |

### 3.2 Lỗi của Design B – Lỗi cốt lõi, cần redesign

| Mức độ | Lỗi |
|---|---|
| 🔴 P0 | **Thiếu Airshower** – lỗi cơ bản nhất của một cleanroom |
| 🔴 P0 | **Thiếu De-gowning room** riêng |
| 🔴 P0 | **Bi-directional personnel flow** – mất chức năng vùng đệm sạch |
| 🔴 P0 | **Không có Pressure Cascade** – không thể đánh giá kiểm soát áp |
| 🔴 P0 | **Không có Pass-box, Material Airlock** |
| 🔴 P0 | **Không có Contamination Barrier Wall** |
| 🔴 P0 | **Không có Service Chase** – maintenance phải vào CR |
| 🔴 P0 | **Không có Acid/Solvent waste segregation** |
| 🔴 P0 | **Không có Chemical Bunker** ngoài cleanroom |
| 🔴 P0 | Litho ISO 6 sát Wet Bench ISO 7 → AMC risk cực cao |
| 🟠 P1 | Chemical Store trong CR + cạnh ATP – nguy hiểm |
| 🟠 P1 | Material flow đi chung personnel aisle |
| 🟠 P1 | Documentation thiếu thông số kỹ thuật cơ bản |

---

## 4. SO SÁNH ĐỊNH TÍNH

### 4.1 Design A – "Engineering-Driven Fab Architecture"

> **Triết lý:** Zero cross-contamination by complex zoning + pressure engineering

**Điểm mạnh nổi bật:**
- Tư duy semiconductor fab hiện đại, mature
- Pressure cascade, waste segregation, chemical engineering chuyên nghiệp
- Documentation đủ chi tiết cho Schematic Design
- Phù hợp: MEMS / Lithography R&D / Advanced university fab / Pilot semiconductor line

**Điểm yếu cốt lõi:**
- EHS egress chưa đạt chuẩn (1 exit duy nhất)
- Phức tạp, dễ collapse cascade khi vận hành thực
- Khó mở rộng quy mô

### 4.2 Design B – "Equipment Arrangement"

> **Triết lý:** Simple linear layout, easy to operate and expand

**Điểm mạnh nổi bật:**
- Layout tuyến tính dễ vận hành, dễ scale
- Tách utility ra ngoài cleanroom rất rõ ràng
- Multi-exit tốt cho egress
- Phù hợp: Teaching cleanroom / Basic university lab / Low-risk process

**Điểm yếu cốt lõi:**
- Chưa đạt mức cleanroom engineering chuẩn
- Bi-directional flow phá vỡ kiểm soát ô nhiễm
- Thiếu hầu hết các thành phần cốt lõi của fab thật (airshower, pass-box, cascade, barrier, chase)

---

## 5. MA TRẬN QUYẾT ĐỊNH LỰA CHỌN

| Tình huống sử dụng | Khuyến nghị |
|---|---|
| R&D fab nghiêm túc, sub-µm process, yield cao | **Design A** (sau khi fix Top P0) |
| Lab học thuật, R&D startup, prototype, micrometer process | **Design B** (sau khi bổ sung cơ bản) |
| MEMS, photonics, advanced packaging R&D | **Design A** |
| Sinh viên, đào tạo, low-risk process | **Design B** |
| Multi-shift, sản xuất ổn định | **Design A** |
| Ngân sách hạn chế, dễ scale | **Design B** |
| Sản xuất thương mại | **Design A** + nâng cấp Industrial-grade |

---

## 6. KHUYẾN NGHỊ CẢI TIẾN

### 6.1 Nâng cấp Design A → "Industrial Fab thật"

**P0 – Bắt buộc trước thi công:**
- [ ] Bổ sung exit thứ 2 (NFPA compliance)
- [ ] Sửa cascade: De-gown ≥ +12 Pa, Airshower ≤ +8 Pa
- [ ] Tách Acid/Solvent bench thành 2 phòng riêng
- [ ] Bổ sung AMC chemical filter cho Litho MAU
- [ ] Bổ sung gas detection tại từng zone + EMO matrix

**P1 – Trước vận hành:**
- [ ] Subfab / interstitial utility floor
- [ ] Tách 3 luồng nhân sự (clean / chemical / maintenance)
- [ ] Wafer return path riêng (AMHS hoặc bypass pass-box)
- [ ] Tách Service Chase: Acid / Solvent / Utility riêng
- [ ] Vibration isolation foundation cho metrology, litho
- [ ] Mini-environment cho Litho

**P2 – Hoàn thiện:**
- [ ] MAU/AHU redundancy (N+1)
- [ ] Bulk gas yard, UPW loop, Chemical Distribution Room
- [ ] Pressure monitoring nodes (BMS)
- [ ] Fire compartmentation (1-hour fire wall)
- [ ] Future expansion knock-out panels

### 6.2 Nâng cấp Design B → "Pilot R&D Fab"

**P0 – Bổ sung cơ bản (gần như redesign):**
- [ ] Airshower giữa Gowning và CR
- [ ] De-gowning room riêng
- [ ] One-way personnel flow (tách entry/exit hoàn toàn)
- [ ] Pass-box và Material Airlock
- [ ] Pressure cascade thực sự (định nghĩa từng phòng)
- [ ] Contamination Barrier Wall
- [ ] Service chase / Subfab
- [ ] Chemical Bunker ngoài trời
- [ ] Acid/Solvent waste segregation
- [ ] 3 stack riêng + scrubber + neutralization

**P1 – Tối ưu:**
- [ ] AMC protection cho Litho
- [ ] Mini-environment cho Litho
- [ ] Tách Chemical Store ra khỏi cleanroom
- [ ] Gas detection từng zone
- [ ] Documentation kỹ thuật đầy đủ (áp suất, ACH, FFU, ΔP)

---

## 7. ĐỀ XUẤT HYBRID DESIGN V4.0

> **Lấy điểm mạnh của cả hai → tạo thiết kế tối ưu**

| Module | Lấy từ |
|---|---|
| Pressure cascade chi tiết, Material flow, Pass-box logic | Design A |
| Linear modular bay layout (dễ scale) | Design B |
| Contamination Barrier Wall + ATP loop riêng | Design A |
| Utility tách ngoài (AHU × 2, Gas, Scrubber, RO, CDA) | Design B |
| 3-stack exhaust + Chemical Bunker + Waste segregation | Design A |
| Multi-exit phân bổ đều (NFPA) | Design B |
| Documentation kỹ thuật chi tiết | Design A |
| Modular tool placement (mỗi phòng độc lập) | Design B |

→ Đây sẽ là design **"industrial-grade + operation-friendly + scalable"**, tối ưu cho R&D Cleanroom Fab Việt Nam giai đoạn pilot → scale-up.

---

## 8. KẾT LUẬN CUỐI CÙNG

### Đánh giá tổng thể
> **Design A (V3.2)** là một thiết kế *"fab architecture"* trưởng thành – giải quyết triệt để bài toán **"Zero Cross-Contamination"** bằng kết hợp hoàn hảo giữa **layout vật lý one-way + pressure cascade chuẩn xác + chemical engineering chuyên nghiệp**.
>
> **Design B** mang tính chất **"equipment arrangement"** – tối ưu hóa diện tích, dễ vận hành và dễ mở rộng, nhưng **hy sinh hoàn toàn các tiêu chuẩn kiểm soát nhiễm chéo cơ bản** của phòng sạch fab semiconductor.
>
> Design B cần **redesign nhiều phần cốt lõi** mới có thể tiệm cận fab thật; Design A chỉ cần **fix Top P0** là vận hành được ngay.

### Khuyến nghị cuối
1. **Ngắn hạn:** Sử dụng **Design A** làm cơ sở thiết kế chính, fix Top P0 trước thi công
2. **Trung hạn:** Áp dụng **Hybrid Design V4.0** kết hợp ưu điểm của cả hai
3. **Dài hạn:** Nâng cấp lên **Industrial Fab thật** với subfab, AMHS, AMC control, redundancy

---

## 9. PHỤ LỤC

### 9.1 Danh mục tiêu chuẩn áp dụng
- ISO 14644-1: Cleanroom classification
- ISO 14644-4: Cleanroom design, construction, start-up
- SEMI S2: Environmental, Health, Safety guidelines for semiconductor manufacturing equipment
- SEMI S6: Safety guidelines for hazardous materials
- SEMI S8: Safety guidelines for ergonomics
- NFPA 101: Life Safety Code
- ANSI Z358.1: Emergency eyewash and shower equipment
- QCVN 06:2022/BXD: Quy chuẩn kỹ thuật quốc gia về an toàn cháy
- IEST RP-CC012: Cleanroom design considerations

### 9.2 Bước tiếp theo đề xuất
- [ ] Vẽ phác thảo **Hybrid Design V4.0**
- [ ] Lập **Decision Matrix** chi tiết cho stakeholder
- [ ] Lập **HAZOP** cho Chemical Lane của Design A
- [ ] Lập **Action Plan & Cost Estimate** nâng cấp Design B
- [ ] **CFD simulation** cho Litho zone của cả hai
- [ ] Lập **Door Interlock Matrix** và **Pressure Monitoring Map**

---

**Người lập:** Comparative Design Assessment Team
**Ngày:** [Cần điền]
**Phê duyệt:** [Cần điền]
**Phân phối:** Project Manager / EHS Manager / Design Lead / QA Manager

---

*Tài liệu này nhằm mục đích đánh giá kỹ thuật, hỗ trợ quyết định thiết kế. Mọi điều chỉnh layout cuối cùng cần được kiểm chứng bằng CFD simulation, HAZOP study và tuân thủ quy định pháp luật địa phương.*
