---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: d5b8d521c72b553143f75b0911cb9b933b0795e7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245240"
---
# <span data-ttu-id="8b87d-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="8b87d-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="8b87d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b87d-102">SYNOPSIS</span></span>
<span data-ttu-id="8b87d-103">Создайте новую службу или обновите службу выхода.</span><span class="sxs-lookup"><span data-stu-id="8b87d-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="8b87d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b87d-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b87d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b87d-105">DESCRIPTION</span></span>
<span data-ttu-id="8b87d-106">Создайте новую службу или обновите службу выхода.</span><span class="sxs-lookup"><span data-stu-id="8b87d-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="8b87d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b87d-107">EXAMPLES</span></span>

### <span data-ttu-id="8b87d-108">Пример 1: создание пружинной облачной службы.</span><span class="sxs-lookup"><span data-stu-id="8b87d-108">Example 1: Create a spring cloud service.</span></span>
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

<span data-ttu-id="8b87d-109">Создание весны облачной службы.</span><span class="sxs-lookup"><span data-stu-id="8b87d-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="8b87d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b87d-110">PARAMETERS</span></span>

### <span data-ttu-id="8b87d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b87d-111">-AsJob</span></span>
<span data-ttu-id="8b87d-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="8b87d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8b87d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b87d-113">-DefaultProfile</span></span>
<span data-ttu-id="8b87d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b87d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b87d-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="8b87d-115">-GitPropertyUri</span></span>
<span data-ttu-id="8b87d-116">URI репозитория</span><span class="sxs-lookup"><span data-stu-id="8b87d-116">URI of the repository</span></span>

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

### <span data-ttu-id="8b87d-117">-Location</span><span class="sxs-lookup"><span data-stu-id="8b87d-117">-Location</span></span>
<span data-ttu-id="8b87d-118">Географическое расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b87d-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="8b87d-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b87d-119">-Name</span></span>
<span data-ttu-id="8b87d-120">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="8b87d-120">The name of the Service resource.</span></span>

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

### <span data-ttu-id="8b87d-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="8b87d-121">-NoWait</span></span>
<span data-ttu-id="8b87d-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="8b87d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8b87d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b87d-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b87d-124">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="8b87d-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8b87d-125">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="8b87d-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8b87d-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8b87d-126">-SkuName</span></span>
<span data-ttu-id="8b87d-127">Название SKU</span><span class="sxs-lookup"><span data-stu-id="8b87d-127">Name of the Sku</span></span>

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

### <span data-ttu-id="8b87d-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8b87d-128">-SkuTier</span></span>
<span data-ttu-id="8b87d-129">Уровень SKU</span><span class="sxs-lookup"><span data-stu-id="8b87d-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="8b87d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b87d-130">-SubscriptionId</span></span>
<span data-ttu-id="8b87d-131">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8b87d-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8b87d-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8b87d-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8b87d-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="8b87d-133">-Tag</span></span>
<span data-ttu-id="8b87d-134">Теги службы, представляющие собой список пар "ключ-значение", описывающих ресурс.</span><span class="sxs-lookup"><span data-stu-id="8b87d-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="8b87d-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="8b87d-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="8b87d-136">Ключ инструментария Application Insights для конечного приложения</span><span class="sxs-lookup"><span data-stu-id="8b87d-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="8b87d-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="8b87d-137">-TraceEnabled</span></span>
<span data-ttu-id="8b87d-138">Указывает, включена ли функция трассировки</span><span class="sxs-lookup"><span data-stu-id="8b87d-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="8b87d-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b87d-139">-Confirm</span></span>
<span data-ttu-id="8b87d-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b87d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b87d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b87d-141">-WhatIf</span></span>
<span data-ttu-id="8b87d-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b87d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b87d-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b87d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b87d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b87d-144">CommonParameters</span></span>
<span data-ttu-id="8b87d-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b87d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b87d-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b87d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b87d-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b87d-147">INPUTS</span></span>

## <span data-ttu-id="8b87d-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b87d-148">OUTPUTS</span></span>

### <span data-ttu-id="8b87d-149">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="8b87d-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="8b87d-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b87d-150">NOTES</span></span>

<span data-ttu-id="8b87d-151">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="8b87d-151">ALIASES</span></span>

## <span data-ttu-id="8b87d-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b87d-152">RELATED LINKS</span></span>

