---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 361ba47486d7cc506e918ea279129110306e415f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392772"
---
# <span data-ttu-id="dca7b-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="dca7b-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="dca7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca7b-102">SYNOPSIS</span></span>
<span data-ttu-id="dca7b-103">Операция обновления службы выхода.</span><span class="sxs-lookup"><span data-stu-id="dca7b-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="dca7b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dca7b-104">SYNTAX</span></span>

### <span data-ttu-id="dca7b-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dca7b-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dca7b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dca7b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dca7b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dca7b-107">DESCRIPTION</span></span>
<span data-ttu-id="dca7b-108">Операция обновления службы выхода.</span><span class="sxs-lookup"><span data-stu-id="dca7b-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="dca7b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dca7b-109">EXAMPLES</span></span>

### <span data-ttu-id="dca7b-110">Пример 1. Обновление службы "Весенние облачные службы" по имени.</span><span class="sxs-lookup"><span data-stu-id="dca7b-110">Example 1: Update Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="dca7b-111">Обновление названия службы "Весенние облачные службы".</span><span class="sxs-lookup"><span data-stu-id="dca7b-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="dca7b-112">Пример 2. Обновление службы "Весенние облака" из трубы.</span><span class="sxs-lookup"><span data-stu-id="dca7b-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Update-AzSpringCloud
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="dca7b-113">Обновим весенние облачные службы по трубе.</span><span class="sxs-lookup"><span data-stu-id="dca7b-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="dca7b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dca7b-114">PARAMETERS</span></span>

### <span data-ttu-id="dca7b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dca7b-115">-AsJob</span></span>
<span data-ttu-id="dca7b-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="dca7b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="dca7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca7b-117">-DefaultProfile</span></span>
<span data-ttu-id="dca7b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dca7b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dca7b-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="dca7b-119">-GitPropertyUri</span></span>
<span data-ttu-id="dca7b-120">URI репозитория</span><span class="sxs-lookup"><span data-stu-id="dca7b-120">URI of the repository</span></span>

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

### <span data-ttu-id="dca7b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dca7b-121">-InputObject</span></span>
<span data-ttu-id="dca7b-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="dca7b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dca7b-123">-Location</span><span class="sxs-lookup"><span data-stu-id="dca7b-123">-Location</span></span>
<span data-ttu-id="dca7b-124">Геосхема ресурса.</span><span class="sxs-lookup"><span data-stu-id="dca7b-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="dca7b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dca7b-125">-Name</span></span>
<span data-ttu-id="dca7b-126">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="dca7b-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca7b-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dca7b-127">-NoWait</span></span>
<span data-ttu-id="dca7b-128">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="dca7b-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dca7b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca7b-129">-ResourceGroupName</span></span>
<span data-ttu-id="dca7b-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="dca7b-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dca7b-131">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="dca7b-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca7b-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dca7b-132">-SkuName</span></span>
<span data-ttu-id="dca7b-133">Имя SKU</span><span class="sxs-lookup"><span data-stu-id="dca7b-133">Name of the Sku</span></span>

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

### <span data-ttu-id="dca7b-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="dca7b-134">-SkuTier</span></span>
<span data-ttu-id="dca7b-135">Уровень SKU</span><span class="sxs-lookup"><span data-stu-id="dca7b-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="dca7b-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dca7b-136">-SubscriptionId</span></span>
<span data-ttu-id="dca7b-137">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dca7b-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dca7b-138">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="dca7b-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca7b-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="dca7b-139">-Tag</span></span>
<span data-ttu-id="dca7b-140">Теги службы, которые являются списком пар ключевых значений, которые описывают ресурс.</span><span class="sxs-lookup"><span data-stu-id="dca7b-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="dca7b-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="dca7b-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="dca7b-142">Ключ анализа целевого приложения</span><span class="sxs-lookup"><span data-stu-id="dca7b-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="dca7b-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="dca7b-143">-TraceEnabled</span></span>
<span data-ttu-id="dca7b-144">Указывает, можно ли включить функцию трассии</span><span class="sxs-lookup"><span data-stu-id="dca7b-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="dca7b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dca7b-145">-Confirm</span></span>
<span data-ttu-id="dca7b-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dca7b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca7b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca7b-147">-WhatIf</span></span>
<span data-ttu-id="dca7b-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dca7b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca7b-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dca7b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca7b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca7b-150">CommonParameters</span></span>
<span data-ttu-id="dca7b-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dca7b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca7b-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dca7b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca7b-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dca7b-153">INPUTS</span></span>

### <span data-ttu-id="dca7b-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="dca7b-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="dca7b-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dca7b-155">OUTPUTS</span></span>

### <span data-ttu-id="dca7b-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="dca7b-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="dca7b-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dca7b-157">NOTES</span></span>

<span data-ttu-id="dca7b-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dca7b-158">ALIASES</span></span>

<span data-ttu-id="dca7b-159">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="dca7b-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dca7b-160">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="dca7b-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dca7b-161">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dca7b-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dca7b-162">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="dca7b-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dca7b-163">`[AppName <String>]`: название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="dca7b-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="dca7b-164">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="dca7b-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="dca7b-165">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="dca7b-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="dca7b-166">`[DeploymentName <String>]`: название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="dca7b-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="dca7b-167">`[DomainName <String>]`: имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="dca7b-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="dca7b-168">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="dca7b-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dca7b-169">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="dca7b-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="dca7b-170">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="dca7b-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="dca7b-171">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="dca7b-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="dca7b-172">`[ServiceName <String>]`: Название ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="dca7b-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="dca7b-173">`[SubscriptionId <String>]`: получает ИД подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dca7b-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="dca7b-174">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="dca7b-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dca7b-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dca7b-175">RELATED LINKS</span></span>

