---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245241"
---
# <span data-ttu-id="23b73-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="23b73-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="23b73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23b73-102">SYNOPSIS</span></span>
<span data-ttu-id="23b73-103">Получение службы и ее свойств.</span><span class="sxs-lookup"><span data-stu-id="23b73-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="23b73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23b73-104">SYNTAX</span></span>

### <span data-ttu-id="23b73-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23b73-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23b73-106">Получить</span><span class="sxs-lookup"><span data-stu-id="23b73-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23b73-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="23b73-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23b73-108">List1</span><span class="sxs-lookup"><span data-stu-id="23b73-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="23b73-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23b73-109">DESCRIPTION</span></span>
<span data-ttu-id="23b73-110">Получение службы и ее свойств.</span><span class="sxs-lookup"><span data-stu-id="23b73-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="23b73-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23b73-111">EXAMPLES</span></span>

### <span data-ttu-id="23b73-112">Пример 1: получение весны облачной службы по названию</span><span class="sxs-lookup"><span data-stu-id="23b73-112">Example 1: Get Spring Cloud Service by name</span></span>
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

<span data-ttu-id="23b73-113">Получить пружинную облачную службу по имени</span><span class="sxs-lookup"><span data-stu-id="23b73-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="23b73-114">Пример 2: список всех облачных служб весны в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23b73-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="23b73-115">Перечислите все облачные службы весны в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23b73-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="23b73-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23b73-116">PARAMETERS</span></span>

### <span data-ttu-id="23b73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b73-117">-DefaultProfile</span></span>
<span data-ttu-id="23b73-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23b73-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b73-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23b73-119">-InputObject</span></span>
<span data-ttu-id="23b73-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="23b73-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="23b73-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23b73-121">-Name</span></span>
<span data-ttu-id="23b73-122">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="23b73-122">The name of the Service resource.</span></span>

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

### <span data-ttu-id="23b73-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b73-123">-ResourceGroupName</span></span>
<span data-ttu-id="23b73-124">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="23b73-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="23b73-125">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="23b73-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="23b73-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23b73-126">-SubscriptionId</span></span>
<span data-ttu-id="23b73-127">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="23b73-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="23b73-128">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="23b73-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="23b73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b73-129">CommonParameters</span></span>
<span data-ttu-id="23b73-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23b73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b73-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23b73-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b73-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23b73-132">INPUTS</span></span>

### <span data-ttu-id="23b73-133">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="23b73-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="23b73-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23b73-134">OUTPUTS</span></span>

### <span data-ttu-id="23b73-135">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="23b73-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="23b73-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="23b73-136">NOTES</span></span>

<span data-ttu-id="23b73-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="23b73-137">ALIASES</span></span>

<span data-ttu-id="23b73-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="23b73-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23b73-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="23b73-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23b73-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23b73-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23b73-141">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="23b73-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23b73-142">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="23b73-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="23b73-143">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="23b73-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="23b73-144">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="23b73-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="23b73-145">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="23b73-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="23b73-146">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="23b73-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="23b73-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="23b73-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23b73-148">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="23b73-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="23b73-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="23b73-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="23b73-150">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="23b73-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="23b73-151">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="23b73-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="23b73-152">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="23b73-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="23b73-153">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="23b73-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="23b73-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23b73-154">RELATED LINKS</span></span>

