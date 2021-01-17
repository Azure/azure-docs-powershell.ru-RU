---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399500"
---
# <span data-ttu-id="d2a1d-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="d2a1d-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="d2a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a1d-103">Включает рекомендации консультанта Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="d2a1d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2a1d-104">SYNTAX</span></span>

### <span data-ttu-id="d2a1d-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2a1d-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a1d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2a1d-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a1d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2a1d-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2a1d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2a1d-108">DESCRIPTION</span></span>
<span data-ttu-id="d2a1d-109">Этот cmdlet включает ранее не подавляемую рекомендацию.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="d2a1d-110">Вы также можете удалить все отвества, связанные с рекомендациями.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="d2a1d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2a1d-111">EXAMPLES</span></span>

### <span data-ttu-id="d2a1d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2a1d-112">Example 1</span></span>
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="d2a1d-113">Удаление всех подавляний для данной рекомендации с именем "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="d2a1d-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="d2a1d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d2a1d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="d2a1d-115">Удаление всех подавляний для переданных рекомендаций из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="d2a1d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2a1d-116">PARAMETERS</span></span>

### <span data-ttu-id="d2a1d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2a1d-117">-Confirm</span></span>
<span data-ttu-id="d2a1d-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a1d-119">-DefaultProfile</span></span>
<span data-ttu-id="d2a1d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2a1d-121">-InputObject</span></span>
<span data-ttu-id="d2a1d-122">Объект Powershell типа PsAzureAdvisorResourceRecommendationBase, Get-AzAdvisorRecommendation звонка.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1d-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="d2a1d-123">-RecommendationName</span></span>
<span data-ttu-id="d2a1d-124">Имя ресурса рекомендации.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-124">ResourceName of the recommendation.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a1d-125">-ResourceId</span></span>
<span data-ttu-id="d2a1d-126">ИД рекомендации, которая должна быть подавляемой.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-126">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a1d-127">-WhatIf</span></span>
<span data-ttu-id="d2a1d-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2a1d-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a1d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a1d-130">CommonParameters</span></span>
<span data-ttu-id="d2a1d-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a1d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d2a1d-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a1d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a1d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2a1d-133">INPUTS</span></span>

### <span data-ttu-id="d2a1d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d2a1d-134">System.String</span></span>

### <span data-ttu-id="d2a1d-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="d2a1d-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="d2a1d-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2a1d-136">OUTPUTS</span></span>

### <span data-ttu-id="d2a1d-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="d2a1d-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="d2a1d-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2a1d-138">NOTES</span></span>

## <span data-ttu-id="d2a1d-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2a1d-139">RELATED LINKS</span></span>
