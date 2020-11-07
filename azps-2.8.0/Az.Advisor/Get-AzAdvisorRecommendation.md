---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 894fc2b3f3e722c7924e05e6c700ae03f741562f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728212"
---
# <span data-ttu-id="88001-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="88001-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="88001-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88001-102">SYNOPSIS</span></span>
<span data-ttu-id="88001-103">Получает список рекомендаций по Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="88001-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="88001-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88001-104">SYNTAX</span></span>

### <span data-ttu-id="88001-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88001-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88001-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88001-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88001-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88001-107">DESCRIPTION</span></span>
<span data-ttu-id="88001-108">Получение списка рекомендаций по Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="88001-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="88001-109">Можно отфильтровать по категории, ИДЕНТИФИКАТОРу ресурса, имени и т. д.</span><span class="sxs-lookup"><span data-stu-id="88001-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="88001-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88001-110">EXAMPLES</span></span>

### <span data-ttu-id="88001-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88001-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="88001-112">Получает список всех рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="88001-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="88001-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88001-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -Category Performance
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="88001-114">Получает список всех рекомендаций, отфильтрованных по категориям "производительность".</span><span class="sxs-lookup"><span data-stu-id="88001-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="88001-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88001-115">PARAMETERS</span></span>

### <span data-ttu-id="88001-116">-Категория</span><span class="sxs-lookup"><span data-stu-id="88001-116">-Category</span></span>
<span data-ttu-id="88001-117">Категория рекомендации</span><span class="sxs-lookup"><span data-stu-id="88001-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88001-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88001-118">-DefaultProfile</span></span>
<span data-ttu-id="88001-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88001-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88001-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88001-120">-ResourceGroupName</span></span>
<span data-ttu-id="88001-121">Имя ResourceGroup для рекомендации</span><span class="sxs-lookup"><span data-stu-id="88001-121">ResourceGroup name of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88001-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88001-122">-ResourceId</span></span>
<span data-ttu-id="88001-123">ResourceId для рекомендации</span><span class="sxs-lookup"><span data-stu-id="88001-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="88001-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88001-124">CommonParameters</span></span>
<span data-ttu-id="88001-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88001-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="88001-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88001-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88001-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88001-127">INPUTS</span></span>

### <span data-ttu-id="88001-128">System. String</span><span class="sxs-lookup"><span data-stu-id="88001-128">System.String</span></span>

## <span data-ttu-id="88001-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88001-129">OUTPUTS</span></span>

### <span data-ttu-id="88001-130">Microsoft. Azure. Commands. Advisor. командлеты. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="88001-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="88001-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="88001-131">NOTES</span></span>

## <span data-ttu-id="88001-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88001-132">RELATED LINKS</span></span>
