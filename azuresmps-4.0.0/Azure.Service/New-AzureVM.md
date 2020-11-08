---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076200"
---
# <span data-ttu-id="dcb60-101">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="dcb60-101">New-AzureVM</span></span>

## <span data-ttu-id="dcb60-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcb60-102">SYNOPSIS</span></span>
<span data-ttu-id="dcb60-103">Создание виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="dcb60-103">Creates an Azure virtual machine.</span></span>

## <span data-ttu-id="dcb60-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcb60-104">SYNTAX</span></span>

### <span data-ttu-id="dcb60-105">ExistingService (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcb60-105">ExistingService (Default)</span></span>
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dcb60-106">CreateService</span><span class="sxs-lookup"><span data-stu-id="dcb60-106">CreateService</span></span>
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dcb60-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcb60-107">DESCRIPTION</span></span>
<span data-ttu-id="dcb60-108">Командлет **New-AzureVM** добавляет новую виртуальную машину к существующей службе Azure или создает виртуальную машину и службу в текущей подписке, если задано *Расположение* или *AffinityGroup* .</span><span class="sxs-lookup"><span data-stu-id="dcb60-108">The **New-AzureVM** cmdlet adds a new virtual machine to an existing Azure service, or creates a virtual machine and service in the current subscription if either the *Location* or *AffinityGroup* is specified.</span></span>

## <span data-ttu-id="dcb60-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcb60-109">EXAMPLES</span></span>

### <span data-ttu-id="dcb60-110">Пример 1: создание виртуальной машины для конфигурации Windows</span><span class="sxs-lookup"><span data-stu-id="dcb60-110">Example 1: Create a virtual machine for a Windows configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

<span data-ttu-id="dcb60-111">Эта команда создает конфигурацию подготовки на основе конфигурации виртуальной машины для операционной системы Windows и использует ее для создания виртуальной машины в указанной территориальной группе.</span><span class="sxs-lookup"><span data-stu-id="dcb60-111">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="dcb60-112">Пример 2: создание виртуальной машины для конфигурации Linux</span><span class="sxs-lookup"><span data-stu-id="dcb60-112">Example 2: Create a virtual machine for a Linux configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

<span data-ttu-id="dcb60-113">Эта команда создает конфигурацию подготовки на основе конфигурации виртуальной машины для Linux и использует ее для создания виртуальной машины в указанной территориальной группе.</span><span class="sxs-lookup"><span data-stu-id="dcb60-113">This command creates a provisioning configuration based on a virtual machine configuration for Linux, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="dcb60-114">Пример 3: создание виртуальной машины и Добавление диска с данными</span><span class="sxs-lookup"><span data-stu-id="dcb60-114">Example 3: Create a virtual machine and add a data disk</span></span>
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

<span data-ttu-id="dcb60-115">Первые две команды получают доступные изображения с помощью командлета **Get-AzureVMImage** и сохраняют один из них в переменной $Image.</span><span class="sxs-lookup"><span data-stu-id="dcb60-115">The first two commands get available images by using the **Get-AzureVMImage** cmdlet, and stores one of them in the $Image variable.</span></span>

<span data-ttu-id="dcb60-116">Эта команда создает конфигурацию подготовки на основе конфигурации виртуальной машины для операционной системы Windows и использует ее для создания виртуальной машины с помощью диска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dcb60-116">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with an Azure data disk.</span></span>

### <span data-ttu-id="dcb60-117">Пример 4: создание виртуальной машины с зарезервированным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="dcb60-117">Example 4: Create a virtual machine with a reserved IP address</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

<span data-ttu-id="dcb60-118">Эта команда создает конфигурацию подготовки на основе конфигурации виртуальной машины для операционной системы Windows и использует ее для создания виртуальной машины с зарезервированным IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="dcb60-118">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with a reserved IP address.</span></span>

## <span data-ttu-id="dcb60-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcb60-119">PARAMETERS</span></span>

