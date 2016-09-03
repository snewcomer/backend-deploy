node {
  checkout scm

  stage 'Deploy application release'
  writeFile file: 'extras.json', text: "{'image_tag':'${IMAGE_TAG}','ecs_tasks':[${TASKS}]}"
  withEnv(["VAULT_PASSWORD=mypassword"])
}
