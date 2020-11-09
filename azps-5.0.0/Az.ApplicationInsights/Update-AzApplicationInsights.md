---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316248"
---
# <span data-ttu-id="f1335-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f1335-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="f1335-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1335-102">SYNOPSIS</span></span>
<span data-ttu-id="f1335-103">Обновление существующего ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="f1335-103">update an existing application insights resource</span></span>

## <span data-ttu-id="f1335-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1335-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1335-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1335-105">DESCRIPTION</span></span>
<span data-ttu-id="f1335-106">Обновление существующего ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="f1335-106">update an existing application insights resource</span></span>

## <span data-ttu-id="f1335-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1335-107">EXAMPLES</span></span>

### <span data-ttu-id="f1335-108">Пример 1 обновление компонента Application Insights</span><span class="sxs-lookup"><span data-stu-id="f1335-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="f1335-109">Обновление компонента Application Insights "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery "отключено"</span><span class="sxs-lookup"><span data-stu-id="f1335-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="f1335-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1335-110">PARAMETERS</span></span>

### <span data-ttu-id="f1335-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1335-111">-DefaultProfile</span></span>
<span data-ttu-id="f1335-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1335-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1335-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1335-113">-Name</span></span>
<span data-ttu-id="f1335-114">Название ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f1335-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="f1335-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="f1335-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="f1335-116">Тип сетевого доступа для получения доступа к Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f1335-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="f1335-117">Значение должно быть "включено" или "отключено"</span><span class="sxs-lookup"><span data-stu-id="f1335-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="f1335-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="f1335-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="f1335-119">Тип сетевого доступа для доступа к запросу Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f1335-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="f1335-120">Значение должно быть "включено" или "отключено"</span><span class="sxs-lookup"><span data-stu-id="f1335-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="f1335-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1335-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1335-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1335-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1335-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f1335-123">-RetentionInDays</span></span>
<span data-ttu-id="f1335-124">Хранение в днях, 90 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1335-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="f1335-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="f1335-125">-Tag</span></span>
<span data-ttu-id="f1335-126">Теги компонентов.</span><span class="sxs-lookup"><span data-stu-id="f1335-126">Component Tags.</span></span>

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

### <span data-ttu-id="f1335-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1335-127">-Confirm</span></span>
<span data-ttu-id="f1335-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1335-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1335-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1335-129">-WhatIf</span></span>
<span data-ttu-id="f1335-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1335-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1335-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1335-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1335-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1335-132">CommonParameters</span></span>
<span data-ttu-id="f1335-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1335-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1335-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1335-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1335-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1335-135">INPUTS</span></span>

### <span data-ttu-id="f1335-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f1335-136">System.String</span></span>

## <span data-ttu-id="f1335-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1335-137">OUTPUTS</span></span>

### <span data-ttu-id="f1335-138">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f1335-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="f1335-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1335-139">NOTES</span></span>

## <span data-ttu-id="f1335-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1335-140">RELATED LINKS</span></span>
