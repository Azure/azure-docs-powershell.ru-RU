---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: d875ad9af0ebe864f9d396fed44961a5d48f38c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975944"
---
# <span data-ttu-id="f7085-101">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="f7085-101">Get-AzCloudServicePublicIPAddress</span></span>

## <span data-ttu-id="f7085-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7085-102">SYNOPSIS</span></span>
<span data-ttu-id="f7085-103">Получите общедоступный IP-адрес облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-103">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="f7085-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7085-104">SYNTAX</span></span>

### <span data-ttu-id="f7085-105">CloudServiceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7085-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### <span data-ttu-id="f7085-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="f7085-106">CloudService</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="f7085-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7085-107">DESCRIPTION</span></span>
<span data-ttu-id="f7085-108">Получите общедоступный IP-адрес облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-108">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="f7085-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7085-109">EXAMPLES</span></span>

### <span data-ttu-id="f7085-110">Пример 1. Получите общедоступные IP-адреса уровня экземпляра для имени облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-110">Example 1: Get instance level public IP addresses for a given cloud service name.</span></span>
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="f7085-111">Возвращает общедоступные IP-адреса уровня экземпляра для имени облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-111">Gets the instance level public IP addresses for a given cloud service name.</span></span>

### <span data-ttu-id="f7085-112">Пример 2. Получите общедоступные IP-адреса уровня экземпляра для данного объекта облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-112">Example 2: Get instance level public IP addresses for a given cloud service object.</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

<span data-ttu-id="f7085-113">Возвращает общедоступные IP-адреса уровня экземпляра для данного объекта облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-113">Gets the instance level public IP addresses for a given cloud service object.</span></span>

## <span data-ttu-id="f7085-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7085-114">PARAMETERS</span></span>

### <span data-ttu-id="f7085-115">-CloudService</span><span class="sxs-lookup"><span data-stu-id="f7085-115">-CloudService</span></span>
<span data-ttu-id="f7085-116">Экземпляр CloudService.</span><span class="sxs-lookup"><span data-stu-id="f7085-116">CloudService instance.</span></span>
<span data-ttu-id="f7085-117">Чтобы построить, см. раздел "ЗАМЕТКИ" для свойств CLOUDSERVICE и создание таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="f7085-117">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f7085-118">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="f7085-118">-CloudServiceName</span></span>
<span data-ttu-id="f7085-119">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="f7085-119">CloudServiceName.</span></span>

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

### <span data-ttu-id="f7085-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7085-120">-ResourceGroupName</span></span>
<span data-ttu-id="f7085-121">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f7085-121">ResourceGroupName.</span></span>

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

### <span data-ttu-id="f7085-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7085-122">-SubscriptionId</span></span>
<span data-ttu-id="f7085-123">Подписка.</span><span class="sxs-lookup"><span data-stu-id="f7085-123">Subscription.</span></span>

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

### <span data-ttu-id="f7085-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7085-124">CommonParameters</span></span>
<span data-ttu-id="f7085-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7085-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7085-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7085-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7085-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7085-127">INPUTS</span></span>

## <span data-ttu-id="f7085-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7085-128">OUTPUTS</span></span>

## <span data-ttu-id="f7085-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7085-129">NOTES</span></span>

<span data-ttu-id="f7085-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f7085-130">ALIASES</span></span>

