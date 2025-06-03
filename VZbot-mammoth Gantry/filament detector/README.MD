Not project, but currently working on integrating the Roadrunner filament detector to my printer:
https://github.com/EiNSTeiN-/roadrunner-filament-sensor/releases

had issue with the original fork.
there was a branch that was created the fixed the issue.
had to remove the original project

rm -rf /home/iroots/roadrunner-filament-sensor

do the mainsail config:
[update_manager roadrunner_filament_sensor]
type: git_repo
path: /home/iroots/roadrunner-filament-sensor
origin: https://github.com/CookiezRGood/roadrunner-filament-sensor.git
install_script: install.sh
primary_branch: patch-2
managed_services: klipper


Chat gpt came in clutch:
finally clone the new repo
git clone -b patch-2 https://github.com/CookiezRGood/roadrunner-filament-sensor.git /home/iroots/roadrunner-filament-sensor
