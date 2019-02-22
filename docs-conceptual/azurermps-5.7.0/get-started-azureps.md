---
title: Начало работы с Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/15/2017
ms.openlocfilehash: a64bc4f07a5dc7d3f42e13877ed3bca53c4987d3
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56145140"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="4c341-102">Начало работы с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c341-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="4c341-103">Модуль Azure PowerShell предназначен для администрирования ресурсов Azure из командной строки, а также для создания скриптов автоматизации, которые работают с Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4c341-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="4c341-104">Его можно использовать в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4c341-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="4c341-105">В этой статье содержатся инструкции по началу работы с Azure PowerShell и объясняются основные принципы работы этого модуля.</span><span class="sxs-lookup"><span data-stu-id="4c341-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="4c341-106">Установите Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c341-106">Install Azure PowerShell</span></span>

<span data-ttu-id="4c341-107">Сначала установите последнюю версию модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c341-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="4c341-108">Сведения о последнем выпуске см. в [заметках о выпуске](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="4c341-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="4c341-109">[Установите Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="4c341-109">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="4c341-110">Чтобы проверить установку, выполните `Get-InstalledModule AzureRM -AllVersions` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="4c341-110">To verify the installation was successful, run `Get-InstalledModule AzureRM -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="4c341-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="4c341-111">Azure Cloud Shell</span></span>

<span data-ttu-id="4c341-112">Самый простой способ начать работу — [запустить службу Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="4c341-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="4c341-113">Запустите Cloud Shell с верхней панели навигации портала Azure.</span><span class="sxs-lookup"><span data-stu-id="4c341-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Значок оболочки](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="4c341-115">Выберите нужную подписку и создайте учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="4c341-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![Создание учетной записи хранения](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="4c341-117">Когда хранилище будет создано, Cloud Shell откроет сеанс PowerShell в браузере.</span><span class="sxs-lookup"><span data-stu-id="4c341-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Использование Cloud Shell с PowerShell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="4c341-119">Вы также можете установить Azure PowerShell для локального использования в сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c341-119">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="4c341-120">Вход в Azure</span><span class="sxs-lookup"><span data-stu-id="4c341-120">Sign in to Azure</span></span>

<span data-ttu-id="4c341-121">Войдите в интерактивном режиме:</span><span class="sxs-lookup"><span data-stu-id="4c341-121">Sign on interactively:</span></span>

1. <span data-ttu-id="4c341-122">Введите `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="4c341-122">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="4c341-123">Появится диалоговое окно с запросом на ввод учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4c341-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="4c341-124">С помощью параметра -Environment можно войти в Azure для Китая или Azure для Германии.</span><span class="sxs-lookup"><span data-stu-id="4c341-124">Option '-Environment' can let you login in Azure China or Azure Germany.</span></span>

   <span data-ttu-id="4c341-125">Пример: Connect-AzureRmAccount -Environment AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="4c341-125">e.g. Connect-AzureRmAccount -Environment AzureChinaCloud</span></span>

2. <span data-ttu-id="4c341-126">Введите электронный адрес и пароль, связанные с вашей учетной записью.</span><span class="sxs-lookup"><span data-stu-id="4c341-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="4c341-127">Azure выполняет проверку подлинности и сохраняет учетные данные, а затем закрывает окно.</span><span class="sxs-lookup"><span data-stu-id="4c341-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="4c341-128">После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для доступа к ресурсам в подписке и управления ими.</span><span class="sxs-lookup"><span data-stu-id="4c341-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="4c341-129">Создание виртуальной машины Windows с помощью простых значений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4c341-129">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="4c341-130">У командлета `New-AzureRmVM` упрощенный синтаксис, что облегчает создание виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4c341-130">The `New-AzureRmVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="4c341-131">Вам нужно указать только два значения параметров: имя виртуальной машины и учетные данные локального администратора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4c341-131">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="4c341-132">Сначала мы создадим объект учетных данных.</span><span class="sxs-lookup"><span data-stu-id="4c341-132">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="4c341-133">Затем — виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="4c341-133">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

<span data-ttu-id="4c341-134">Это достаточно просто.</span><span class="sxs-lookup"><span data-stu-id="4c341-134">That was easy.</span></span> <span data-ttu-id="4c341-135">Но может возникнуть вопрос, что при этом еще создается, а также как настроена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="4c341-135">But, you may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="4c341-136">Сначала посмотрим на наши группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c341-136">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="4c341-137">Группа ресурсов **cloud-shell-storage-westus** создается при первом использовании Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="4c341-137">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="4c341-138">Группа ресурсов **SampleVM** создается командлетом `New-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="4c341-138">The **SampleVM** resource group was created by the `New-AzureRmVM` cmdlet.</span></span>

<span data-ttu-id="4c341-139">Но какие же ресурсы созданы в этой новой группе ресурсов?</span><span class="sxs-lookup"><span data-stu-id="4c341-139">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

<span data-ttu-id="4c341-140">Давайте получим дополнительные сведения о виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4c341-140">Let's get some more details about the VM.</span></span> <span data-ttu-id="4c341-141">В этих примерах показано, как получить сведения об образе операционной системы, используемом для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4c341-141">This examples shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="4c341-142">Создание полностью настроенной виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="4c341-142">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="4c341-143">В предыдущем примере для создания виртуальной машины Windows используется упрощенный синтаксис и значения параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4c341-143">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="4c341-144">В этом примере мы предоставляем значения для всех параметров виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4c341-144">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="4c341-145">Создание группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4c341-145">Create a resource group</span></span>

<span data-ttu-id="4c341-146">В этом примере мы создадим группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c341-146">For this example we want to create a Resource Group.</span></span> <span data-ttu-id="4c341-147">Группы ресурсов в Azure позволяют управлять разными ресурсами, которые вы хотите логически сгруппировать.</span><span class="sxs-lookup"><span data-stu-id="4c341-147">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="4c341-148">Например, вы можете создать группу ресурсов для приложения или проекта, а затем добавить в эту группу виртуальную машину, базу данных и службу CDN.</span><span class="sxs-lookup"><span data-stu-id="4c341-148">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="4c341-149">Создайте группу ресурсов с именем MyResourceGroup в регионе Azure "Западная Европа".</span><span class="sxs-lookup"><span data-stu-id="4c341-149">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="4c341-150">Используйте для этого следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4c341-150">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="4c341-151">Эта новая группа ресурсов будет использоваться для размещения всех ресурсов, необходимых для создаваемой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4c341-151">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="4c341-152">Чтобы создать виртуальную машину Linux, сначала нужно создать необходимые ресурсы и назначить их в качестве конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4c341-152">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="4c341-153">Затем эту конфигурацию можно использовать для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4c341-153">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="4c341-154">Кроме того, вам потребуется открытый ключ SSH `id_rsa.pub` в каталоге формата SSH вашего профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c341-154">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="4c341-155">Создание необходимых сетевых ресурсов</span><span class="sxs-lookup"><span data-stu-id="4c341-155">Create the required network resources</span></span>

<span data-ttu-id="4c341-156">Сначала создайте конфигурацию подсети, которая будет использоваться для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4c341-156">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="4c341-157">Также нужно создать общедоступный IP-адрес, чтобы можно было подключаться к этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4c341-157">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="4c341-158">Создайте группу безопасности сети для защиты доступа к общедоступному адресу.</span><span class="sxs-lookup"><span data-stu-id="4c341-158">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="4c341-159">Наконец, создайте виртуальный сетевой адаптер, используя все предыдущие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="4c341-159">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="4c341-160">Создание конфигурации виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="4c341-160">Create the VM configuration</span></span>

<span data-ttu-id="4c341-161">Теперь, когда у вас есть необходимые ресурсы, можно создать объект конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4c341-161">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="4c341-162">Создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="4c341-162">Create the virtual machine</span></span>

<span data-ttu-id="4c341-163">Теперь мы можем создать виртуальную машину, используя объект конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4c341-163">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="4c341-164">Вы можете войти на созданную виртуальную машину Linux, используя SSH и общедоступный IP-адрес этой виртуальной машины:</span><span class="sxs-lookup"><span data-stu-id="4c341-164">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="4c341-165">Создание других ресурсов в Azure</span><span class="sxs-lookup"><span data-stu-id="4c341-165">Creating other resources in Azure</span></span>

<span data-ttu-id="4c341-166">Вы узнали, как создавать группы ресурсов, а также виртуальные машины Linux и Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4c341-166">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="4c341-167">Но вы также можете создать в Azure много других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c341-167">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="4c341-168">Например, чтобы создать подсистему балансировки нагрузки Azure, которую можно затем связать с новой виртуальной машиной, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4c341-168">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="4c341-169">Также для своей инфраструктуры вы можете создать новую частную виртуальную сеть, используя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4c341-169">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="4c341-170">Преимущество Azure и Azure PowerShell заключается в том, что их можно использовать для создания как облачной инфраструктуры, так и управляемых служб платформы.</span><span class="sxs-lookup"><span data-stu-id="4c341-170">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="4c341-171">Управляемые службы платформы также можно объединять с инфраструктурой, создавая еще более мощные решения.</span><span class="sxs-lookup"><span data-stu-id="4c341-171">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="4c341-172">Например, используя Azure PowerShell, вы можете создать службу приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="4c341-172">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="4c341-173">Служба приложений Azure — это управляемая служба платформы, на которой можно размещать веб-приложения, не беспокоясь об инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="4c341-173">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="4c341-174">Создав службу приложений Azure, вы можете создать два новых веб-приложения Azure с помощью следующих команд:</span><span class="sxs-lookup"><span data-stu-id="4c341-174">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="4c341-175">Отображение списка развернутых ресурсов</span><span class="sxs-lookup"><span data-stu-id="4c341-175">Listing deployed resources</span></span>

<span data-ttu-id="4c341-176">Чтобы вывести список ресурсов, работающих в Azure, используйте командлет `Get-AzureRmResource`.</span><span class="sxs-lookup"><span data-stu-id="4c341-176">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="4c341-177">В следующем примере показаны ресурсы, входящие в созданную группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c341-177">The following example shows the resources we just created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="4c341-178">Удаление ресурсов</span><span class="sxs-lookup"><span data-stu-id="4c341-178">Deleting resources</span></span>

<span data-ttu-id="4c341-179">Чтобы очистить учетную запись Azure, необходимо удалить ресурсы, созданные в этом примере.</span><span class="sxs-lookup"><span data-stu-id="4c341-179">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="4c341-180">Используйте командлеты `Remove-AzureRm*` для удаления ресурсов, которые больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="4c341-180">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="4c341-181">Чтобы удалить виртуальную машину Windows, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4c341-181">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="4c341-182">Вам будет предложено подтвердить удаление указанных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c341-182">You will be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4c341-183">Также можно удалить несколько ресурсов одновременно.</span><span class="sxs-lookup"><span data-stu-id="4c341-183">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="4c341-184">Например, следующая команда удаляет всю группу ресурсов MyResourceGroup, связанную со всеми примерами в этом руководстве по началу работы.</span><span class="sxs-lookup"><span data-stu-id="4c341-184">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="4c341-185">Эта команда удаляет группу ресурсов и все ресурсы, которые группа содержит.</span><span class="sxs-lookup"><span data-stu-id="4c341-185">This removes the resource group and all of the resources in it.</span></span>

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4c341-186">Это может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="4c341-186">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="4c341-187">Получение примеров</span><span class="sxs-lookup"><span data-stu-id="4c341-187">Get samples</span></span>

<span data-ttu-id="4c341-188">Дополнительные сведения о способах использования Azure PowerShell см. в примерах популярных сценариев для [виртуальных машин Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [виртуальных машин Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [веб-приложений](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) и [баз данных SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="4c341-188">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="4c341-189">Дополнительная информация</span><span class="sxs-lookup"><span data-stu-id="4c341-189">Next steps</span></span>

* [<span data-ttu-id="4c341-190">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c341-190">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="4c341-191">Управление подписками Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c341-191">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="4c341-192">Создание субъектов-служб в Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c341-192">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="4c341-193">Ознакомьтесь с заметками о выпуске, касающимися миграции с более ранней версии: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="4c341-193">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="4c341-194">Помощь от сообщества:</span><span class="sxs-lookup"><span data-stu-id="4c341-194">Get help from the community:</span></span>
  * [<span data-ttu-id="4c341-195">Форум Azure на MSDN</span><span class="sxs-lookup"><span data-stu-id="4c341-195">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="4c341-196">Stackoverflow</span><span class="sxs-lookup"><span data-stu-id="4c341-196">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
