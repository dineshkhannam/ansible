node {
    stage("git plull for dev"){
        checkout scm
    }
    stage("exectuing ansible playbook"){
        
        if  (env.BRANCH_NAME != 'master') {
       sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible-master', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'ansible-playbook -i /home/ansible/project1/ansible/prod-host /home/ansible/project1/ansible/install_docker.yml', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
    }
           if  (env.BRANCH_NAME != 'dev') {
       sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible-master', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'ansible-playbook -i /home/ansible/project1/ansible/dev-host /home/ansible/project1/ansible/install_docker.yml', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
    }
           if  (env.BRANCH_NAME != 'qa') {
       sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible-master', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'ansible-playbook -i /home/ansible/project1/ansible/qa-host /home/ansible/project1/ansible/install_docker.yml', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
    }
        
    }
    
    
}
