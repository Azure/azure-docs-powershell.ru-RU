---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 24e90ebae59c9d9a4449c57270b7ca69f9b05b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233505"
---
# <span data-ttu-id="c46ef-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="c46ef-101">New-AzCloudService</span></span>

## <span data-ttu-id="c46ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c46ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c46ef-103">Создайте или обновйте облачную службу.</span><span class="sxs-lookup"><span data-stu-id="c46ef-103">Create or update a cloud service.</span></span>
<span data-ttu-id="c46ef-104">Обратите внимание, что некоторые свойства можно настроить только при создании облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="c46ef-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c46ef-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c46ef-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c46ef-106">DESCRIPTION</span></span>
<span data-ttu-id="c46ef-107">Создайте или обновйте облачную службу.</span><span class="sxs-lookup"><span data-stu-id="c46ef-107">Create or update a cloud service.</span></span>
<span data-ttu-id="c46ef-108">Обратите внимание, что некоторые свойства можно настроить только при создании облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="c46ef-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c46ef-109">EXAMPLES</span></span>

### <span data-ttu-id="c46ef-110">Пример 1. Создание облачной службы с одной ролью</span><span class="sxs-lookup"><span data-stu-id="c46ef-110">Example 1: Create new cloud service with single role</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile
```

<span data-ttu-id="c46ef-111">Над набором команд создается облачная служба с одной ролью</span><span class="sxs-lookup"><span data-stu-id="c46ef-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="c46ef-112">Пример 2. Создание облачной службы с одной ролью и расширением RDP</span><span class="sxs-lookup"><span data-stu-id="c46ef-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosoOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
PS C:\> $extensionProfile = @{extension = @($extension)}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile
```

<span data-ttu-id="c46ef-113">Над набором команд создается облачная служба с одной ролью и расширением RDP.</span><span class="sxs-lookup"><span data-stu-id="c46ef-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="c46ef-114">Пример 3. Создание облачной службы с одной ролью и сертификатом из хранилища ключа</span><span class="sxs-lookup"><span data-stu-id="c46ef-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create OS profile object
$keyVault = Get-AzKeyVault -ResourceGroupName ContosOrg -VaultName ContosKeyVault
$certificate=Get-AzKeyVaultCertificate -VaultName ContosKeyVault -Name ContosCert
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
$osProfile = @{secret = @($secretGroup)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -OSProfile $osProfile
```

<span data-ttu-id="c46ef-115">С помощью вышеуказанного набора команд создается облачная служба с одной ролью и сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="c46ef-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="c46ef-116">Пример 4. Создание облачной службы с несколькими ролями и расширениями</span><span class="sxs-lookup"><span data-stu-id="c46ef-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
```powershell
# Create role profile object
PS C:\> $role1 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $role2 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoBackend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role1, $role2)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'

# Create Geneva extension object
PS C:\> $genevaExtension = New-AzCloudServiceExtensionObject -Name GenevaExtension -Publisher Microsoft.Azure.Geneva -Type GenevaMonitoringPaaS -TypeHandlerVersion "2.14.0.2"
PS C:\> $extensionProfile = @{extension = @($rdpExtension, $genevaExtension)}

# Add tags
$tag=@{"Owner" = "Contoso"}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile                           `
                  -Tag $tag
```

<span data-ttu-id="c46ef-117">С помощью вышеуказанного набора команд создается облачная служба с одной ролью и сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="c46ef-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="c46ef-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c46ef-118">PARAMETERS</span></span>

