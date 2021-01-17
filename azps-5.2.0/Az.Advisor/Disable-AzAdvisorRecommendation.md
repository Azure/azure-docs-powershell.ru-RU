---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: c9ad0e4b6744c00e9b3f4e7894daa52d2575dd90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399495"
---
# <span data-ttu-id="967f1-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="967f1-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="967f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="967f1-102">SYNOPSIS</span></span>
<span data-ttu-id="967f1-103">Отключать рекомендации консультанта Azure.</span><span class="sxs-lookup"><span data-stu-id="967f1-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="967f1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="967f1-104">SYNTAX</span></span>

### <span data-ttu-id="967f1-105">IdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="967f1-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="967f1-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="967f1-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="967f1-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="967f1-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="967f1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="967f1-108">DESCRIPTION</span></span>
<span data-ttu-id="967f1-109">Это позволяет отложить определенную рекомендацию на определенный срок или на бесконечное время.</span><span class="sxs-lookup"><span data-stu-id="967f1-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="967f1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="967f1-110">EXAMPLES</span></span>

### <span data-ttu-id="967f1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="967f1-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="967f1-112">Создайте подавления для названия рекомендации, задав значение по умолчанию -SuppressionName, а дни по умолчанию — как -1.</span><span class="sxs-lookup"><span data-stu-id="967f1-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="967f1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="967f1-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="967f1-114">Для данного ИД рекомендации создается подавляция.</span><span class="sxs-lookup"><span data-stu-id="967f1-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="967f1-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="967f1-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzAdvisorRecommendation -ResourceId "/subscriptions/user_subscription/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" | Disable-A
zAdvisorRecommendation

SuppressionId : daf24e78-af2d-e8d3-9c50-fa970edc2937
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="967f1-116">Создание отключения с помощью Get-AzAdvisorRecommendation в disable-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="967f1-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="967f1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="967f1-117">PARAMETERS</span></span>

### <span data-ttu-id="967f1-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="967f1-118">-Confirm</span></span>
<span data-ttu-id="967f1-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="967f1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="967f1-120">-Дни</span><span class="sxs-lookup"><span data-stu-id="967f1-120">-Days</span></span>
<span data-ttu-id="967f1-121">Дни, которые нужно отключить.</span><span class="sxs-lookup"><span data-stu-id="967f1-121">Days to disable.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="967f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="967f1-122">-DefaultProfile</span></span>
<span data-ttu-id="967f1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="967f1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="967f1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="967f1-124">-InputObject</span></span>
<span data-ttu-id="967f1-125">Объект Powershell типа PsAzureAdvisorResourceRecommendationBase, Get-AzAdvisorRecommendation звонка.</span><span class="sxs-lookup"><span data-stu-id="967f1-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="967f1-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="967f1-126">-RecommendationName</span></span>
<span data-ttu-id="967f1-127">Имя ресурса рекомендации</span><span class="sxs-lookup"><span data-stu-id="967f1-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="967f1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="967f1-128">-ResourceId</span></span>
<span data-ttu-id="967f1-129">ИД рекомендации, которая должна быть подавляемой.</span><span class="sxs-lookup"><span data-stu-id="967f1-129">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="967f1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="967f1-130">-WhatIf</span></span>
<span data-ttu-id="967f1-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="967f1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="967f1-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="967f1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="967f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="967f1-133">CommonParameters</span></span>
<span data-ttu-id="967f1-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="967f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="967f1-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="967f1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="967f1-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="967f1-136">INPUTS</span></span>

### <span data-ttu-id="967f1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="967f1-137">System.String</span></span>

### <span data-ttu-id="967f1-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="967f1-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="967f1-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="967f1-139">OUTPUTS</span></span>

### <span data-ttu-id="967f1-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="967f1-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="967f1-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="967f1-141">NOTES</span></span>

## <span data-ttu-id="967f1-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="967f1-142">RELATED LINKS</span></span>
