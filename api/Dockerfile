FROM --platform=linux/amd64 public.ecr.aws/lambda/nodejs:20

WORKDIR ${LAMBDA_TASK_ROOT}

COPY package*.json ./

# skip devDependencies
RUN npm install --production

COPY src ${LAMBDA_TASK_ROOT}/src

CMD ["app.handler"]

