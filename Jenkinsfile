#!groovy

pipeline {

  agent any

  environment {
    GIT_URL = "https://github.com/jenkinsfiles-ansible-playbooks-configs/ansible-ci.git"
  }

  parameters {
    string(
      name: 'GIT_BRANCHES',
      defaultValue: '',
      description: "Git branch or tag name or commit id of GIT_URL of Jenkins job configuration file"
    )
  }

  stages {
    stage('Ansible CI') {
      failFast false
      parallel {
        stage('Ansible local') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "local/ansible/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_ansible_local"
                            )
                          ]
          }
        }

        stage('Ansible ssh') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "ssh/ansible/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_ansible_ssh"
                            )
                          ]
          }
        }

        stage('AWS CLI local') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "local/awscli/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_awscli_local"
                            )
                          ]
          }
        }

        stage('AWS CLI ssh') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "ssh/awscli/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_awscli_ssh"
                            )
                          ]
          }
        }

        stage('AWX local') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "local/awx/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_awx_local"
                            )
                          ]
          }
        }

        stage('AWX ssh') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "ssh/awx/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_awx_ssh"
                            )
                          ]
          }
        }

        stage('Chrome local') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "local/chrome/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_chrome_local"
                            )
                          ]
          }
        }

        stage('Chrome ssh') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "ssh/chrome/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_chrome_ssh"
                            )
                          ]
          }
        }

        stage('Docker local') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "local/docker/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_docker_local"
                            )
                          ]
          }
        }

        stage('Docker ssh') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "ssh/docker/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_docker_ssh"
                            )
                          ]
          }
        }

        stage('Jenkins local') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "local/jenkins_install/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_jenkins_install_local"
                            )
                          ]
          }
        }

        stage('Jenkins ssh') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "ssh/jenkins_install/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_jenkins_install_ssh"
                            )
                          ]
          }
        }

        stage('PlantUML Server local') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "local/plantuml_server/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_plantuml_server_local"
                            )
                          ]
          }
        }

        stage('PlantUML Server ssh') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "ssh/plantuml_server/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_plantuml_server_ssh"
                            )
                          ]
          }
        }

        stage('VNC Server local') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "local/vnc_server/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_vnc_server_local"
                            )
                          ]
          }
        }

        stage('VNC Server ssh') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'CONFIG_FILE_PATH',
                              value: "ssh/vnc_server/config.yml"
                            ),
                            string(
                              name: 'GIT_BRANCHES',
                              value: "${params.GIT_BRANCHES}"
                            ),
                            string(
                              name: 'GIT_URL',
                              value: "${env.GIT_URL}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jeknins_job_ansible_cli_vnc_server_ssh"
                            )
                          ]
          }
        }

      }
    }
  }
}
