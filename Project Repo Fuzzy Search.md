```shell
epcd() {
 PROJECT_DEV_DIR=~/Git/example-project-dev
 TARGET_DIR=$(find $PROJECT_DEV_DIR -maxdepth 2 -type d | grep -v "/\." | sort | uniq | fzf +m -1 -e -i --query ${1:-""})
 if [ ! -z $TARGET_DIR ]; then 
  cd $TARGET_DIR
 fi
}
```