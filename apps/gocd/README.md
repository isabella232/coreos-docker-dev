GoCD in a Box
=================================

* [GoCD-Docker](https://github.com/gocd/gocd-docker)
* [GoCD Documentation](https://www.go.cd/documentation/user/current/)


Start GitLab Services
======================
    cd units
    fleetctl start gocd.service
    # wait for http://172.17.8.101:8153 is up
    fleetctl start gocd-agent-ci-base.service
    fleetctl start gocd-agent-ci-app.service
    fleetctl start gocd-agent-cd-dev.service
    fleetctl start gocd-agent-cd-stage.service
    fleetctl start gocd-agent-cd-prod.service

check service status and get the gitlab service ip:

    fleetctl list-units
    ping gocd.docker.local

open http://gocd.docker.local:8153 or http://172.17.8.101:8153
