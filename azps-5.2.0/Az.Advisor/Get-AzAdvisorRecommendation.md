---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399492"
---
# <span data-ttu-id="73774-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="73774-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="73774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73774-102">SYNOPSIS</span></span>
<span data-ttu-id="73774-103">Получает список рекомендаций консультанта Azure.</span><span class="sxs-lookup"><span data-stu-id="73774-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="73774-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73774-104">SYNTAX</span></span>

### <span data-ttu-id="73774-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73774-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73774-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73774-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73774-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73774-107">DESCRIPTION</span></span>
<span data-ttu-id="73774-108">Получение списка рекомендаций консультанта Azure.</span><span class="sxs-lookup"><span data-stu-id="73774-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="73774-109">Можно отфильтровать по категориям, ИД ресурсов, именам и т. д.</span><span class="sxs-lookup"><span data-stu-id="73774-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="73774-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73774-110">EXAMPLES</span></span>

### <span data-ttu-id="73774-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="73774-111">Example 1</span></span>
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
<span data-ttu-id="73774-112">Получает список всех рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="73774-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="73774-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="73774-113">Example 2</span></span>
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
<span data-ttu-id="73774-114">Возвращает список всех рекомендаций, отфильтрованных по категориям Производительность.</span><span class="sxs-lookup"><span data-stu-id="73774-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="73774-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73774-115">PARAMETERS</span></span>

### <span data-ttu-id="73774-116">-Category</span><span class="sxs-lookup"><span data-stu-id="73774-116">-Category</span></span>
<span data-ttu-id="73774-117">Категория рекомендации</span><span class="sxs-lookup"><span data-stu-id="73774-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security, OperationalExcellence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73774-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73774-118">-DefaultProfile</span></span>
<span data-ttu-id="73774-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73774-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73774-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73774-120">-ResourceGroupName</span></span>
<span data-ttu-id="73774-121">Имя группы ресурсов рекомендации</span><span class="sxs-lookup"><span data-stu-id="73774-121">ResourceGroup name of the recommendation</span></span>

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

### <span data-ttu-id="73774-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73774-122">-ResourceId</span></span>
<span data-ttu-id="73774-123">ResourceId рекомендации</span><span class="sxs-lookup"><span data-stu-id="73774-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="73774-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73774-124">CommonParameters</span></span>
<span data-ttu-id="73774-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73774-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="73774-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73774-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73774-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73774-127">INPUTS</span></span>

### <span data-ttu-id="73774-128">System.String</span><span class="sxs-lookup"><span data-stu-id="73774-128">System.String</span></span>

## <span data-ttu-id="73774-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73774-129">OUTPUTS</span></span>

### <span data-ttu-id="73774-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="73774-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="73774-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73774-131">NOTES</span></span>

## <span data-ttu-id="73774-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73774-132">RELATED LINKS</span></span>