### <span data-ttu-id="c46ef-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c46ef-119">-AsJob</span></span>
<span data-ttu-id="c46ef-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c46ef-120">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-121">-Configuration</span><span class="sxs-lookup"><span data-stu-id="c46ef-121">-Configuration</span></span>
<span data-ttu-id="c46ef-122">Определяет конфигурацию службы XML (CSCFG) для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-123">-ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="c46ef-123">-ConfigurationUrl</span></span>
<span data-ttu-id="c46ef-124">Указывает URL-адрес, который ссылается на расположение конфигурации службы в службе BLOB-проект.</span><span class="sxs-lookup"><span data-stu-id="c46ef-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="c46ef-125">URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения. Это свойство является свойством только для записи и не возвращается при звонках GET.</span><span class="sxs-lookup"><span data-stu-id="c46ef-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c46ef-126">-DefaultProfile</span></span>
<span data-ttu-id="c46ef-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c46ef-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="c46ef-128">-ExtensionProfile</span></span>
<span data-ttu-id="c46ef-129">Описание профиля расширения облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="c46ef-130">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств EXTENSIONPROFILE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c46ef-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceExtensionProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-131">-Location</span><span class="sxs-lookup"><span data-stu-id="c46ef-131">-Location</span></span>
<span data-ttu-id="c46ef-132">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c46ef-132">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c46ef-133">-Name</span></span>
<span data-ttu-id="c46ef-134">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-134">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-135">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c46ef-135">-NetworkProfile</span></span>
<span data-ttu-id="c46ef-136">Профиль сети для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="c46ef-137">Чтобы построить, см. раздел "ЗАМЕТКИ" для свойств NETWORKPROFILE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c46ef-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceNetworkProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c46ef-138">-NoWait</span></span>
<span data-ttu-id="c46ef-139">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="c46ef-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="c46ef-140">-OSProfile</span></span>
<span data-ttu-id="c46ef-141">В статье описан профиль ОС для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="c46ef-142">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств OSPROFILE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c46ef-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="c46ef-143">-PackageUrl</span></span>
<span data-ttu-id="c46ef-144">Url-адрес, который ссылается на расположение пакета службы в службе BLOB-документов.</span><span class="sxs-lookup"><span data-stu-id="c46ef-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="c46ef-145">URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения. Это свойство является свойством только для записи и не возвращается при звонках GET.</span><span class="sxs-lookup"><span data-stu-id="c46ef-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c46ef-146">-ResourceGroupName</span></span>
<span data-ttu-id="c46ef-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c46ef-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="c46ef-148">-RoleProfile</span></span>
<span data-ttu-id="c46ef-149">Описание профиля роли для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="c46ef-150">Чтобы построить новую таблицу, см. раздел "Заметки" для свойств ROLEPROFILE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c46ef-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceRoleProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="c46ef-151">-StartCloudService</span></span>
<span data-ttu-id="c46ef-152">(Необязательно) Указывает, следует ли запускать облачную службу сразу после ее создания.</span><span class="sxs-lookup"><span data-stu-id="c46ef-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="c46ef-153">Значение по `true` умолчанию: . Если этот код ложный, модель обслуживания по-прежнему развертывается, но не сразу же запустится.</span><span class="sxs-lookup"><span data-stu-id="c46ef-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="c46ef-154">Вместо этого служба будет иметь poweredOff, пока вы не позвоните в службу "Начните", и она будет запущена.</span><span class="sxs-lookup"><span data-stu-id="c46ef-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="c46ef-155">С развернутой службы по-прежнему взимается плата, даже если она отключена.</span><span class="sxs-lookup"><span data-stu-id="c46ef-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c46ef-156">-SubscriptionId</span></span>
<span data-ttu-id="c46ef-157">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c46ef-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c46ef-158">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="c46ef-159">-Tag</span></span>
<span data-ttu-id="c46ef-160">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c46ef-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="c46ef-161">-UpgradeMode</span></span>
<span data-ttu-id="c46ef-162">Режим обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="c46ef-163">При развертывании службы для обновления доменов выделяются экземпляры ролей.</span><span class="sxs-lookup"><span data-stu-id="c46ef-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="c46ef-164">Обновления можно за инициативой обновления вручную в каждом домене обновления или автоматически во всех доменах обновления. Возможные значения: автоматически вручную, если не указано, по умолчанию \<br /\> \<br /\>  \<br /\> \<br /\>  \<br /\> \<br /\>  \<br /\> \<br /\> задано значение "Авто". Чтобы применить обновление вручную, необходимо создать put UpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="c46ef-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="c46ef-165">Если за установлено автоматическое обновление, обновление автоматически применяется к каждому домену обновления последовательно.</span><span class="sxs-lookup"><span data-stu-id="c46ef-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.CloudServiceUpgradeMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c46ef-166">-Confirm</span></span>
<span data-ttu-id="c46ef-167">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c46ef-167">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c46ef-168">-WhatIf</span></span>
<span data-ttu-id="c46ef-169">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c46ef-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c46ef-170">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c46ef-170">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46ef-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c46ef-171">CommonParameters</span></span>
<span data-ttu-id="c46ef-172">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c46ef-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c46ef-173">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c46ef-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c46ef-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c46ef-174">INPUTS</span></span>

## <span data-ttu-id="c46ef-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c46ef-175">OUTPUTS</span></span>

### <span data-ttu-id="c46ef-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="c46ef-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="c46ef-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c46ef-177">NOTES</span></span>

<span data-ttu-id="c46ef-178">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c46ef-178">ALIASES</span></span>

