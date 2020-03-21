Build custom docker image for mattermost

    docker build -t cloudgenius/mattermost .
    docker push cloudgenius/mattermost

Create NFS mount points

    k exec -it test sh
    mkdir -p mattermostdata mattermostlogs mattermostconfig mattermostplugins
    chown -R 1000:1000 mattermostdata mattermostlogs mattermostconfig mattermostplugins

mattermost database is not automatically created so you must exec into mysql pod and create 
mattermost DB
