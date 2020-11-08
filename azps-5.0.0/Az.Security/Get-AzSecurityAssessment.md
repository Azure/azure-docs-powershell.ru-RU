---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249464"
---
# <span data-ttu-id="e8e8d-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e8e8d-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="e8e8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e8d-103">Получение оценок системы безопасности и их результатов в подписке</span><span class="sxs-lookup"><span data-stu-id="e8e8d-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="e8e8d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8e8d-104">SYNTAX</span></span>

### <span data-ttu-id="e8e8d-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8e8d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8e8d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e8e8d-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8e8d-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="e8e8d-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8e8d-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e8d-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8e8d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8e8d-109">DESCRIPTION</span></span>
<span data-ttu-id="e8e8d-110">Получение оценки безопасности и результатов их проведения на подписке.</span><span class="sxs-lookup"><span data-stu-id="e8e8d-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="e8e8d-111">С помощью средств оценки безопасности вы узнаете, какие рекомендации будут передаваться центром безопасности Azure для устранения проблем с вашей подпиской на Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e8d-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="e8e8d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8e8d-112">EXAMPLES</span></span>

### <span data-ttu-id="e8e8d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8e8d-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="e8e8d-114">Получение всей оценки безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="e8e8d-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="e8e8d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8e8d-115">PARAMETERS</span></span>

### <span data-ttu-id="e8e8d-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e8d-116">-AssessedResourceId</span></span>
<span data-ttu-id="e8e8d-117">Полный идентификатор ресурса, для которого рассчитывается оценка.</span><span class="sxs-lookup"><span data-stu-id="e8e8d-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="e8e8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e8d-118">-DefaultProfile</span></span>
<span data-ttu-id="e8e8d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e8d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8e8d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8e8d-120">-Name</span></span>
<span data-ttu-id="e8e8d-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e8e8d-121">Resource name.</span></span>

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

### <span data-ttu-id="e8e8d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e8d-122">-ResourceId</span></span>
<span data-ttu-id="e8e8d-123">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="e8e8d-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e8e8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e8d-124">CommonParameters</span></span>
<span data-ttu-id="e8e8d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8e8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e8d-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8e8d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e8d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8e8d-127">INPUTS</span></span>

### <span data-ttu-id="e8e8d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e8e8d-128">System.String</span></span>

## <span data-ttu-id="e8e8d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8e8d-129">OUTPUTS</span></span>

### <span data-ttu-id="e8e8d-130">Microsoft. Azure. Commands. Security. Models. оценивающие. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e8e8d-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="e8e8d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8e8d-131">NOTES</span></span>

## <span data-ttu-id="e8e8d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8e8d-132">RELATED LINKS</span></span>
