---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 5a8a09955158c21ff6d52e2327370c48448c12d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008547"
---
# <span data-ttu-id="e6ffd-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e6ffd-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="e6ffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ffd-103">Оценка безопасности и их результаты по подписке</span><span class="sxs-lookup"><span data-stu-id="e6ffd-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="e6ffd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6ffd-104">SYNTAX</span></span>

### <span data-ttu-id="e6ffd-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6ffd-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6ffd-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e6ffd-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6ffd-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="e6ffd-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6ffd-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6ffd-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6ffd-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6ffd-109">DESCRIPTION</span></span>
<span data-ttu-id="e6ffd-110">Возвращает оценку безопасности и результаты по подписке.</span><span class="sxs-lookup"><span data-stu-id="e6ffd-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="e6ffd-111">При оценке безопасности вы узнаете, какие советы и методики можно повторно использовать в Центре безопасности Azure для снижения уровня вашей подписки на Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ffd-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="e6ffd-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6ffd-112">EXAMPLES</span></span>

### <span data-ttu-id="e6ffd-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6ffd-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="e6ffd-114">Все оценки безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="e6ffd-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="e6ffd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6ffd-115">PARAMETERS</span></span>

### <span data-ttu-id="e6ffd-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="e6ffd-116">-AssessedResourceId</span></span>
<span data-ttu-id="e6ffd-117">Полный ИД ресурса, на основе который вычисляется оценка.</span><span class="sxs-lookup"><span data-stu-id="e6ffd-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ffd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ffd-118">-DefaultProfile</span></span>
<span data-ttu-id="e6ffd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ffd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ffd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e6ffd-120">-Name</span></span>
<span data-ttu-id="e6ffd-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e6ffd-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ffd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6ffd-122">-ResourceId</span></span>
<span data-ttu-id="e6ffd-123">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="e6ffd-123">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ffd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ffd-124">CommonParameters</span></span>
<span data-ttu-id="e6ffd-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ffd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ffd-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6ffd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ffd-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6ffd-127">INPUTS</span></span>

### <span data-ttu-id="e6ffd-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e6ffd-128">System.String</span></span>

## <span data-ttu-id="e6ffd-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6ffd-129">OUTPUTS</span></span>

### <span data-ttu-id="e6ffd-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e6ffd-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="e6ffd-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6ffd-131">NOTES</span></span>

## <span data-ttu-id="e6ffd-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6ffd-132">RELATED LINKS</span></span>
