---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: b46ab9b8dee108f6d2126c199e5609d92452b95a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007208"
---
# <span data-ttu-id="f824d-101">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="f824d-101">Switch-AzCloudService</span></span>

## <span data-ttu-id="f824d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f824d-102">SYNOPSIS</span></span>
<span data-ttu-id="f824d-103">Обмен VIP-решениями между двумя балансирными балансами нагрузки облачной службы (расширенной поддержки).</span><span class="sxs-lookup"><span data-stu-id="f824d-103">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="f824d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f824d-104">SYNTAX</span></span>

### <span data-ttu-id="f824d-105">CloudServiceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f824d-105">CloudServiceName (Default)</span></span>
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f824d-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="f824d-106">CloudService</span></span>
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f824d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f824d-107">DESCRIPTION</span></span>
<span data-ttu-id="f824d-108">Обмен VIP-решениями между двумя балансирными балансами нагрузки облачной службы (расширенной поддержки).</span><span class="sxs-lookup"><span data-stu-id="f824d-108">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="f824d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f824d-109">EXAMPLES</span></span>

### <span data-ttu-id="f824d-110">Пример 1. Переключение облачной службы с использованием имени</span><span class="sxs-lookup"><span data-stu-id="f824d-110">Example 1: Switch cloud service using name</span></span>
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="f824d-111">Команда выше вызывает операцию VIPSWAP в облачной службе с именем "BService" и выполнит операцию, как только пользователь подтвердит действие в запросе на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f824d-111">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="f824d-112">"BService" с заменяемой облачной службой.</span><span class="sxs-lookup"><span data-stu-id="f824d-112">'BService' with be swapped with its swappable cloud service.</span></span>

### <span data-ttu-id="f824d-113">Пример 2. Переключение облачной службы с помощью объекта облачной службы</span><span class="sxs-lookup"><span data-stu-id="f824d-113">Example 2: Switch cloud service using cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

<span data-ttu-id="f824d-114">Команда выше вызывает операцию VIPSWAP в облачной службе с именем "BService" и выполнит операцию, как только пользователь подтвердит действие в запросе на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f824d-114">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="f824d-115">"BService" с заменяемой облачной службой.</span><span class="sxs-lookup"><span data-stu-id="f824d-115">'BService' with be swapped with its swappable cloud service.</span></span>

## <span data-ttu-id="f824d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f824d-116">PARAMETERS</span></span>

### <span data-ttu-id="f824d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f824d-117">-AsJob</span></span>
<span data-ttu-id="f824d-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f824d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="f824d-119">-Async</span><span class="sxs-lookup"><span data-stu-id="f824d-119">-Async</span></span>


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

### <span data-ttu-id="f824d-120">-CloudService</span><span class="sxs-lookup"><span data-stu-id="f824d-120">-CloudService</span></span>
<span data-ttu-id="f824d-121">Чтобы построить, см. раздел "ЗАМЕТКИ" для свойств CLOUDSERVICE и создание таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="f824d-121">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f824d-122">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="f824d-122">-CloudServiceName</span></span>


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

### <span data-ttu-id="f824d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f824d-123">-DefaultProfile</span></span>
<span data-ttu-id="f824d-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f824d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f824d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f824d-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="f824d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f824d-126">-SubscriptionId</span></span>
<span data-ttu-id="f824d-127">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f824d-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f824d-128">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="f824d-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f824d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f824d-129">-Confirm</span></span>
<span data-ttu-id="f824d-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f824d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f824d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f824d-131">-WhatIf</span></span>
<span data-ttu-id="f824d-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f824d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f824d-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f824d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f824d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f824d-134">CommonParameters</span></span>
<span data-ttu-id="f824d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f824d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f824d-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f824d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f824d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f824d-137">INPUTS</span></span>

## <span data-ttu-id="f824d-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f824d-138">OUTPUTS</span></span>

### <span data-ttu-id="f824d-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f824d-139">System.Boolean</span></span>

## <span data-ttu-id="f824d-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f824d-140">NOTES</span></span>

<span data-ttu-id="f824d-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f824d-141">ALIASES</span></span>

