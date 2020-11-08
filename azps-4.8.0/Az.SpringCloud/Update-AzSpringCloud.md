---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 02a880d669e3e93693dc39823587fe1d676ac279
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078720"
---
# <span data-ttu-id="fbafc-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="fbafc-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="fbafc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbafc-102">SYNOPSIS</span></span>
<span data-ttu-id="fbafc-103">Операция обновления завершающей службы.</span><span class="sxs-lookup"><span data-stu-id="fbafc-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="fbafc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbafc-104">SYNTAX</span></span>

### <span data-ttu-id="fbafc-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fbafc-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fbafc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fbafc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fbafc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbafc-107">DESCRIPTION</span></span>
<span data-ttu-id="fbafc-108">Операция обновления завершающей службы.</span><span class="sxs-lookup"><span data-stu-id="fbafc-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="fbafc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbafc-109">EXAMPLES</span></span>

### <span data-ttu-id="fbafc-110">Пример 1: обновление пружинной облачной службы по названию.</span><span class="sxs-lookup"><span data-stu-id="fbafc-110">Example 1: Update Spring Cloud Service by name.</span></span>
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

<span data-ttu-id="fbafc-111">Обновите облачную службу весны по названию.</span><span class="sxs-lookup"><span data-stu-id="fbafc-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="fbafc-112">Пример 2: обновление пружинной облачной службы из канала.</span><span class="sxs-lookup"><span data-stu-id="fbafc-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
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

<span data-ttu-id="fbafc-113">Обновите облачную службу весны из канала.</span><span class="sxs-lookup"><span data-stu-id="fbafc-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="fbafc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbafc-114">PARAMETERS</span></span>

### <span data-ttu-id="fbafc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbafc-115">-AsJob</span></span>
<span data-ttu-id="fbafc-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="fbafc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fbafc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbafc-117">-DefaultProfile</span></span>
<span data-ttu-id="fbafc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbafc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbafc-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="fbafc-119">-GitPropertyUri</span></span>
<span data-ttu-id="fbafc-120">URI репозитория</span><span class="sxs-lookup"><span data-stu-id="fbafc-120">URI of the repository</span></span>

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

### <span data-ttu-id="fbafc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbafc-121">-InputObject</span></span>
<span data-ttu-id="fbafc-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="fbafc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fbafc-123">-Location</span><span class="sxs-lookup"><span data-stu-id="fbafc-123">-Location</span></span>
<span data-ttu-id="fbafc-124">Географическое расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="fbafc-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="fbafc-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fbafc-125">-Name</span></span>
<span data-ttu-id="fbafc-126">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="fbafc-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="fbafc-127">-Wait</span><span class="sxs-lookup"><span data-stu-id="fbafc-127">-NoWait</span></span>
<span data-ttu-id="fbafc-128">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="fbafc-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fbafc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbafc-129">-ResourceGroupName</span></span>
<span data-ttu-id="fbafc-130">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="fbafc-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fbafc-131">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="fbafc-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fbafc-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fbafc-132">-SkuName</span></span>
<span data-ttu-id="fbafc-133">Название SKU</span><span class="sxs-lookup"><span data-stu-id="fbafc-133">Name of the Sku</span></span>

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

### <span data-ttu-id="fbafc-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fbafc-134">-SkuTier</span></span>
<span data-ttu-id="fbafc-135">Уровень SKU</span><span class="sxs-lookup"><span data-stu-id="fbafc-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="fbafc-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fbafc-136">-SubscriptionId</span></span>
<span data-ttu-id="fbafc-137">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fbafc-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fbafc-138">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="fbafc-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fbafc-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="fbafc-139">-Tag</span></span>
<span data-ttu-id="fbafc-140">Теги службы, представляющие собой список пар "ключ-значение", описывающих ресурс.</span><span class="sxs-lookup"><span data-stu-id="fbafc-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="fbafc-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="fbafc-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="fbafc-142">Ключ инструментария Application Insights для конечного приложения</span><span class="sxs-lookup"><span data-stu-id="fbafc-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="fbafc-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="fbafc-143">-TraceEnabled</span></span>
<span data-ttu-id="fbafc-144">Указывает, включена ли функция трассировки</span><span class="sxs-lookup"><span data-stu-id="fbafc-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="fbafc-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbafc-145">-Confirm</span></span>
<span data-ttu-id="fbafc-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbafc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbafc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbafc-147">-WhatIf</span></span>
<span data-ttu-id="fbafc-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbafc-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbafc-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbafc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbafc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbafc-150">CommonParameters</span></span>
<span data-ttu-id="fbafc-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbafc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbafc-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbafc-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbafc-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbafc-153">INPUTS</span></span>

### <span data-ttu-id="fbafc-154">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="fbafc-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="fbafc-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbafc-155">OUTPUTS</span></span>

### <span data-ttu-id="fbafc-156">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20190501Preview. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="fbafc-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IServiceResource</span></span>

## <span data-ttu-id="fbafc-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbafc-157">NOTES</span></span>

<span data-ttu-id="fbafc-158">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="fbafc-158">ALIASES</span></span>

<span data-ttu-id="fbafc-159">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fbafc-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fbafc-160">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fbafc-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fbafc-161">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fbafc-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fbafc-162">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="fbafc-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fbafc-163">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="fbafc-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="fbafc-164">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="fbafc-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="fbafc-165">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="fbafc-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="fbafc-166">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="fbafc-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="fbafc-167">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="fbafc-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="fbafc-168">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="fbafc-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fbafc-169">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="fbafc-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="fbafc-170">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="fbafc-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="fbafc-171">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="fbafc-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="fbafc-172">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="fbafc-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="fbafc-173">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fbafc-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="fbafc-174">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="fbafc-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fbafc-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbafc-175">RELATED LINKS</span></span>