### <span data-ttu-id="dcb60-120">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="dcb60-120">-AffinityGroup</span></span>
<span data-ttu-id="dcb60-121">Указывает территориальную группу Azure, в которой находится облачная служба.</span><span class="sxs-lookup"><span data-stu-id="dcb60-121">Specifies the Azure affinity group in which the cloud service resides.</span></span>
<span data-ttu-id="dcb60-122">Этот параметр является обязательным только в том случае, если этот командлет создает облачную службу.</span><span class="sxs-lookup"><span data-stu-id="dcb60-122">This parameter is required only when this cmdlet creates a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-123">-DeploymentLabel</span><span class="sxs-lookup"><span data-stu-id="dcb60-123">-DeploymentLabel</span></span>
<span data-ttu-id="dcb60-124">Указывает метку для развертывания.</span><span class="sxs-lookup"><span data-stu-id="dcb60-124">Specifies a label for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="dcb60-125">-DeploymentName</span></span>
<span data-ttu-id="dcb60-126">Указывает имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="dcb60-126">Specifies a deployment name.</span></span>
<span data-ttu-id="dcb60-127">Если не указано, этот командлет использует имя службы в качестве имени развертывания.</span><span class="sxs-lookup"><span data-stu-id="dcb60-127">If not specified, this cmdlet uses the service name as the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-128">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="dcb60-128">-DnsSettings</span></span>
<span data-ttu-id="dcb60-129">Указывает объект DNS-сервера, который определяет параметры DNS для нового развертывания.</span><span class="sxs-lookup"><span data-stu-id="dcb60-129">Specifies a DNS Server object that defines the DNS settings for the new deployment.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dcb60-130">-InformationAction</span></span>
<span data-ttu-id="dcb60-131">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="dcb60-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dcb60-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="dcb60-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dcb60-133">Продолжал</span><span class="sxs-lookup"><span data-stu-id="dcb60-133">Continue</span></span>
- <span data-ttu-id="dcb60-134">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="dcb60-134">Ignore</span></span>
- <span data-ttu-id="dcb60-135">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="dcb60-135">Inquire</span></span>
- <span data-ttu-id="dcb60-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dcb60-136">SilentlyContinue</span></span>
- <span data-ttu-id="dcb60-137">Остановить</span><span class="sxs-lookup"><span data-stu-id="dcb60-137">Stop</span></span>
- <span data-ttu-id="dcb60-138">Рвать</span><span class="sxs-lookup"><span data-stu-id="dcb60-138">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dcb60-139">-InformationVariable</span></span>
<span data-ttu-id="dcb60-140">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="dcb60-140">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-141">-InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="dcb60-141">-InternalLoadBalancerConfig</span></span>
<span data-ttu-id="dcb60-142">Указывает внутренний балансировщик нагрузки.</span><span class="sxs-lookup"><span data-stu-id="dcb60-142">Specifies an internal load balancer.</span></span>
<span data-ttu-id="dcb60-143">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="dcb60-143">This parameter is not used.</span></span>

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-144">-Location</span><span class="sxs-lookup"><span data-stu-id="dcb60-144">-Location</span></span>
<span data-ttu-id="dcb60-145">Указывает место, на котором размещена новая служба.</span><span class="sxs-lookup"><span data-stu-id="dcb60-145">Specifies the location that hosts the new service.</span></span>
<span data-ttu-id="dcb60-146">Если служба уже существует, не указывайте этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dcb60-146">If the service already exists, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="dcb60-147">-Profile</span></span>
<span data-ttu-id="dcb60-148">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dcb60-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dcb60-149">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dcb60-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-150">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="dcb60-150">-ReservedIPName</span></span>
<span data-ttu-id="dcb60-151">Задает имя зарезервированного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="dcb60-151">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-152">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="dcb60-152">-ReverseDnsFqdn</span></span>
<span data-ttu-id="dcb60-153">Указывает полное доменное имя для обратного DNS-имени.</span><span class="sxs-lookup"><span data-stu-id="dcb60-153">Specifies the fully-qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-154">-ServiceDescription</span><span class="sxs-lookup"><span data-stu-id="dcb60-154">-ServiceDescription</span></span>
<span data-ttu-id="dcb60-155">Задает описание новой службы.</span><span class="sxs-lookup"><span data-stu-id="dcb60-155">Specifies a description for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-156">-ServiceLabel</span><span class="sxs-lookup"><span data-stu-id="dcb60-156">-ServiceLabel</span></span>
<span data-ttu-id="dcb60-157">Указывает метку для новой службы.</span><span class="sxs-lookup"><span data-stu-id="dcb60-157">Specifies a label for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dcb60-158">-ServiceName</span></span>
<span data-ttu-id="dcb60-159">Указывает новое или существующее имя службы.</span><span class="sxs-lookup"><span data-stu-id="dcb60-159">Specifies the new or existing service name.</span></span>

<span data-ttu-id="dcb60-160">Если служба не существует, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="dcb60-160">If the service does not exist, this cmdlet creates it for you.</span></span>
<span data-ttu-id="dcb60-161">Укажите место для создания службы с помощью параметра *Location* или *AffinityGroup* .</span><span class="sxs-lookup"><span data-stu-id="dcb60-161">Use the *Location* or *AffinityGroup* parameter to specify where to create the service.</span></span>

<span data-ttu-id="dcb60-162">Если служба существует, параметр *Location* или *AffinityGroup* не требуется.</span><span class="sxs-lookup"><span data-stu-id="dcb60-162">If the service exists, the *Location* or *AffinityGroup* parameter is not needed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-163">-VMS</span><span class="sxs-lookup"><span data-stu-id="dcb60-163">-VMs</span></span>
<span data-ttu-id="dcb60-164">Указывает список объектов виртуальной машины для создания.</span><span class="sxs-lookup"><span data-stu-id="dcb60-164">Specifies a list of virtual machine objects to create.</span></span>

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-165">-VNetName</span><span class="sxs-lookup"><span data-stu-id="dcb60-165">-VNetName</span></span>
<span data-ttu-id="dcb60-166">Указывает имя виртуальной сети, на котором этот командлет развертывает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="dcb60-166">Specifies the virtual network name where this cmdlet deploys the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-167">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="dcb60-167">-WaitForBoot</span></span>
<span data-ttu-id="dcb60-168">Указывает, что этот командлет ожидает, пока виртуальная машина не достигнет состояния **ReadyRole** .</span><span class="sxs-lookup"><span data-stu-id="dcb60-168">Specifies that this cmdlet waits for the virtual machine to reach the **ReadyRole** state.</span></span>
<span data-ttu-id="dcb60-169">Этот командлет завершает работу со сбоем, если виртуальная машина находится в одном из следующих состояний в ожидании: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="dcb60-169">This cmdlet fails if the virtual machine falls in one of the following states while waiting: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb60-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcb60-170">CommonParameters</span></span>
<span data-ttu-id="dcb60-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcb60-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcb60-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcb60-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcb60-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcb60-173">INPUTS</span></span>

## <span data-ttu-id="dcb60-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcb60-174">OUTPUTS</span></span>

## <span data-ttu-id="dcb60-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcb60-175">NOTES</span></span>

## <span data-ttu-id="dcb60-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcb60-176">RELATED LINKS</span></span>

[<span data-ttu-id="dcb60-177">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="dcb60-177">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="dcb60-178">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="dcb60-178">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="dcb60-179">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="dcb60-179">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="dcb60-180">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="dcb60-180">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