<span data-ttu-id="f824d-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f824d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f824d-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f824d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f824d-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f824d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f824d-145"><CloudService>CLOUDSERVICE:</span><span class="sxs-lookup"><span data-stu-id="f824d-145">CLOUDSERVICE <CloudService>:</span></span> 
  - <span data-ttu-id="f824d-146">`Location <String>`: расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="f824d-146">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="f824d-147">`[Configuration <String>]`Определяет конфигурацию службы XML (CSCFG) для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f824d-147">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="f824d-148">`[ConfigurationUrl <String>]`: указывает URL-адрес, который ссылается на расположение конфигурации службы в службе BLOB-бизнес.</span><span class="sxs-lookup"><span data-stu-id="f824d-148">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="f824d-149">URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f824d-149">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="f824d-150">Это свойство является свойством только для записи и не возвращается при звонках GET.</span><span class="sxs-lookup"><span data-stu-id="f824d-150">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="f824d-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Описание профиля расширения облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f824d-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="f824d-152">`[Extension <IExtension[]>]`: Список расширений для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f824d-152">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="f824d-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Укажите, может ли платформа автоматически обновлять TypeHandlerVersion до более высокого уровня, когда они становятся доступны.</span><span class="sxs-lookup"><span data-stu-id="f824d-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="f824d-154">`[ForceUpdateTag <String>]`Тег, чтобы принудительно применить предоставленные общедоступные и защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="f824d-154">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="f824d-155">Изменение значения тега позволяет повторно запускать расширение без изменения общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="f824d-155">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="f824d-156">Если параметр forceUpdateTag не изменился, обработник по-прежнему будет применять обновления общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="f824d-156">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="f824d-157">Если ни принудительное изменение параметра,ни каких-либо из общедоступных или защищенных параметров не изменилось, расширение будет перенаправляться в экземпляр роли с одинаковым номером последовательности и будет управлять внедрением, нужно ли повторно запускать его.</span><span class="sxs-lookup"><span data-stu-id="f824d-157">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="f824d-158">`[Name <String>]`: имя расширения.</span><span class="sxs-lookup"><span data-stu-id="f824d-158">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="f824d-159">`[ProtectedSetting <String>]`: Защищенные параметры расширения, которые шифруются перед его отправлением в экземпляр роли.</span><span class="sxs-lookup"><span data-stu-id="f824d-159">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="f824d-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f824d-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="f824d-161">`[Publisher <String>]`: имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="f824d-161">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="f824d-162">`[RolesAppliedTo <String[]>]`: Необязательный список ролей для применения этого расширения.</span><span class="sxs-lookup"><span data-stu-id="f824d-162">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="f824d-163">Если свойство не указано или указано "\*", расширение применяется для всех ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="f824d-163">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="f824d-164">`[Setting <String>]`: общедоступные параметры расширения.</span><span class="sxs-lookup"><span data-stu-id="f824d-164">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="f824d-165">Для расширений JSON это параметры JSON.</span><span class="sxs-lookup"><span data-stu-id="f824d-165">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="f824d-166">Для расширения XML (например, RDP) это параметр XML для расширения.</span><span class="sxs-lookup"><span data-stu-id="f824d-166">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="f824d-167">`[SourceVaultId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f824d-167">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="f824d-168">`[Type <String>]`: тип расширения.</span><span class="sxs-lookup"><span data-stu-id="f824d-168">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="f824d-169">`[TypeHandlerVersion <String>]`: определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="f824d-169">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="f824d-170">Определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="f824d-170">Specifies the version of the extension.</span></span> <span data-ttu-id="f824d-171">Если этот элемент не указан или в качестве значения используется звездочка (\*), используется последняя версия расширения.</span><span class="sxs-lookup"><span data-stu-id="f824d-171">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="f824d-172">Если задан номер основной версии и звездочка как дополнительный номер версии (X.), будет выбрана последняя дополнительный версия указанной основной версии.</span><span class="sxs-lookup"><span data-stu-id="f824d-172">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="f824d-173">Если указан основной номер версии и небольшой номер версии (X.Y), будет выбрана конкретная версия расширения.</span><span class="sxs-lookup"><span data-stu-id="f824d-173">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="f824d-174">Если указана версия, для экземпляра роли выполняется автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="f824d-174">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="f824d-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Профиль сети для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f824d-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="f824d-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`Список конфигураций балансиров нагрузки для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f824d-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="f824d-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Список IP-адресов</span><span class="sxs-lookup"><span data-stu-id="f824d-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="f824d-178">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f824d-178">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="f824d-179">`[PrivateIPAddress <String>]`: личный IP-адрес, на который ссылается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="f824d-179">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="f824d-180">`[PublicIPAddressId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f824d-180">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="f824d-181">`[SubnetId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f824d-181">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="f824d-182">`[Name <String>]`: Название ресурса</span><span class="sxs-lookup"><span data-stu-id="f824d-182">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="f824d-183">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="f824d-183">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="f824d-184">`[Id <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f824d-184">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="f824d-185">`[OSProfile <ICloudServiceOSProfile>]`: Описание профиля ОС для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f824d-185">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="f824d-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Набор сертификатов, которые нужно установить на экземпляры ролей.</span><span class="sxs-lookup"><span data-stu-id="f824d-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="f824d-187">`[SourceVaultId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f824d-187">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="f824d-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: список ссылок на основные хранилища в SourceVault, которые содержат сертификаты.</span><span class="sxs-lookup"><span data-stu-id="f824d-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="f824d-189">`[CertificateUrl <String>]`. Это URL-адрес сертификата, который был выложен в хранилище ключей в качестве секретного.</span><span class="sxs-lookup"><span data-stu-id="f824d-189">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="f824d-190">`[PackageUrl <String>]`: указывает URL-адрес, который ссылается на расположение пакета обслуживания в службе BLOB-бизнес.</span><span class="sxs-lookup"><span data-stu-id="f824d-190">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="f824d-191">URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f824d-191">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="f824d-192">Это свойство является свойством только для записи и не возвращается при звонках GET.</span><span class="sxs-lookup"><span data-stu-id="f824d-192">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="f824d-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Описание профиля роли для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f824d-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="f824d-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: Список ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="f824d-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="f824d-195">`[Name <String>]`: название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f824d-195">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="f824d-196">`[SkuCapacity <Int64?>]`Определяет количество экземпляров ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="f824d-196">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="f824d-197">`[SkuName <String>]`: название SKU.</span><span class="sxs-lookup"><span data-stu-id="f824d-197">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="f824d-198">ПРИМЕЧАНИЕ. Если новый SKU не поддерживается на оборудовании, наномном оборудовании сейчас работает облачная служба, необходимо удалить и воссоздать облачную службу или вернуться к старым SKU.</span><span class="sxs-lookup"><span data-stu-id="f824d-198">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="f824d-199">`[SkuTier <String>]`: определяет уровень облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f824d-199">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="f824d-200">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="f824d-200">Possible Values are</span></span> <br /><br /> <span data-ttu-id="f824d-201">**Стандартный**</span><span class="sxs-lookup"><span data-stu-id="f824d-201">**Standard**</span></span> <br /><br /> <span data-ttu-id="f824d-202">**Базовая**</span><span class="sxs-lookup"><span data-stu-id="f824d-202">**Basic**</span></span>
  - <span data-ttu-id="f824d-203">`[StartCloudService <Boolean?>]`: (Необязательно) Указывает, следует ли запускать облачную службу сразу после ее создания.</span><span class="sxs-lookup"><span data-stu-id="f824d-203">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="f824d-204">Значение по `true` умолчанию: .</span><span class="sxs-lookup"><span data-stu-id="f824d-204">The default value is `true`.</span></span>         <span data-ttu-id="f824d-205">Если этот код ложный, модель обслуживания по-прежнему развертывается, но не сразу же запустится.</span><span class="sxs-lookup"><span data-stu-id="f824d-205">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="f824d-206">Вместо этого служба будет иметь poweredOff, пока вы не позвоните в службу "Начните", и она будет запущена.</span><span class="sxs-lookup"><span data-stu-id="f824d-206">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="f824d-207">С развернутой службы по-прежнему взимается плата, даже если она отключена.</span><span class="sxs-lookup"><span data-stu-id="f824d-207">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="f824d-208">`[Tag <ICloudServiceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f824d-208">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="f824d-209">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="f824d-209">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f824d-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`Режим обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="f824d-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="f824d-211">При развертывании службы для обновления доменов выделяются экземпляры ролей.</span><span class="sxs-lookup"><span data-stu-id="f824d-211">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="f824d-212">Обновления можно за инициативой обновления вручную в каждом домене обновления или автоматически во всех доменах обновления.</span><span class="sxs-lookup"><span data-stu-id="f824d-212">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="f824d-213">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="f824d-213">Possible Values are</span></span> <br /><br /><span data-ttu-id="f824d-214">**Авто**</span><span class="sxs-lookup"><span data-stu-id="f824d-214">**Auto**</span></span><br /><br /><span data-ttu-id="f824d-215">**Вручную**</span><span class="sxs-lookup"><span data-stu-id="f824d-215">**Manual**</span></span> <br /><br /><span data-ttu-id="f824d-216">**Одновременный**</span><span class="sxs-lookup"><span data-stu-id="f824d-216">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="f824d-217">Если не указано, по умолчанию задано значение "Авто". Чтобы применить обновление вручную, необходимо создать put UpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="f824d-217">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="f824d-218">Если за установлено автоматическое обновление, обновление автоматически применяется к каждому домену обновления последовательно.</span><span class="sxs-lookup"><span data-stu-id="f824d-218">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="f824d-219">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f824d-219">RELATED LINKS</span></span>