<span data-ttu-id="f7085-131">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f7085-131">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f7085-132">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f7085-132">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7085-133">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7085-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f7085-134">CLOUDSERVICE <CloudService> : экземпляр CloudService.</span><span class="sxs-lookup"><span data-stu-id="f7085-134">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="f7085-135">`Location <String>`: расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7085-135">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="f7085-136">`[Configuration <String>]`Определяет конфигурацию службы XML (CSCFG) для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-136">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="f7085-137">`[ConfigurationUrl <String>]`: указывает URL-адрес, который ссылается на расположение конфигурации службы в службе BLOB-бизнес.</span><span class="sxs-lookup"><span data-stu-id="f7085-137">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="f7085-138">URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7085-138">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="f7085-139">Это свойство является свойством только для записи и не возвращается при звонках GET.</span><span class="sxs-lookup"><span data-stu-id="f7085-139">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="f7085-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Описание профиля расширения облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="f7085-141">`[Extension <IExtension[]>]`: Список расширений для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-141">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="f7085-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Укажите, может ли платформа автоматически обновлять TypeHandlerVersion до более высокого уровня, когда они становятся доступны.</span><span class="sxs-lookup"><span data-stu-id="f7085-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="f7085-143">`[ForceUpdateTag <String>]`Тег, чтобы принудительно применить предоставленные общедоступные и защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="f7085-143">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="f7085-144">Изменение значения тега позволяет повторно запускать расширение без изменения общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="f7085-144">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="f7085-145">Если параметр forceUpdateTag не изменился, обработник по-прежнему будет применять обновления общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="f7085-145">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="f7085-146">Если ни принудительное изменение параметра,ни каких-либо из общедоступных или защищенных параметров не изменилось, расширение будет перенаправляться в экземпляр роли с одинаковым номером последовательности и будет управлять внедрением, нужно ли повторно запускать его.</span><span class="sxs-lookup"><span data-stu-id="f7085-146">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="f7085-147">`[Name <String>]`: имя расширения.</span><span class="sxs-lookup"><span data-stu-id="f7085-147">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="f7085-148">`[ProtectedSetting <String>]`: Защищенные параметры расширения, которые шифруются перед его отправлением в экземпляр роли.</span><span class="sxs-lookup"><span data-stu-id="f7085-148">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="f7085-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f7085-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="f7085-150">`[Publisher <String>]`: имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="f7085-150">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="f7085-151">`[RolesAppliedTo <String[]>]`: Необязательный список ролей для применения этого расширения.</span><span class="sxs-lookup"><span data-stu-id="f7085-151">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="f7085-152">Если свойство не указано или указано "\*", расширение применяется для всех ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="f7085-152">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="f7085-153">`[Setting <String>]`: общедоступные параметры расширения.</span><span class="sxs-lookup"><span data-stu-id="f7085-153">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="f7085-154">Для расширений JSON это параметры JSON.</span><span class="sxs-lookup"><span data-stu-id="f7085-154">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="f7085-155">Для расширения XML (например, RDP) это параметр XML для расширения.</span><span class="sxs-lookup"><span data-stu-id="f7085-155">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="f7085-156">`[SourceVaultId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f7085-156">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="f7085-157">`[Type <String>]`: тип расширения.</span><span class="sxs-lookup"><span data-stu-id="f7085-157">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="f7085-158">`[TypeHandlerVersion <String>]`: определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="f7085-158">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="f7085-159">Определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="f7085-159">Specifies the version of the extension.</span></span> <span data-ttu-id="f7085-160">Если этот элемент не указан или в качестве значения используется звездочка (\*), используется последняя версия расширения.</span><span class="sxs-lookup"><span data-stu-id="f7085-160">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="f7085-161">Если задан номер основной версии и звездочка как дополнительный номер версии (X.), будет выбрана последняя дополнительный версия указанной основной версии.</span><span class="sxs-lookup"><span data-stu-id="f7085-161">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="f7085-162">Если указан основной и второстепенный номер версии (X.Y), будет выбрана конкретная версия расширения.</span><span class="sxs-lookup"><span data-stu-id="f7085-162">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="f7085-163">Если указана версия, для экземпляра роли выполняется автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="f7085-163">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="f7085-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Профиль сети для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="f7085-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`Список конфигураций балансиров нагрузки для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="f7085-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Список IP-адресов</span><span class="sxs-lookup"><span data-stu-id="f7085-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="f7085-167">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f7085-167">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="f7085-168">`[PrivateIPAddress <String>]`: личный IP-адрес, на который ссылается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="f7085-168">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="f7085-169">`[PublicIPAddressId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f7085-169">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="f7085-170">`[SubnetId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f7085-170">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="f7085-171">`[Name <String>]`: Название ресурса</span><span class="sxs-lookup"><span data-stu-id="f7085-171">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="f7085-172">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="f7085-172">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="f7085-173">`[Id <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f7085-173">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="f7085-174">`[OSProfile <ICloudServiceOSProfile>]`: Описание профиля ОС для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-174">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="f7085-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Набор сертификатов, которые нужно установить на экземпляры ролей.</span><span class="sxs-lookup"><span data-stu-id="f7085-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="f7085-176">`[SourceVaultId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f7085-176">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="f7085-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: список ссылок на основные хранилища в SourceVault, которые содержат сертификаты.</span><span class="sxs-lookup"><span data-stu-id="f7085-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="f7085-178">`[CertificateUrl <String>]`. Это URL-адрес сертификата, который был выложен в хранилище ключей в качестве секретного.</span><span class="sxs-lookup"><span data-stu-id="f7085-178">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="f7085-179">`[PackageUrl <String>]`: указывает URL-адрес, который ссылается на расположение пакета службы в службе BLOB-бизнес.</span><span class="sxs-lookup"><span data-stu-id="f7085-179">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="f7085-180">URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7085-180">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="f7085-181">Это свойство является свойством только для записи и не возвращается при звонках GET.</span><span class="sxs-lookup"><span data-stu-id="f7085-181">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="f7085-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Описание профиля роли для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="f7085-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: Список ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="f7085-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="f7085-184">`[Name <String>]`: название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7085-184">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="f7085-185">`[SkuCapacity <Int64?>]`Определяет количество экземпляров ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="f7085-185">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="f7085-186">`[SkuName <String>]`: название SKU.</span><span class="sxs-lookup"><span data-stu-id="f7085-186">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="f7085-187">ПРИМЕЧАНИЕ. Если новый SKU не поддерживается на оборудовании, наемное облачным сервисом, необходимо удалить и воссоздать облачную службу или вернуться к старым SKU.</span><span class="sxs-lookup"><span data-stu-id="f7085-187">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="f7085-188">`[SkuTier <String>]`: уровень облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-188">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="f7085-189">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="f7085-189">Possible Values are</span></span> <br /><br /> <span data-ttu-id="f7085-190">**Стандартный**</span><span class="sxs-lookup"><span data-stu-id="f7085-190">**Standard**</span></span> <br /><br /> <span data-ttu-id="f7085-191">**Базовая**</span><span class="sxs-lookup"><span data-stu-id="f7085-191">**Basic**</span></span>
  - <span data-ttu-id="f7085-192">`[StartCloudService <Boolean?>]`: (Необязательно) Указывает, следует ли запускать облачную службу сразу после ее создания.</span><span class="sxs-lookup"><span data-stu-id="f7085-192">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="f7085-193">Значение по `true` умолчанию: .</span><span class="sxs-lookup"><span data-stu-id="f7085-193">The default value is `true`.</span></span>         <span data-ttu-id="f7085-194">Если этот код ложный, модель обслуживания по-прежнему развертывается, но не сразу же запустится.</span><span class="sxs-lookup"><span data-stu-id="f7085-194">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="f7085-195">Вместо этого служба будет иметь poweredOff, пока вы не позвоните в службу "Начните", и она будет запущена.</span><span class="sxs-lookup"><span data-stu-id="f7085-195">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="f7085-196">С развернутой службы по-прежнему взимается плата, даже если она отключена.</span><span class="sxs-lookup"><span data-stu-id="f7085-196">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="f7085-197">`[Tag <ICloudServiceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7085-197">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="f7085-198">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="f7085-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f7085-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`Режим обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f7085-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="f7085-200">При развертывании службы для обновления доменов выделяются экземпляры ролей.</span><span class="sxs-lookup"><span data-stu-id="f7085-200">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="f7085-201">Обновления можно за инициативой обновления вручную в каждом домене обновления или автоматически во всех доменах обновления.</span><span class="sxs-lookup"><span data-stu-id="f7085-201">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="f7085-202">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="f7085-202">Possible Values are</span></span> <br /><br /><span data-ttu-id="f7085-203">**Авто**</span><span class="sxs-lookup"><span data-stu-id="f7085-203">**Auto**</span></span><br /><br /><span data-ttu-id="f7085-204">**Вручную**</span><span class="sxs-lookup"><span data-stu-id="f7085-204">**Manual**</span></span> <br /><br /><span data-ttu-id="f7085-205">**Одновременный**</span><span class="sxs-lookup"><span data-stu-id="f7085-205">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="f7085-206">Если не указано, по умолчанию задано значение "Авто". Чтобы применить обновление вручную, необходимо создать put UpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="f7085-206">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="f7085-207">Если за установлено автоматическое обновление, обновление автоматически применяется к каждому домену обновления последовательно.</span><span class="sxs-lookup"><span data-stu-id="f7085-207">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="f7085-208">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7085-208">RELATED LINKS</span></span>

