---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: d5b8d521c72b553143f75b0911cb9b933b0795e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217473"
---
# <span data-ttu-id="649fb-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="649fb-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="649fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="649fb-102">SYNOPSIS</span></span>
<span data-ttu-id="649fb-103">Создать новую службу или обновить службу выхода.</span><span class="sxs-lookup"><span data-stu-id="649fb-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="649fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="649fb-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="649fb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="649fb-105">DESCRIPTION</span></span>
<span data-ttu-id="649fb-106">Создание службы или обновление службы, выйдите из системы.</span><span class="sxs-lookup"><span data-stu-id="649fb-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="649fb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="649fb-107">EXAMPLES</span></span>

### <span data-ttu-id="649fb-108">Пример 1. Создание весенних облачных служб.</span><span class="sxs-lookup"><span data-stu-id="649fb-108">Example 1: Create a spring cloud service.</span></span>
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

<span data-ttu-id="649fb-109">Создайте весенние облачные службы.</span><span class="sxs-lookup"><span data-stu-id="649fb-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="649fb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="649fb-110">PARAMETERS</span></span>

### <span data-ttu-id="649fb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="649fb-111">-AsJob</span></span>
<span data-ttu-id="649fb-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="649fb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="649fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="649fb-113">-DefaultProfile</span></span>
<span data-ttu-id="649fb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="649fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="649fb-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="649fb-115">-GitPropertyUri</span></span>
<span data-ttu-id="649fb-116">URI репозитория</span><span class="sxs-lookup"><span data-stu-id="649fb-116">URI of the repository</span></span>

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

### <span data-ttu-id="649fb-117">-Location</span><span class="sxs-lookup"><span data-stu-id="649fb-117">-Location</span></span>
<span data-ttu-id="649fb-118">Геосхема ресурса.</span><span class="sxs-lookup"><span data-stu-id="649fb-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="649fb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="649fb-119">-Name</span></span>
<span data-ttu-id="649fb-120">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="649fb-120">The name of the Service resource.</span></span>

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

### <span data-ttu-id="649fb-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="649fb-121">-NoWait</span></span>
<span data-ttu-id="649fb-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="649fb-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="649fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="649fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="649fb-124">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="649fb-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="649fb-125">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="649fb-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="649fb-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="649fb-126">-SkuName</span></span>
<span data-ttu-id="649fb-127">Название SKU</span><span class="sxs-lookup"><span data-stu-id="649fb-127">Name of the Sku</span></span>

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

### <span data-ttu-id="649fb-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="649fb-128">-SkuTier</span></span>
<span data-ttu-id="649fb-129">Уровень SKU</span><span class="sxs-lookup"><span data-stu-id="649fb-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="649fb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="649fb-130">-SubscriptionId</span></span>
<span data-ttu-id="649fb-131">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="649fb-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="649fb-132">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="649fb-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="649fb-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="649fb-133">-Tag</span></span>
<span data-ttu-id="649fb-134">Теги службы, которые являются списком пар ключевых значений, которые описывают ресурс.</span><span class="sxs-lookup"><span data-stu-id="649fb-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="649fb-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="649fb-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="649fb-136">Ключ анализа целевого приложения</span><span class="sxs-lookup"><span data-stu-id="649fb-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="649fb-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="649fb-137">-TraceEnabled</span></span>
<span data-ttu-id="649fb-138">Указывает, можно ли включить функцию трассии</span><span class="sxs-lookup"><span data-stu-id="649fb-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="649fb-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="649fb-139">-Confirm</span></span>
<span data-ttu-id="649fb-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="649fb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="649fb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="649fb-141">-WhatIf</span></span>
<span data-ttu-id="649fb-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="649fb-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="649fb-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="649fb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="649fb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="649fb-144">CommonParameters</span></span>
<span data-ttu-id="649fb-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="649fb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="649fb-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="649fb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="649fb-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="649fb-147">INPUTS</span></span>

## <span data-ttu-id="649fb-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="649fb-148">OUTPUTS</span></span>

### <span data-ttu-id="649fb-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="649fb-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="649fb-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="649fb-150">NOTES</span></span>

<span data-ttu-id="649fb-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="649fb-151">ALIASES</span></span>

## <span data-ttu-id="649fb-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="649fb-152">RELATED LINKS</span></span>

