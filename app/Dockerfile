# SINGLE STAGE BUILD
FROM node:20.15.1-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY ./ ./
RUN npm run build
EXPOSE 3000
CMD ["npm", "run", "start"]

# MULTI STAGE BUILD
# # Stage 1: Build Stage
# FROM node:20.15.1-alpine AS builder
# WORKDIR /app
# COPY package*.json ./
# RUN npm install --omit=dev
# COPY . .
# RUN npm run build
# # Stage 2: Production Stage
# FROM node:20.15.1-alpine AS runner
# WORKDIR /app
# COPY --from=builder /app/package.json ./
# COPY --from=builder /app/node_modules ./node_modules
# COPY --from=builder /app/.next ./.next
# COPY --from=builder /app/public ./public
# EXPOSE 3000
# CMD ["npm", "run", "start"]