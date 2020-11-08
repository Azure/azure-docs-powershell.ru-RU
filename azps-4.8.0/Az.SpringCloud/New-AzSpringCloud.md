---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: c84037fd402e5ecea51cc4f60dcddb1873878f5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243941"
---
# <span data-ttu-id="fbb79-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="fbb79-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="fbb79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbb79-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb79-103">Создайте новую службу или обновите службу выхода.</span><span class="sxs-lookup"><span data-stu-id="fbb79-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="fbb79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbb79-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fbb79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbb79-105">DESCRIPTION</span></span>
<span data-ttu-id="fbb79-106">Создайте новую службу или обновите службу выхода.</span><span class="sxs-lookup"><span data-stu-id="fbb79-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="fbb79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbb79-107">EXAMPLES</span></span>

### <span data-ttu-id="fbb79-108">Пример 1: создание пружинной облачной службы.</span><span class="sxs-lookup"><span data-stu-id="fbb79-108">Example 1: Create a spring cloud service.</span></span>
```powershell
PS C:\> New-AzSpringCloud -ResourceGroupName spring-cloud-rp -name spring-cloud-service -Location eastus

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

<span data-ttu-id="fbb79-109">Создание весны облачной службы.</span><span class="sxs-lookup"><span data-stu-id="fbb79-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="fbb79-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbb79-110">PARAMETERS</span></span>

### <span data-ttu-id="fbb79-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbb79-111">-AsJob</span></span>
<span data-ttu-id="fbb79-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="fbb79-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fbb79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb79-113">-DefaultProfile</span></span>
<span data-ttu-id="fbb79-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb79-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="fbb79-115">-GitPropertyUri</span></span>
<span data-ttu-id="fbb79-116">URI репозитория</span><span class="sxs-lookup"><span data-stu-id="fbb79-116">URI of the repository</span></span>

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

### <span data-ttu-id="fbb79-117">-Location</span><span class="sxs-lookup"><span data-stu-id="fbb79-117">-Location</span></span>
<span data-ttu-id="fbb79-118">Географическое расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="fbb79-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="fbb79-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fbb79-119">-Name</span></span>
<span data-ttu-id="fbb79-120">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="fbb79-120">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb79-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="fbb79-121">-NoWait</span></span>
<span data-ttu-id="fbb79-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="fbb79-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fbb79-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb79-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbb79-124">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="fbb79-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fbb79-125">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="fbb79-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fbb79-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fbb79-126">-SkuName</span></span>
<span data-ttu-id="fbb79-127">Название SKU</span><span class="sxs-lookup"><span data-stu-id="fbb79-127">Name of the Sku</span></span>

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

### <span data-ttu-id="fbb79-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fbb79-128">-SkuTier</span></span>
<span data-ttu-id="fbb79-129">Уровень SKU</span><span class="sxs-lookup"><span data-stu-id="fbb79-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="fbb79-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fbb79-130">-SubscriptionId</span></span>
<span data-ttu-id="fbb79-131">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb79-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fbb79-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="fbb79-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fbb79-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="fbb79-133">-Tag</span></span>
<span data-ttu-id="fbb79-134">Теги службы, представляющие собой список пар "ключ-значение", описывающих ресурс.</span><span class="sxs-lookup"><span data-stu-id="fbb79-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="fbb79-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="fbb79-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="fbb79-136">Ключ инструментария Application Insights для конечного приложения</span><span class="sxs-lookup"><span data-stu-id="fbb79-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="fbb79-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="fbb79-137">-TraceEnabled</span></span>
<span data-ttu-id="fbb79-138">Указывает, включена ли функция трассировки</span><span class="sxs-lookup"><span data-stu-id="fbb79-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="fbb79-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbb79-139">-Confirm</span></span>
<span data-ttu-id="fbb79-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbb79-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb79-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb79-141">-WhatIf</span></span>
<span data-ttu-id="fbb79-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbb79-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb79-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbb79-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb79-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb79-144">CommonParameters</span></span>
<span data-ttu-id="fbb79-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbb79-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb79-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbb79-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb79-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbb79-147">INPUTS</span></span>

## <span data-ttu-id="fbb79-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbb79-148">OUTPUTS</span></span>

### <span data-ttu-id="fbb79-149">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20190501Preview. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="fbb79-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IServiceResource</span></span>

## <span data-ttu-id="fbb79-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbb79-150">NOTES</span></span>

<span data-ttu-id="fbb79-151">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="fbb79-151">ALIASES</span></span>

## <span data-ttu-id="fbb79-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbb79-152">RELATED LINKS</span></span>

