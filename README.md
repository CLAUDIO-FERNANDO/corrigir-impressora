# corrigir-impressora
comando para corrigir erro de compatilhamento de impressoras 


Com o método abaixo é possível solucionar a questão do erro de compartilhamento de impressoras de rede sem a remoção da atualização.

Abra o prompt de comando como Administrador;

Execute o comando abaixo:
REG ADD HKLM\System\CurrentControlSet\Control\Print /v RpcAuthnLevelPrivacyEnabled /t REG_DWORD /d 0 /f

Reinicie o serviço Spooler de impressão com o comando abaixo:
net stop spooler && net start spooler

Teste a impressão novamente.
