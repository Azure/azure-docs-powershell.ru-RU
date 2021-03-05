---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: c371749643952e8209b3cbec0721331a4d380d94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011704"
---
# <span data-ttu-id="a1b27-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="a1b27-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="a1b27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1b27-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b27-103">Получает результаты в службе оценки в подписке.</span><span class="sxs-lookup"><span data-stu-id="a1b27-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="a1b27-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1b27-104">SYNTAX</span></span>

### <span data-ttu-id="a1b27-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1b27-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1b27-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a1b27-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1b27-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="a1b27-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1b27-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="a1b27-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1b27-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b27-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1b27-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1b27-110">DESCRIPTION</span></span>
<span data-ttu-id="a1b27-111">Получает результаты в службе оценки в подписке.</span><span class="sxs-lookup"><span data-stu-id="a1b27-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="a1b27-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1b27-112">EXAMPLES</span></span>

### <span data-ttu-id="a1b27-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1b27-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="a1b27-114">Получает все результаты оценки в подписке.</span><span class="sxs-lookup"><span data-stu-id="a1b27-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="a1b27-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1b27-115">PARAMETERS</span></span>

### <span data-ttu-id="a1b27-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b27-116">-AssessedResourceId</span></span>
<span data-ttu-id="a1b27-117">Полный ИД ресурса, на основе который вычисляется оценка.</span><span class="sxs-lookup"><span data-stu-id="a1b27-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionScope, SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b27-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="a1b27-118">-AssessmentName</span></span>
<span data-ttu-id="a1b27-119">Название ресурса оценки.</span><span class="sxs-lookup"><span data-stu-id="a1b27-119">Name of the assessment resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b27-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b27-120">-DefaultProfile</span></span>
<span data-ttu-id="a1b27-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b27-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b27-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a1b27-122">-Name</span></span>
<span data-ttu-id="a1b27-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1b27-123">Resource name.</span></span>

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
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b27-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b27-124">-ResourceId</span></span>
<span data-ttu-id="a1b27-125">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="a1b27-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a1b27-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b27-126">CommonParameters</span></span>
<span data-ttu-id="a1b27-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b27-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b27-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1b27-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b27-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1b27-129">INPUTS</span></span>

### <span data-ttu-id="a1b27-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a1b27-130">System.String</span></span>

## <span data-ttu-id="a1b27-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1b27-131">OUTPUTS</span></span>

### <span data-ttu-id="a1b27-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="a1b27-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="a1b27-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1b27-133">NOTES</span></span>

## <span data-ttu-id="a1b27-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1b27-134">RELATED LINKS</span></span>
