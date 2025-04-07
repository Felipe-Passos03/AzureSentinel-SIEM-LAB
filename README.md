<h1>SIEM - AZURE SENTINEL</h1>

<h2>Descrição</h2>
Project consists of a simple PowerShell script that walks the user through "zeroing out" (wiping) any drives that are connected to the system. The utility allows you to select the target disk and choose the number of passes that are performed. The PowerShell script will configure a diskpart script file based on the user's selections and then launch Diskpart to perform the disk sanitization.
<br />


<h2>Ferramentas utilizadas</h2>

- <b>PowerShell</b> 
- <b>Diskpart</b>

<h2>Ambientes usados</h2>

- <b>Windows 10</b> (21H2)

<h2>Como foi feito:</h2>

<p align="center">
Logando na VM criada a partir do Azure: <br/>
<img src="https://i.imgur.com/IYsputv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <br>
 Desabilitando as defesas do Windows para tornar a VM vunerável a ataques: <br/>
<img src="https://i.imgur.com/8QaFsCf_d.webp?maxwidth=760&fidelity=grand" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="https://i.imgur.com/Bru0Odr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <br>
 Conferindo se a VM está sendo alcançada pela internet (está)<br/>
 <img src="https://i.imgur.com/CrSrUPV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <br>
  <br>
 Verificando tentativas de intrusão da VM através do EventViewer<br/>
 <img src="https://i.imgur.com/T5yfzjx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <br>
   <br>
 Criando um log analytics workspace e adicionando no Azure Sentinel, irá permitir vizualizar as logs de eventos que estão ocorrendo dentro da VM<br/>
 <img src="https://i.imgur.com/TWtOYgc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <br>
   <br>
 Instalando o Windows security event para coletar logs de segurança da VM <br/>
 <img src="https://i.imgur.com/1DlmxIM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <br>
 <br>
 Permitindo logs através o Azure monitor Windows Agent  <br/>
 <img src="https://i.imgur.com/vHh0EMh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <br>
 <br>
 Filtrando logs com KQL - Como a imagem mostra, estão tentando realizar um RDP brute force na VM  <br/>
 <img src="https://i.imgur.com/Et6NZGX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <br>
 <br>
 Adicionando geolocalização dos ataques através do Sentinel <br/>
 <img src="https://i.imgur.com/J7kscdF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <br>
 <br>
 Através de um workbook criado no Azure sentinel, é possível ver o mapa de ataque em tempo real a VM. <br/>
 <img src="https://i.imgur.com/2Z3bTJQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <br>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
