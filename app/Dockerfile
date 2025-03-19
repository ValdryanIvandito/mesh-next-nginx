# SINGLE STAGE BUILD
FROM node:20.15.1-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY ./ ./
RUN npm run build
EXPOSE 3000
CMD ["npm", "run", "start"]

# # MULTI STAGE BUILD
# # Stage 1: Build Stage
# FROM node:20.15.1-alpine AS builder
# WORKDIR /app

# # Copy package.json dan package-lock.json (lebih efisien untuk caching layer)
# COPY package*.json ./

# # Install dependencies tanpa menyertakan devDependencies di production
# RUN npm install --omit=dev

# # Copy seluruh kode sumber
# COPY . .

# # Build aplikasi Next.js
# RUN npm run build

# # Stage 2: Production Stage
# FROM node:20.15.1-alpine AS runner
# WORKDIR /app

# # Hanya copy file yang dibutuhkan untuk production
# COPY --from=builder /app/package.json ./
# COPY --from=builder /app/node_modules ./node_modules
# COPY --from=builder /app/.next ./.next
# COPY --from=builder /app/public ./public

# # Set ENV agar Next.js berjalan dalam mode production
# # ENV NODE_ENV=production
# EXPOSE 3000

# # Jalankan aplikasi dalam mode production
# CMD ["npm", "run", "start"]

# docker build -t miraclemonad/next app
# docker container create --name next -p 3000:3000 miraclemonad/next
# docker container start next
# docker container stop next