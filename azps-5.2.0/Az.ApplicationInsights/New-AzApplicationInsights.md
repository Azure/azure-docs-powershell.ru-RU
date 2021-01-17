---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406812"
---
# <span data-ttu-id="fab5a-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fab5a-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="fab5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab5a-102">SYNOPSIS</span></span>
<span data-ttu-id="fab5a-103">Создание нового ресурса для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="fab5a-103">Create a new application insights resource</span></span>

## <span data-ttu-id="fab5a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fab5a-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fab5a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fab5a-105">DESCRIPTION</span></span>
<span data-ttu-id="fab5a-106">Создание нового ресурса для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="fab5a-106">Create a new application insights resource</span></span>

## <span data-ttu-id="fab5a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fab5a-107">EXAMPLES</span></span>

### <span data-ttu-id="fab5a-108">Пример 1. Создание нового ресурса для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="fab5a-108">Example 1 Create a new application insights resource</span></span>
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

<span data-ttu-id="fab5a-109">Добавление нового ресурса аналитики приложений с именем "тест" в группе ресурсов "testgroup" с типом "java"</span><span class="sxs-lookup"><span data-stu-id="fab5a-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="fab5a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fab5a-110">PARAMETERS</span></span>

### <span data-ttu-id="fab5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab5a-111">-DefaultProfile</span></span>
<span data-ttu-id="fab5a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fab5a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fab5a-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="fab5a-113">-Kind</span></span>
<span data-ttu-id="fab5a-114">Тип приложения.</span><span class="sxs-lookup"><span data-stu-id="fab5a-114">Application kind.</span></span>

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

### <span data-ttu-id="fab5a-115">-Location</span><span class="sxs-lookup"><span data-stu-id="fab5a-115">-Location</span></span>
<span data-ttu-id="fab5a-116">Расположение ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="fab5a-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="fab5a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fab5a-117">-Name</span></span>
<span data-ttu-id="fab5a-118">Имя ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="fab5a-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="fab5a-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="fab5a-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="fab5a-120">Тип сетевого доступа для доступа к анализу приложений.</span><span class="sxs-lookup"><span data-stu-id="fab5a-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="fab5a-121">Значение должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="fab5a-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="fab5a-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="fab5a-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="fab5a-123">Тип доступа к сети для запроса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="fab5a-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="fab5a-124">Значение должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="fab5a-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="fab5a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab5a-125">-ResourceGroupName</span></span>
<span data-ttu-id="fab5a-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fab5a-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="fab5a-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="fab5a-127">-RetentionInDays</span></span>
<span data-ttu-id="fab5a-128">Хранение в днях, 90 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fab5a-128">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="fab5a-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="fab5a-129">-Tag</span></span>
<span data-ttu-id="fab5a-130">Теги компонентов.</span><span class="sxs-lookup"><span data-stu-id="fab5a-130">Component Tags.</span></span>

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

### <span data-ttu-id="fab5a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fab5a-131">-Confirm</span></span>
<span data-ttu-id="fab5a-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fab5a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab5a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab5a-133">-WhatIf</span></span>
<span data-ttu-id="fab5a-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fab5a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fab5a-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fab5a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab5a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab5a-136">CommonParameters</span></span>
<span data-ttu-id="fab5a-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab5a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab5a-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fab5a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab5a-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fab5a-139">INPUTS</span></span>

### <span data-ttu-id="fab5a-140">Нет</span><span class="sxs-lookup"><span data-stu-id="fab5a-140">None</span></span>

## <span data-ttu-id="fab5a-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fab5a-141">OUTPUTS</span></span>

### <span data-ttu-id="fab5a-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="fab5a-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="fab5a-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fab5a-143">NOTES</span></span>

## <span data-ttu-id="fab5a-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fab5a-144">RELATED LINKS</span></span>
