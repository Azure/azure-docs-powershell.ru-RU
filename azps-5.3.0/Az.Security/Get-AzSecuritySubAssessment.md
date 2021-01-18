---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517690"
---
# <span data-ttu-id="0279b-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="0279b-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="0279b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0279b-102">SYNOPSIS</span></span>
<span data-ttu-id="0279b-103">Получает результаты оценки в подписке.</span><span class="sxs-lookup"><span data-stu-id="0279b-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="0279b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0279b-104">SYNTAX</span></span>

### <span data-ttu-id="0279b-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0279b-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0279b-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="0279b-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0279b-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="0279b-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0279b-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="0279b-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0279b-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0279b-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0279b-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0279b-110">DESCRIPTION</span></span>
<span data-ttu-id="0279b-111">Получает результаты оценки в подписке.</span><span class="sxs-lookup"><span data-stu-id="0279b-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="0279b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0279b-112">EXAMPLES</span></span>

### <span data-ttu-id="0279b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0279b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="0279b-114">Получает все результаты оценки в подписке.</span><span class="sxs-lookup"><span data-stu-id="0279b-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="0279b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0279b-115">PARAMETERS</span></span>

### <span data-ttu-id="0279b-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="0279b-116">-AssessedResourceId</span></span>
<span data-ttu-id="0279b-117">Полный ИД ресурса, на основе который вычисляется оценка.</span><span class="sxs-lookup"><span data-stu-id="0279b-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="0279b-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="0279b-118">-AssessmentName</span></span>
<span data-ttu-id="0279b-119">Название ресурса оценки.</span><span class="sxs-lookup"><span data-stu-id="0279b-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="0279b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0279b-120">-DefaultProfile</span></span>
<span data-ttu-id="0279b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0279b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0279b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0279b-122">-Name</span></span>
<span data-ttu-id="0279b-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="0279b-123">Resource name.</span></span>

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

### <span data-ttu-id="0279b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0279b-124">-ResourceId</span></span>
<span data-ttu-id="0279b-125">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="0279b-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="0279b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0279b-126">CommonParameters</span></span>
<span data-ttu-id="0279b-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0279b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0279b-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0279b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0279b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0279b-129">INPUTS</span></span>

### <span data-ttu-id="0279b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0279b-130">System.String</span></span>

## <span data-ttu-id="0279b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0279b-131">OUTPUTS</span></span>

### <span data-ttu-id="0279b-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="0279b-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="0279b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0279b-133">NOTES</span></span>

## <span data-ttu-id="0279b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0279b-134">RELATED LINKS</span></span>
