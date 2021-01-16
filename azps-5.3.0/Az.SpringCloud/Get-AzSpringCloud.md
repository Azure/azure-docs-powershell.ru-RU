---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506680"
---
# <span data-ttu-id="aae50-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="aae50-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="aae50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aae50-102">SYNOPSIS</span></span>
<span data-ttu-id="aae50-103">Получите службу и ее свойства.</span><span class="sxs-lookup"><span data-stu-id="aae50-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="aae50-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aae50-104">SYNTAX</span></span>

### <span data-ttu-id="aae50-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aae50-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aae50-106">Получить</span><span class="sxs-lookup"><span data-stu-id="aae50-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aae50-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aae50-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aae50-108">List1</span><span class="sxs-lookup"><span data-stu-id="aae50-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="aae50-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aae50-109">DESCRIPTION</span></span>
<span data-ttu-id="aae50-110">Получите службу и ее свойства.</span><span class="sxs-lookup"><span data-stu-id="aae50-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="aae50-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aae50-111">EXAMPLES</span></span>

### <span data-ttu-id="aae50-112">Пример 1. Получить службу "Весенние облачные службы" по имени</span><span class="sxs-lookup"><span data-stu-id="aae50-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
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

<span data-ttu-id="aae50-113">Получить службу "Весенние облачные службы" по имени</span><span class="sxs-lookup"><span data-stu-id="aae50-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="aae50-114">Пример 2. Перечислить все весенние облачные службы в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aae50-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="aae50-115">Перечислить все весенние облачные службы в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aae50-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="aae50-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aae50-116">PARAMETERS</span></span>

### <span data-ttu-id="aae50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae50-117">-DefaultProfile</span></span>
<span data-ttu-id="aae50-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aae50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aae50-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aae50-119">-InputObject</span></span>
<span data-ttu-id="aae50-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="aae50-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aae50-121">-Name</span><span class="sxs-lookup"><span data-stu-id="aae50-121">-Name</span></span>
<span data-ttu-id="aae50-122">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="aae50-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae50-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aae50-123">-ResourceGroupName</span></span>
<span data-ttu-id="aae50-124">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="aae50-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="aae50-125">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="aae50-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae50-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aae50-126">-SubscriptionId</span></span>
<span data-ttu-id="aae50-127">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aae50-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="aae50-128">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="aae50-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae50-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae50-129">CommonParameters</span></span>
<span data-ttu-id="aae50-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae50-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae50-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aae50-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae50-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aae50-132">INPUTS</span></span>

### <span data-ttu-id="aae50-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="aae50-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="aae50-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aae50-134">OUTPUTS</span></span>

### <span data-ttu-id="aae50-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="aae50-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="aae50-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aae50-136">NOTES</span></span>

<span data-ttu-id="aae50-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="aae50-137">ALIASES</span></span>

<span data-ttu-id="aae50-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="aae50-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aae50-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="aae50-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aae50-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aae50-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aae50-141">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="aae50-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aae50-142">`[AppName <String>]`: название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="aae50-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="aae50-143">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="aae50-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="aae50-144">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="aae50-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="aae50-145">`[DeploymentName <String>]`: название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="aae50-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="aae50-146">`[DomainName <String>]`: имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="aae50-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="aae50-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="aae50-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aae50-148">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="aae50-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="aae50-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="aae50-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="aae50-150">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="aae50-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="aae50-151">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="aae50-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="aae50-152">`[SubscriptionId <String>]`. Получает ИД подписки, однозначно определяя подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aae50-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="aae50-153">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="aae50-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="aae50-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aae50-154">RELATED LINKS</span></span>

