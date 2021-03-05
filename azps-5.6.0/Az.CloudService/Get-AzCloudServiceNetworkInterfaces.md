---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-AzCloudServiceNetworkInterfaces
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
ms.openlocfilehash: ae6bb602e90fd86334a28a804deed2be429347ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008104"
---
# <span data-ttu-id="d88dc-101">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="d88dc-101">Get-AzCloudServiceNetworkInterfaces</span></span>

## <span data-ttu-id="d88dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d88dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d88dc-103">Получите сетевые интерфейсы облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-103">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="d88dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d88dc-104">SYNTAX</span></span>

### <span data-ttu-id="d88dc-105">CloudServiceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d88dc-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-RoleInstanceName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d88dc-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="d88dc-106">CloudService</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudService <CloudService> [-SubscriptionId <String>]
 [-RoleInstanceName <String>] [<CommonParameters>]
```

## <span data-ttu-id="d88dc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d88dc-107">DESCRIPTION</span></span>
<span data-ttu-id="d88dc-108">Получите сетевые интерфейсы облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-108">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="d88dc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d88dc-109">EXAMPLES</span></span>

### <span data-ttu-id="d88dc-110">Пример 1. Получите сетевые интерфейсы по названию облачной службы</span><span class="sxs-lookup"><span data-stu-id="d88dc-110">Example 1: Get network interfaces by a cloud service name</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="d88dc-111">Получает все сетевые интерфейсы для имени облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-111">Gets all the network interfaces for a given cloud service name.</span></span>

### <span data-ttu-id="d88dc-112">Пример 2. Получите сетевые интерфейсы от объекта облачной службы</span><span class="sxs-lookup"><span data-stu-id="d88dc-112">Example 2: Get network interfaces by a cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs

```

<span data-ttu-id="d88dc-113">Получает все сетевые интерфейсы для данного объекта облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-113">Gets all the network interfaces for a given cloud service object.</span></span>

### <span data-ttu-id="d88dc-114">Пример 3. Получите сетевые интерфейсы по объекту облачной службы и имени экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="d88dc-114">Example 3: Get network interfaces by a cloud service object and role instance name.</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs -RoleInstanceName WebRole1_IN_0

