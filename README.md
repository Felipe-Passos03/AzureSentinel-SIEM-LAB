<h1>SIEM - AZURE SENTINEL</h1>

<h2>Descrição</h2>
Projeto consiste em demonstrar na prática o número de ataques recebidos em tempo real a uma VM sem configurações de segurança. Através do monitoramento do Azure Sentinel, é possível criar alertas e definir métricas.
<br />


<h2>Ferramentas utilizadas</h2>

- <b>Azure Sentinel</b> 
- <b>Log Analytics Workspace</b>
- <b>KQL</b>

<h2>Ambientes usados</h2>

- <b>Windows 10 PRO VM</b> (21H2)

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
