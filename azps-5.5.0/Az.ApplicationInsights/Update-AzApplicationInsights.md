---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244301"
---
# <span data-ttu-id="4acd9-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4acd9-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="4acd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4acd9-102">SYNOPSIS</span></span>
<span data-ttu-id="4acd9-103">Обновление существующего ресурса статистики приложения</span><span class="sxs-lookup"><span data-stu-id="4acd9-103">update an existing application insights resource</span></span>

## <span data-ttu-id="4acd9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4acd9-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4acd9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4acd9-105">DESCRIPTION</span></span>
<span data-ttu-id="4acd9-106">Обновление существующего ресурса статистики приложения</span><span class="sxs-lookup"><span data-stu-id="4acd9-106">update an existing application insights resource</span></span>

## <span data-ttu-id="4acd9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4acd9-107">EXAMPLES</span></span>

### <span data-ttu-id="4acd9-108">Пример 1. Компонент "Обновление статистики приложения"</span><span class="sxs-lookup"><span data-stu-id="4acd9-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="4acd9-109">Update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to disabled</span><span class="sxs-lookup"><span data-stu-id="4acd9-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="4acd9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4acd9-110">PARAMETERS</span></span>

### <span data-ttu-id="4acd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4acd9-111">-DefaultProfile</span></span>
<span data-ttu-id="4acd9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4acd9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4acd9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4acd9-113">-Name</span></span>
<span data-ttu-id="4acd9-114">Имя ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4acd9-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="4acd9-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="4acd9-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="4acd9-116">Тип сетевого доступа для доступа к анализу приложений.</span><span class="sxs-lookup"><span data-stu-id="4acd9-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="4acd9-117">Значение должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="4acd9-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="4acd9-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="4acd9-119">Тип доступа к сети для запроса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4acd9-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="4acd9-120">Значение должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="4acd9-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4acd9-121">-ResourceGroupName</span></span>
<span data-ttu-id="4acd9-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4acd9-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="4acd9-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4acd9-123">-RetentionInDays</span></span>
<span data-ttu-id="4acd9-124">Хранение в днях, 90 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4acd9-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4acd9-125">-Tag</span></span>
<span data-ttu-id="4acd9-126">Теги компонентов.</span><span class="sxs-lookup"><span data-stu-id="4acd9-126">Component Tags.</span></span>

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

### <span data-ttu-id="4acd9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4acd9-127">-Confirm</span></span>
<span data-ttu-id="4acd9-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4acd9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4acd9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4acd9-129">-WhatIf</span></span>
<span data-ttu-id="4acd9-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4acd9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4acd9-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4acd9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4acd9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4acd9-132">CommonParameters</span></span>
<span data-ttu-id="4acd9-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4acd9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4acd9-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4acd9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4acd9-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4acd9-135">INPUTS</span></span>

### <span data-ttu-id="4acd9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4acd9-136">System.String</span></span>

## <span data-ttu-id="4acd9-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4acd9-137">OUTPUTS</span></span>

### <span data-ttu-id="4acd9-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4acd9-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="4acd9-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4acd9-139">NOTES</span></span>

## <span data-ttu-id="4acd9-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4acd9-140">RELATED LINKS</span></span>
