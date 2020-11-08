---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248172"
---
# <span data-ttu-id="e3284-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="e3284-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="e3284-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3284-102">SYNOPSIS</span></span>
<span data-ttu-id="e3284-103">Возвращает подписку, которая приводит к подписке.</span><span class="sxs-lookup"><span data-stu-id="e3284-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e3284-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3284-104">SYNTAX</span></span>

### <span data-ttu-id="e3284-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3284-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3284-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e3284-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3284-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="e3284-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3284-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="e3284-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3284-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3284-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3284-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3284-110">DESCRIPTION</span></span>
<span data-ttu-id="e3284-111">Возвращает подписку, которая приводит к подписке.</span><span class="sxs-lookup"><span data-stu-id="e3284-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e3284-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3284-112">EXAMPLES</span></span>

### <span data-ttu-id="e3284-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e3284-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="e3284-114">Возвращает все подзадачи, которые приводят к подписке.</span><span class="sxs-lookup"><span data-stu-id="e3284-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e3284-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3284-115">PARAMETERS</span></span>

### <span data-ttu-id="e3284-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="e3284-116">-AssessedResourceId</span></span>
<span data-ttu-id="e3284-117">Полный идентификатор ресурса, для которого рассчитывается оценка.</span><span class="sxs-lookup"><span data-stu-id="e3284-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="e3284-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="e3284-118">-AssessmentName</span></span>
<span data-ttu-id="e3284-119">Название ресурса оценки.</span><span class="sxs-lookup"><span data-stu-id="e3284-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="e3284-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3284-120">-DefaultProfile</span></span>
<span data-ttu-id="e3284-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3284-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3284-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3284-122">-Name</span></span>
<span data-ttu-id="e3284-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e3284-123">Resource name.</span></span>

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

### <span data-ttu-id="e3284-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3284-124">-ResourceId</span></span>
<span data-ttu-id="e3284-125">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="e3284-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e3284-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3284-126">CommonParameters</span></span>
<span data-ttu-id="e3284-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3284-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3284-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3284-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3284-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3284-129">INPUTS</span></span>

### <span data-ttu-id="e3284-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e3284-130">System.String</span></span>

## <span data-ttu-id="e3284-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3284-131">OUTPUTS</span></span>

### <span data-ttu-id="e3284-132">Microsoft. Azure. Commands. Security. Models. reоценивающие. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="e3284-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="e3284-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3284-133">NOTES</span></span>

## <span data-ttu-id="e3284-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3284-134">RELATED LINKS</span></span>
