---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066458"
---
# <span data-ttu-id="2c1ee-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="2c1ee-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="2c1ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c1ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1ee-103">Включает рекомендации для Azure Advisor (-ы).</span><span class="sxs-lookup"><span data-stu-id="2c1ee-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="2c1ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c1ee-104">SYNTAX</span></span>

### <span data-ttu-id="2c1ee-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c1ee-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c1ee-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c1ee-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c1ee-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c1ee-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c1ee-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c1ee-108">DESCRIPTION</span></span>
<span data-ttu-id="2c1ee-109">Этот командлет включает ранее подавленную рекомендацию.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="2c1ee-110">Вы можете также удалить все подавления, связанные с рекомендацией.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="2c1ee-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c1ee-111">EXAMPLES</span></span>

### <span data-ttu-id="2c1ee-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2c1ee-112">Example 1</span></span>
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

<span data-ttu-id="2c1ee-113">Удаляет все подавление для указанной рекомендации с именем "recommendation_id".</span><span class="sxs-lookup"><span data-stu-id="2c1ee-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="2c1ee-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2c1ee-114">Example 2</span></span>
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

<span data-ttu-id="2c1ee-115">Удаляет все подавление для указанных рекомендаций, переданных из конвейера.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="2c1ee-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c1ee-116">PARAMETERS</span></span>

### <span data-ttu-id="2c1ee-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c1ee-117">-Confirm</span></span>
<span data-ttu-id="2c1ee-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c1ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1ee-119">-DefaultProfile</span></span>
<span data-ttu-id="2c1ee-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c1ee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c1ee-121">-InputObject</span></span>
<span data-ttu-id="2c1ee-122">PsAzureAdvisorResourceRecommendationBase тип объекта PowerShell, возвращенный вызовом Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="2c1ee-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="2c1ee-123">-RecommendationName</span></span>
<span data-ttu-id="2c1ee-124">ResourceName (значение) рекомендации.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="2c1ee-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c1ee-125">-ResourceId</span></span>
<span data-ttu-id="2c1ee-126">Идентификатор рекомендации, которое нужно отключить.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="2c1ee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c1ee-127">-WhatIf</span></span>
<span data-ttu-id="2c1ee-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c1ee-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c1ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1ee-130">CommonParameters</span></span>
<span data-ttu-id="2c1ee-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c1ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2c1ee-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c1ee-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1ee-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c1ee-133">INPUTS</span></span>

### <span data-ttu-id="2c1ee-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2c1ee-134">System.String</span></span>

### <span data-ttu-id="2c1ee-135">Microsoft. Azure. Commands. Advisor. командлеты. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="2c1ee-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="2c1ee-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c1ee-136">OUTPUTS</span></span>

### <span data-ttu-id="2c1ee-137">Microsoft. Azure. Commands. Advisor. командлеты. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="2c1ee-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="2c1ee-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c1ee-138">NOTES</span></span>

## <span data-ttu-id="2c1ee-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c1ee-139">RELATED LINKS</span></span>
