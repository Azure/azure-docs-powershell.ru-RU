---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235866"
---
# <span data-ttu-id="e8698-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="e8698-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="e8698-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8698-102">SYNOPSIS</span></span>
<span data-ttu-id="e8698-103">Возвращает подписку, которая приводит к подписке.</span><span class="sxs-lookup"><span data-stu-id="e8698-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e8698-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8698-104">SYNTAX</span></span>

### <span data-ttu-id="e8698-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8698-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8698-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e8698-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8698-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="e8698-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8698-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="e8698-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8698-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8698-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8698-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8698-110">DESCRIPTION</span></span>
<span data-ttu-id="e8698-111">Возвращает подписку, которая приводит к подписке.</span><span class="sxs-lookup"><span data-stu-id="e8698-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e8698-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8698-112">EXAMPLES</span></span>

### <span data-ttu-id="e8698-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8698-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="e8698-114">Возвращает все подзадачи, которые приводят к подписке.</span><span class="sxs-lookup"><span data-stu-id="e8698-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e8698-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8698-115">PARAMETERS</span></span>

### <span data-ttu-id="e8698-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="e8698-116">-AssessedResourceId</span></span>
<span data-ttu-id="e8698-117">Полный идентификатор ресурса, для которого рассчитывается оценка.</span><span class="sxs-lookup"><span data-stu-id="e8698-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="e8698-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="e8698-118">-AssessmentName</span></span>
<span data-ttu-id="e8698-119">Название ресурса оценки.</span><span class="sxs-lookup"><span data-stu-id="e8698-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="e8698-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8698-120">-DefaultProfile</span></span>
<span data-ttu-id="e8698-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8698-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8698-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8698-122">-Name</span></span>
<span data-ttu-id="e8698-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8698-123">Resource name.</span></span>

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

### <span data-ttu-id="e8698-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8698-124">-ResourceId</span></span>
<span data-ttu-id="e8698-125">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="e8698-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e8698-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8698-126">CommonParameters</span></span>
<span data-ttu-id="e8698-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8698-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8698-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8698-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8698-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8698-129">INPUTS</span></span>

### <span data-ttu-id="e8698-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8698-130">System.String</span></span>

## <span data-ttu-id="e8698-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8698-131">OUTPUTS</span></span>

### <span data-ttu-id="e8698-132">Microsoft. Azure. Commands. Security. Models. reоценивающие. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="e8698-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="e8698-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8698-133">NOTES</span></span>

## <span data-ttu-id="e8698-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8698-134">RELATED LINKS</span></span>
