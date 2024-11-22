# Windows SERVER 2019 VM summon


## Configure WINRM

    # WinRM aktivieren
    Enable-PSRemoting -Force

    # Remote-Verbindungen über WinRM zulassen (verhindert Verbindungsprobleme)
    Set-Item WSMan:\localhost\client\trustedhosts -Value "*" -Force

    # Firewall für WinRM öffnen
    New-NetFirewallRule -Name "WinRM" -DisplayName "Windows Remote Management" -Enabled True -Protocol TCP -Direction Inbound -LocalPort 5985




## How to Run the code 

If every other step is followed you just need to run this code 
    ```ansible-playbook -i hosts.md create_vm.yml```