```

<span data-ttu-id="d88dc-115">Получает все сетевые интерфейсы для объекта облачной службы и имени экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="d88dc-115">Gets all the network interfaces for a given cloud service object and role instance name.</span></span>

## <span data-ttu-id="d88dc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d88dc-116">PARAMETERS</span></span>

### <span data-ttu-id="d88dc-117">-CloudService</span><span class="sxs-lookup"><span data-stu-id="d88dc-117">-CloudService</span></span>
<span data-ttu-id="d88dc-118">Экземпляр CloudService.</span><span class="sxs-lookup"><span data-stu-id="d88dc-118">CloudService instance.</span></span>
<span data-ttu-id="d88dc-119">Чтобы построить, см. раздел "ЗАМЕТКИ" для свойств CLOUDSERVICE и создание таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="d88dc-119">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88dc-120">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="d88dc-120">-CloudServiceName</span></span>
<span data-ttu-id="d88dc-121">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="d88dc-121">CloudServiceName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88dc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d88dc-122">-ResourceGroupName</span></span>
<span data-ttu-id="d88dc-123">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="d88dc-123">ResourceGroupName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88dc-124">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="d88dc-124">-RoleInstanceName</span></span>
<span data-ttu-id="d88dc-125">RoleInstanceName.</span><span class="sxs-lookup"><span data-stu-id="d88dc-125">RoleInstanceName.</span></span>

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

### <span data-ttu-id="d88dc-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d88dc-126">-SubscriptionId</span></span>
<span data-ttu-id="d88dc-127">Подписка.</span><span class="sxs-lookup"><span data-stu-id="d88dc-127">Subscription.</span></span>

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

### <span data-ttu-id="d88dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88dc-128">CommonParameters</span></span>
<span data-ttu-id="d88dc-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d88dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88dc-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d88dc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88dc-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d88dc-131">INPUTS</span></span>

## <span data-ttu-id="d88dc-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d88dc-132">OUTPUTS</span></span>

## <span data-ttu-id="d88dc-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d88dc-133">NOTES</span></span>

<span data-ttu-id="d88dc-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d88dc-134">ALIASES</span></span>

<span data-ttu-id="d88dc-135">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d88dc-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d88dc-136">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d88dc-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d88dc-137">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d88dc-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d88dc-138">CLOUDSERVICE <CloudService> : экземпляр CloudService.</span><span class="sxs-lookup"><span data-stu-id="d88dc-138">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="d88dc-139">`Location <String>`: расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d88dc-139">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="d88dc-140">`[Configuration <String>]`Определяет конфигурацию службы XML (CSCFG) для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-140">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="d88dc-141">`[ConfigurationUrl <String>]`: указывает URL-адрес, который ссылается на расположение конфигурации службы в службе BLOB-бизнес.</span><span class="sxs-lookup"><span data-stu-id="d88dc-141">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="d88dc-142">URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-142">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="d88dc-143">Это свойство является свойством только для записи и не возвращается при звонках GET.</span><span class="sxs-lookup"><span data-stu-id="d88dc-143">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="d88dc-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Описание профиля расширения облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="d88dc-145">`[Extension <IExtension[]>]`: Список расширений для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-145">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="d88dc-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Укажите, может ли платформа автоматически обновлять TypeHandlerVersion до более высокого уровня, когда они становятся доступны.</span><span class="sxs-lookup"><span data-stu-id="d88dc-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="d88dc-147">`[ForceUpdateTag <String>]`: примените к тегу предоставленные общедоступные и защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="d88dc-147">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="d88dc-148">Изменение значения тега позволяет повторно запускать расширение без изменения общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="d88dc-148">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="d88dc-149">Если параметр forceUpdateTag не изменился, обработник по-прежнему будет применять обновления общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="d88dc-149">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="d88dc-150">Если ни принудительное изменение параметра,ни каких-либо из общедоступных или защищенных параметров не изменилось, расширение будет перенаправляться в экземпляр роли с одинаковым номером последовательности и будет возможно повторное внедрение.</span><span class="sxs-lookup"><span data-stu-id="d88dc-150">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="d88dc-151">`[Name <String>]`: имя расширения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-151">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="d88dc-152">`[ProtectedSetting <String>]`: Защищенные параметры расширения, которые шифруются перед его отправлением в экземпляр роли.</span><span class="sxs-lookup"><span data-stu-id="d88dc-152">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="d88dc-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="d88dc-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="d88dc-154">`[Publisher <String>]`: имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="d88dc-154">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="d88dc-155">`[RolesAppliedTo <String[]>]`: Необязательный список ролей для применения этого расширения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-155">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="d88dc-156">Если свойство не указано или указано "\*", расширение применяется для всех ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="d88dc-156">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="d88dc-157">`[Setting <String>]`: общедоступные параметры расширения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-157">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="d88dc-158">Для расширений JSON это параметры JSON.</span><span class="sxs-lookup"><span data-stu-id="d88dc-158">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="d88dc-159">Для расширения XML (например, RDP) это параметр XML для расширения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-159">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="d88dc-160">`[SourceVaultId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="d88dc-160">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="d88dc-161">`[Type <String>]`: тип расширения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-161">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="d88dc-162">`[TypeHandlerVersion <String>]`: определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-162">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="d88dc-163">Определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-163">Specifies the version of the extension.</span></span> <span data-ttu-id="d88dc-164">Если этот элемент не указан или в качестве значения используется звездочка (\*), используется последняя версия расширения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-164">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="d88dc-165">Если задан номер основной версии и звездочка как дополнительный номер версии (X.), будет выбрана последняя дополнительный версия указанной основной версии.</span><span class="sxs-lookup"><span data-stu-id="d88dc-165">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="d88dc-166">Если указан основной и второстепенный номер версии (X.Y), будет выбрана конкретная версия расширения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-166">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="d88dc-167">Если указана версия, для экземпляра роли выполняется автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="d88dc-167">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="d88dc-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Профиль сети для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="d88dc-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`Список конфигураций балансиров нагрузки для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="d88dc-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Список IP-адресов</span><span class="sxs-lookup"><span data-stu-id="d88dc-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="d88dc-171">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="d88dc-171">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="d88dc-172">`[PrivateIPAddress <String>]`: личный IP-адрес, на который ссылается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="d88dc-172">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="d88dc-173">`[PublicIPAddressId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="d88dc-173">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="d88dc-174">`[SubnetId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="d88dc-174">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="d88dc-175">`[Name <String>]`: Название ресурса</span><span class="sxs-lookup"><span data-stu-id="d88dc-175">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="d88dc-176">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="d88dc-176">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="d88dc-177">`[Id <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="d88dc-177">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="d88dc-178">`[OSProfile <ICloudServiceOSProfile>]`: описание профиля ОС для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-178">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="d88dc-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: набор сертификатов, которые должны быть установлены на экземпляры ролей.</span><span class="sxs-lookup"><span data-stu-id="d88dc-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="d88dc-180">`[SourceVaultId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="d88dc-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="d88dc-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: список ссылок на основные хранилища в SourceVault, которые содержат сертификаты.</span><span class="sxs-lookup"><span data-stu-id="d88dc-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="d88dc-182">`[CertificateUrl <String>]`. Это URL-адрес сертификата, который был выложен в хранилище ключей в качестве секретного.</span><span class="sxs-lookup"><span data-stu-id="d88dc-182">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="d88dc-183">`[PackageUrl <String>]`: указывает URL-адрес, который ссылается на расположение пакета обслуживания в службе BLOB-бизнес.</span><span class="sxs-lookup"><span data-stu-id="d88dc-183">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="d88dc-184">URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d88dc-184">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="d88dc-185">Это свойство является свойством только для записи и не возвращается при звонках GET.</span><span class="sxs-lookup"><span data-stu-id="d88dc-185">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="d88dc-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Описание профиля роли для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="d88dc-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: Список ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="d88dc-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="d88dc-188">`[Name <String>]`: название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d88dc-188">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="d88dc-189">`[SkuCapacity <Int64?>]`Определяет количество экземпляров ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="d88dc-189">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="d88dc-190">`[SkuName <String>]`: название SKU.</span><span class="sxs-lookup"><span data-stu-id="d88dc-190">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="d88dc-191">ПРИМЕЧАНИЕ. Если новый SKU не поддерживается на оборудовании, наномном оборудовании сейчас работает облачная служба, необходимо удалить и воссоздать облачную службу или вернуться к старым SKU.</span><span class="sxs-lookup"><span data-stu-id="d88dc-191">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="d88dc-192">`[SkuTier <String>]`: определяет уровень облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-192">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="d88dc-193">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d88dc-193">Possible Values are</span></span> <br /><br /> <span data-ttu-id="d88dc-194">**Стандартный**</span><span class="sxs-lookup"><span data-stu-id="d88dc-194">**Standard**</span></span> <br /><br /> <span data-ttu-id="d88dc-195">**Базовая**</span><span class="sxs-lookup"><span data-stu-id="d88dc-195">**Basic**</span></span>
  - <span data-ttu-id="d88dc-196">`[StartCloudService <Boolean?>]`: (Необязательно) Указывает, следует ли запускать облачную службу сразу после ее создания.</span><span class="sxs-lookup"><span data-stu-id="d88dc-196">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="d88dc-197">Значение по `true` умолчанию: .</span><span class="sxs-lookup"><span data-stu-id="d88dc-197">The default value is `true`.</span></span>         <span data-ttu-id="d88dc-198">Если этот код ложный, модель обслуживания по-прежнему развертывается, но не сразу же запустится.</span><span class="sxs-lookup"><span data-stu-id="d88dc-198">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="d88dc-199">Вместо этого служба будет иметь poweredOff, пока вы не позвоните в службу "Начните", и она будет запущена.</span><span class="sxs-lookup"><span data-stu-id="d88dc-199">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="d88dc-200">С развернутой службы по-прежнему взимается плата, даже если она отключена.</span><span class="sxs-lookup"><span data-stu-id="d88dc-200">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="d88dc-201">`[Tag <ICloudServiceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d88dc-201">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="d88dc-202">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="d88dc-202">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d88dc-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`Режим обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="d88dc-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="d88dc-204">При развертывании службы для обновления доменов выделяются экземпляры ролей.</span><span class="sxs-lookup"><span data-stu-id="d88dc-204">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="d88dc-205">Обновления можно за инициативой обновления вручную в каждом домене обновления или автоматически во всех доменах обновления.</span><span class="sxs-lookup"><span data-stu-id="d88dc-205">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="d88dc-206">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d88dc-206">Possible Values are</span></span> <br /><br /><span data-ttu-id="d88dc-207">**Авто**</span><span class="sxs-lookup"><span data-stu-id="d88dc-207">**Auto**</span></span><br /><br /><span data-ttu-id="d88dc-208">**Вручную**</span><span class="sxs-lookup"><span data-stu-id="d88dc-208">**Manual**</span></span> <br /><br /><span data-ttu-id="d88dc-209">**Одновременный**</span><span class="sxs-lookup"><span data-stu-id="d88dc-209">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="d88dc-210">Если не указано, по умолчанию задано значение "Авто". Чтобы применить обновление вручную, необходимо создать put UpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="d88dc-210">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="d88dc-211">Если за установлено автоматическое обновление, обновление автоматически применяется к каждому домену обновления последовательно.</span><span class="sxs-lookup"><span data-stu-id="d88dc-211">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="d88dc-212">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d88dc-212">RELATED LINKS</span></span>

