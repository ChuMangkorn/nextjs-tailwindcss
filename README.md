Pokemon Finder App with Next.js & Tailwind CSS



(แนะนำ: บันทึกภาพหน้าจอของแอปพลิเคชันที่รันเสร็จแล้ว และนำมาใส่ตรงนี้เพื่อให้คนอื่นเห็นภาพรวมของโปรเจกต์ได้ทันที)

📝 คำอธิบาย (Description)
โปรเจกต์นี้คือเว็บแอปพลิเคชันสำหรับค้นหาและแสดงข้อมูลโปเกมอน สร้างขึ้นด้วย Next.js (App Router) และใช้ Tailwind CSS ในการออกแบบหน้าตาให้สวยงามและตอบสนองต่อทุกขนาดหน้าจอ (Responsive) โดยดึงข้อมูลทั้งหมดมาจาก PokeAPI แบบ Real-time

ผู้ใช้สามารถดูรายชื่อโปเกมอนทั้งหมด, ค้นหาโปเกมอนที่ต้องการด้วยชื่อ, และคลิกเพื่อดูรายละเอียดเชิงลึกของโปเกมอนแต่ละตัวได้

✨ ฟีเจอร์หลัก (Features)
แสดงรายการโปเกมอน: แสดงรายชื่อโปเกมอนทั้งหมดพร้อมรูปภาพจาก PokeAPI
ค้นหาโปเกมอน: สามารถกรอกชื่อโปเกมอนในช่องค้นหาเพื่อแสดงข้อมูลของโปเกมอนตัวนั้นๆ
ดูข้อมูลรายละเอียด: คลิกที่โปเกมอนเพื่อเข้าไปยังหน้าแสดงรายละเอียดเฉพาะตัว เช่น น้ำหนัก, ความสามารถ (Abilities), และประเภท (Types)
Routing แบบไดนามิก: ใช้ Dynamic Routes ของ Next.js ในการสร้างหน้ารายละเอียดสำหรับโปเกมอนแต่ละตัว (/pokeinfo/[id]) และหน้าผลการค้นหา (/pokesearch/[pokeName])
ดีไซน์สวยงามและทันสมัย: ออกแบบด้วย Tailwind CSS และใช้ Font จาก next/font (Geist)
Client-Side Rendering (CSR): ใช้ useEffect และ useState ในการดึงและจัดการข้อมูลฝั่ง Client
🛠️ เทคโนโลยีที่ใช้ (Tech Stack)
Framework: Next.js 15
Library: React 19
Styling: Tailwind CSS
Data Fetching API: PokeAPI
Linting: ESLint
Deployment: แนะนำให้ใช้ Vercel
🚀 การติดตั้งและเริ่มใช้งาน (Getting Started)
ทำตามขั้นตอนต่อไปนี้เพื่อรันโปรเจกต์บนเครื่องของคุณ

สิ่งที่ต้องมี (Prerequisites)
Node.js (เวอร์ชัน 18.18.0 หรือสูงกว่า)
npm, yarn, หรือ pnpm
ขั้นตอนการติดตั้ง
Clone a repository:

Bash

git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
ติดตั้ง Dependencies:

Bash

npm install
รัน Development Server:

Bash

npm run dev
เปิดเบราว์เซอร์แล้วไปที่ http://localhost:3000 เพื่อดูผลลัพธ์

📜 Scripts ที่มีให้ (Available Scripts)
ในโปรเจกต์นี้มี Scripts ที่ตั้งค่าไว้แล้วดังนี้:

npm run dev: รันแอปพลิเคชันในโหมด Development
npm run build: สร้างแอปพลิเคชันสำหรับ Production
npm run start: รันแอปพลิเคชันที่ Build เสร็จแล้ว (โหมด Production)
npm run lint: ตรวจสอบความถูกต้องของโค้ดด้วย ESLint
🔧 การกำหนดค่า (Configuration)
Environment Variables
โปรเจกต์นี้ใช้ PokeAPI ซึ่งเป็น Public API จึง ไม่จำเป็นต้องตั้งค่า Environment Variables ใดๆ เพิ่มเติม

การตั้งค่า Next.js (next.config.mjs)
มีการตั้งค่าเพิ่มเติมเพื่อให้สามารถแสดงรูปภาพจาก raw.githubusercontent.com ซึ่งเป็นแหล่งที่มาของรูปโปเกมอนได้

JavaScript

/** @type {import('next').NextConfig} */
const nextConfig = {
  images:{
    domains:["raw.githubusercontent.com"]
  }
};
export default nextConfig;
📄 ใบอนุญาต (License)
โปรเจกต์นี้อยู่ภายใต้ใบอนุญาต MIT ดูรายละเอียดเพิ่มเติมได้ที่ไฟล์ LICENSE