<span data-ttu-id="c46ef-179">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c46ef-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c46ef-180">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c46ef-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c46ef-181">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c46ef-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c46ef-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile> : описание профиля расширения облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="c46ef-183">`[Extension <IExtension[]>]`: Список расширений для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="c46ef-184">`[AutoUpgradeMinorVersion <Boolean?>]`. Явным образом укажите, может ли платформа автоматически обновлять TypeHandlerVersion до более мелких версий, когда они станут доступны.</span><span class="sxs-lookup"><span data-stu-id="c46ef-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="c46ef-185">`[ForceUpdateTag <String>]`Тег, чтобы принудительно применить предоставленные общедоступные и защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="c46ef-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="c46ef-186">Изменение значения тега позволяет повторно запускать расширение без изменения общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="c46ef-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="c46ef-187">Если параметр forceUpdateTag не изменился, обработник по-прежнему будет применять обновления общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="c46ef-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="c46ef-188">Если ни принудительное изменение параметра,ни каких-либо из общедоступных или защищенных параметров не изменилось, расширение будет перенаправляться в экземпляр роли с одинаковым номером последовательности и будет возможно повторное внедрение.</span><span class="sxs-lookup"><span data-stu-id="c46ef-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="c46ef-189">`[Name <String>]`: имя расширения.</span><span class="sxs-lookup"><span data-stu-id="c46ef-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="c46ef-190">`[ProtectedSetting <String>]`: Защищенные параметры расширения, которые шифруются перед его отправлением в экземпляр роли.</span><span class="sxs-lookup"><span data-stu-id="c46ef-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="c46ef-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c46ef-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="c46ef-192">`[Publisher <String>]`: имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="c46ef-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="c46ef-193">`[RolesAppliedTo <String[]>]`: Необязательный список ролей для применения этого расширения.</span><span class="sxs-lookup"><span data-stu-id="c46ef-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="c46ef-194">Если свойство не указано или указано "\*", расширение применяется для всех ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="c46ef-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="c46ef-195">`[Setting <String>]`: общедоступные параметры расширения.</span><span class="sxs-lookup"><span data-stu-id="c46ef-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="c46ef-196">Для расширений JSON это параметры JSON.</span><span class="sxs-lookup"><span data-stu-id="c46ef-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="c46ef-197">Для расширения XML (например, RDP) это параметр XML для расширения.</span><span class="sxs-lookup"><span data-stu-id="c46ef-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="c46ef-198">`[SourceVaultId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="c46ef-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="c46ef-199">`[Type <String>]`: тип расширения.</span><span class="sxs-lookup"><span data-stu-id="c46ef-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="c46ef-200">`[TypeHandlerVersion <String>]`: Определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="c46ef-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="c46ef-201">Определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="c46ef-201">Specifies the version of the extension.</span></span> <span data-ttu-id="c46ef-202">Если этот элемент не указан или в качестве значения используется звездочка (\*), используется последняя версия расширения.</span><span class="sxs-lookup"><span data-stu-id="c46ef-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="c46ef-203">Если задан номер основной версии и звездочка как дополнительный номер версии (X.), будет выбрана последняя дополнительный версия указанной основной версии.</span><span class="sxs-lookup"><span data-stu-id="c46ef-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="c46ef-204">Если указан основной номер версии и небольшой номер версии (X.Y), будет выбрана конкретная версия расширения.</span><span class="sxs-lookup"><span data-stu-id="c46ef-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="c46ef-205">Если указана версия, для экземпляра роли выполняется автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="c46ef-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="c46ef-206">NETWORKPROFILE: <ICloudServiceNetworkProfile> профиль сети для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="c46ef-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`Список конфигураций балансиров нагрузки для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="c46ef-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Список IP-адресов</span><span class="sxs-lookup"><span data-stu-id="c46ef-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="c46ef-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c46ef-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="c46ef-210">`[PrivateIPAddress <String>]`: личный IP-адрес, на который ссылается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="c46ef-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="c46ef-211">`[PublicIPAddressId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="c46ef-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="c46ef-212">`[SubnetId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="c46ef-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="c46ef-213">`[Name <String>]`: Название ресурса</span><span class="sxs-lookup"><span data-stu-id="c46ef-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="c46ef-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="c46ef-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="c46ef-215">`[Id <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="c46ef-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="c46ef-216">OSPROFILE <ICloudServiceOSProfile> : описание профиля ОС для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="c46ef-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Набор сертификатов, которые нужно установить на экземпляры ролей.</span><span class="sxs-lookup"><span data-stu-id="c46ef-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="c46ef-218">`[SourceVaultId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="c46ef-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="c46ef-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: список ссылок на основные хранилища в SourceVault, которые содержат сертификаты.</span><span class="sxs-lookup"><span data-stu-id="c46ef-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="c46ef-220">`[CertificateUrl <String>]`. Это URL-адрес сертификата, который был выложен в хранилище ключей в качестве секретного.</span><span class="sxs-lookup"><span data-stu-id="c46ef-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="c46ef-221">ROLEPROFILE <ICloudServiceRoleProfile> : описание профиля роли для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="c46ef-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: Список ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="c46ef-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="c46ef-223">`[Name <String>]`: название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c46ef-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="c46ef-224">`[SkuCapacity <Int64?>]`Определяет количество экземпляров ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="c46ef-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="c46ef-225">`[SkuName <String>]`: название SKU.</span><span class="sxs-lookup"><span data-stu-id="c46ef-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="c46ef-226">ПРИМЕЧАНИЕ. Если новый SKU не поддерживается на оборудовании, наемное облачным сервисом, необходимо удалить и воссоздать облачную службу или вернуться к старым SKU.</span><span class="sxs-lookup"><span data-stu-id="c46ef-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="c46ef-227">`[SkuTier <String>]`: уровень облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c46ef-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="c46ef-228">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="c46ef-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="c46ef-229">**Стандартный**</span><span class="sxs-lookup"><span data-stu-id="c46ef-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="c46ef-230">**Базовая**</span><span class="sxs-lookup"><span data-stu-id="c46ef-230">**Basic**</span></span>

## <span data-ttu-id="c46ef-231">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c46ef-231">RELATED LINKS</span></span>

