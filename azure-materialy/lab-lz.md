<h1>Lab 1</h1><br>
Prerekvizity:<br>
•	Dedikovaná subscription s Contributor nebo Owner právy<br><br>
<b>Zadání</b><br>
Vytvořte si v subscription vlastní hub and spoke topologii splňující následující kritéria:<br>
<ul>
<li>Pro jednoduchost v tomto cvičení můžete dávat všechny zdroje v tomto cvičení do jedné resource groupy.
<li>Všechny zdroje vytvářejte v Europe West regionu.
<li>Můžete využít portal nebo AZ CLI.
<li>Označte resource group tagem environment:lab
<li>Buďte konzistentní ve své jmenné konvenci.
<li>Adresní rozsahy: Hub sít 10.0.0.0/24, spoke1 10.0.1.0/24, spoke2 10.0.2.0/24
<li>Subnety hub sítě: AzureFirewallSubnet /26, AzureBastionSubnet /26, GatewaySubnet /27
<li>Subnety spoke1 sítě: FrontendSubnet 10.0.1.0/26, BackendSubnet 10.0.1.64/26
<li>Subnety spoke2 sítě: FrontendSubnet 10.0.2.0/26, BackendSubnet 10.0.2.64/26
<li>Proveďte deployment Azure Firewall a Bastionu
  </ul><br>
Vytvořte mezi hubem a spoke sítěmi peerting.<br>
Připojte ke každé subnetu NSG kromě GatewaySubnetu, AzureFirewallSubnetu. Víte proč? Jak bude vypadat NSG na BastionSubnetu?<br>
Vytvořte si Windows VM ve spoke1 vnet, FrontendSubnet a připojte se na vzdálenou plochu pomocí bastionu.<br>
Ověřte dostupnost internetu z webového prohlížeče.<br>
Nastavte UDR, aby veškerý provoz byl směrován přes Azure Firewall.<br>
Zablokujte na firewallu adresu google.com a ověřte zablokování přes Windows VM.<br>
Aplikujte na Vaší resource group Azure Security Benchmark initiative v Azure Policies.<br>
Prohlédněte si ASB politiky. Co je to remediation taks? Jak lze udělat vlastní politiky?<br>
<br>
Optional: <br>
vytvořte si vlastní politiku a otestujte jeji funkčnost.<br>
Zdědte tag z resouce group na všechny zdroje uvnitř resource group.<br>
Vytvořte storage account a zintegrujte ho do BackendSubnetu spoke 2, využijte private endpoint. Otestujte komunikaci na blob storage z VM.<br>
Přidejte private DNS a otestuje.<br>
