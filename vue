Если ошибка Watchpack Error (watcher): Error: ENOSPC: System limit for number of file watchers reached

# проверить значение 
cat /proc/sys/fs/inotify/max_user_watches

# insert the new value into the system config
echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p

# config variable name (not runnable)
fs.inotify.max_user_watches=524288


создать новый проект vite
npm init vite my_app --template vue-ts
потом вылезает меню:
Select a framework: › - Use arrow-keys. Return to submit.
❯   Vanilla
    Vue
    React
    Preact
    Lit
    Svelte
    Solid
    Qwik
    Others
    
typescript:
npx ts-node index.ts - исполнить файл .ts    
