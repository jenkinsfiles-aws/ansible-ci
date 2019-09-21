#!groovy

pipeline {

  agent any

  environment {
    GIT_URL_ANSIBLECFG = "https://github.com/TomonoriMatsumura/ansible-cfg.git"

    SSH_PRIVATE_KEY = "centos7.pem"
  }

  parameters {
    string(
      name: 'ANSIBLE_INVENTORY_FILE_NAME',
      defaultValue: '',
      description: "ansible-playbook command inventory file name"
    )
  }

  stages {
    stage('Ansible CI') {
      failFast false 
      parallel {
        stage('Install ansible') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "yum-update-all-and-reboot.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_SYSTEM}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l ansible"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "ansible"
                            )
                          ]

            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "install.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_ANSIBLE}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l ansible"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "ansible"
                            )
                          ]
          }
        }
    
        stage('Install AWS CLI') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "yum-update-all-and-reboot.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_SYSTEM}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l awscli"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "awscli"
                            )
                          ]

            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "install.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_AWSCLI}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l awscli"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "awscli"
                            )
                          ]
          }
        }
    
        stage('Install AWX') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "yum-update-all-and-reboot.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_SYSTEM}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l awx"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "awx"
                            )
                          ]

            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "install.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_AWX}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l awx"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "awx"
                            )
                          ]
          }
        }
    
        stage('Install chrome') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "yum-update-all-and-reboot.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_SYSTEM}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l chrome"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "chrome"
                            )
                          ]

            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "install.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_CHROME}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l chrome"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "chrome"
                            )
                          ]
          }
        }

        stage('Install docker') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "yum-update-all-and-reboot.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_SYSTEM}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l docker"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "docker"
                            )
                          ]

            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "install.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_DOCKER}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l docker"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "docker"
                            )
                          ]
          }
        }

        stage('Install exa') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "yum-update-all-and-reboot.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_SYSTEM}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l exa"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "exa"
                            )
                          ]

            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "install.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_EXA}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l exa"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "exa"
                            )
                          ]


          }
        }

        stage('Install Jenkins') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "yum-update-all-and-reboot.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_SYSTEM}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l jenkins"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jenkins"
                            )
                          ]

            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "install.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_JENKINS_INSTALL}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l jenkins"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "jenkins_install"
                            )
                          ]
          }
        }

        stage('Install PlantUML Server') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "yum-update-all-and-reboot.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_SYSTEM}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l plantumlserver"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "plantumlserver"
                            )
                          ]

            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "install.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_PLANTUML_SERVER}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l plantumlserver"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "plantumlserver"
                            )
                          ]
          }
        }

        stage('Install VNC Server') {
          steps {
            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "yum-update-all-and-reboot.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_SYSTEM}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l vncserver"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "vncserver"
                            )
                          ]

            build job: 'ansible/playbook',
              parameters: [
                            string(
                              name: 'ANSIBLE_PLAYBOOK',
                              value: "install.yml"
                            ),
                            string(
                              name: 'GIT_URL_PLAYBOOKS',
                              value: "${env.GITHUB_ANSIBLE_CENTOS7_VNCSERVER}"
                            ),
                            string(
                              name: 'GIT_URL_ANSIBLECFG',
                              value: "${env.GIT_URL_ANSIBLECFG}"
                            ),
                            string(
                              name: 'INVENTORY_PARAMS',
                              value: "-i ${env.ANSIBLE_INVENTORY_FILES_DIR}/${params.ANSIBLE_INVENTORY_FILE_NAME} -l vncserver"
                            ),
                            string(
                              name: 'SSH_PRIVATE_KEY',
                              value: "${env.SSH_PRIVATE_KEY}"
                            ),
                            string(
                              name: 'WORKING_DIR',
                              value: "vncserver"
                            )
                          ]
          }
        }

      }
    }
  }
}