---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246922"
---
# <span data-ttu-id="23816-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="23816-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="23816-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23816-102">SYNOPSIS</span></span>
<span data-ttu-id="23816-103">Создание нового ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="23816-103">Create a new application insights resource</span></span>

## <span data-ttu-id="23816-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23816-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23816-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23816-105">DESCRIPTION</span></span>
<span data-ttu-id="23816-106">Создание нового ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="23816-106">Create a new application insights resource</span></span>

## <span data-ttu-id="23816-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23816-107">EXAMPLES</span></span>

### <span data-ttu-id="23816-108">Пример 1. Создание нового ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="23816-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="23816-109">Добавление нового ресурса Application Insights с именем "тест" в группе ресурсов "testgroup" с обозначением "Java"</span><span class="sxs-lookup"><span data-stu-id="23816-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="23816-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23816-110">PARAMETERS</span></span>

### <span data-ttu-id="23816-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23816-111">-DefaultProfile</span></span>
<span data-ttu-id="23816-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23816-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23816-113">-Видах</span><span class="sxs-lookup"><span data-stu-id="23816-113">-Kind</span></span>
<span data-ttu-id="23816-114">Виды приложения.</span><span class="sxs-lookup"><span data-stu-id="23816-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23816-115">-Location</span><span class="sxs-lookup"><span data-stu-id="23816-115">-Location</span></span>
<span data-ttu-id="23816-116">Расположение ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="23816-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23816-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23816-117">-Name</span></span>
<span data-ttu-id="23816-118">Название ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="23816-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23816-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="23816-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="23816-120">Тип сетевого доступа для получения доступа к Application Insights.</span><span class="sxs-lookup"><span data-stu-id="23816-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="23816-121">Значение должно быть "включено" или "отключено"</span><span class="sxs-lookup"><span data-stu-id="23816-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23816-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="23816-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="23816-123">Тип сетевого доступа для доступа к запросу Application Insights.</span><span class="sxs-lookup"><span data-stu-id="23816-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="23816-124">Значение должно быть "включено" или "отключено"</span><span class="sxs-lookup"><span data-stu-id="23816-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23816-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23816-125">-ResourceGroupName</span></span>
<span data-ttu-id="23816-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23816-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23816-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="23816-127">-RetentionInDays</span></span>
<span data-ttu-id="23816-128">Хранение в днях, 90 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23816-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23816-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="23816-129">-Tag</span></span>
<span data-ttu-id="23816-130">Теги компонентов.</span><span class="sxs-lookup"><span data-stu-id="23816-130">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23816-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23816-131">-Confirm</span></span>
<span data-ttu-id="23816-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="23816-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23816-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23816-133">-WhatIf</span></span>
<span data-ttu-id="23816-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="23816-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23816-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="23816-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23816-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23816-136">CommonParameters</span></span>
<span data-ttu-id="23816-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23816-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23816-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23816-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23816-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23816-139">INPUTS</span></span>

### <span data-ttu-id="23816-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="23816-140">None</span></span>

## <span data-ttu-id="23816-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23816-141">OUTPUTS</span></span>

### <span data-ttu-id="23816-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="23816-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="23816-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="23816-143">NOTES</span></span>

## <span data-ttu-id="23816-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23816-144">RELATED LINKS</span></span>
