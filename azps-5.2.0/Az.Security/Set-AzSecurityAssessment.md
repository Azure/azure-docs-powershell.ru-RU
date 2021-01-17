---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394740"
---
# <span data-ttu-id="da1a7-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="da1a7-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="da1a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da1a7-102">SYNOPSIS</span></span>
<span data-ttu-id="da1a7-103">Создание или обновление результатов оценки безопасности для ресурса</span><span class="sxs-lookup"><span data-stu-id="da1a7-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="da1a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da1a7-104">SYNTAX</span></span>

### <span data-ttu-id="da1a7-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da1a7-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da1a7-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="da1a7-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da1a7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da1a7-107">DESCRIPTION</span></span>
<span data-ttu-id="da1a7-108">Создайте или обновив результаты оценки безопасности для ресурса, можно использовать для изменения состояния существующего результата или добавления дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="da1a7-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="da1a7-109">могут использоваться только для типов оценок CustomerManaged и только после создания метаданных оценки с соответствием.</span><span class="sxs-lookup"><span data-stu-id="da1a7-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="da1a7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da1a7-110">EXAMPLES</span></span>

### <span data-ttu-id="da1a7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da1a7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="da1a7-112">Пометка результата подписки как неработоспособного для оценки типа "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" — дополнительные сведения о типе оценки можно найти в типе assessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="da1a7-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="da1a7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da1a7-113">PARAMETERS</span></span>

### <span data-ttu-id="da1a7-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="da1a7-114">-AdditionalData</span></span>
<span data-ttu-id="da1a7-115">Данные, которые прикрепляются к результатам оценки для более четкого исследования или четкости состояния.</span><span class="sxs-lookup"><span data-stu-id="da1a7-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a7-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="da1a7-116">-AssessedResourceId</span></span>
<span data-ttu-id="da1a7-117">Полный ИД ресурса, на основе который вычисляется оценка.</span><span class="sxs-lookup"><span data-stu-id="da1a7-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="da1a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da1a7-118">-DefaultProfile</span></span>
<span data-ttu-id="da1a7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da1a7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da1a7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="da1a7-120">-Name</span></span>
<span data-ttu-id="da1a7-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="da1a7-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a7-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="da1a7-122">-StatusCause</span></span>
<span data-ttu-id="da1a7-123">Progremmatic code for the cause of the assessment's result.</span><span class="sxs-lookup"><span data-stu-id="da1a7-123">Progremmatic code for the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a7-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="da1a7-124">-StatusCode</span></span>
<span data-ttu-id="da1a7-125">Прогреметный код для результата оценки.</span><span class="sxs-lookup"><span data-stu-id="da1a7-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="da1a7-126">могут быть неработоспособными или неработоспособными.</span><span class="sxs-lookup"><span data-stu-id="da1a7-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
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

### <span data-ttu-id="da1a7-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="da1a7-127">-StatusDescription</span></span>
<span data-ttu-id="da1a7-128">Понятное описание причин, повестовав оценку.</span><span class="sxs-lookup"><span data-stu-id="da1a7-128">Human readable description of the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1a7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da1a7-129">-Confirm</span></span>
<span data-ttu-id="da1a7-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="da1a7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da1a7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da1a7-131">-WhatIf</span></span>
<span data-ttu-id="da1a7-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da1a7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da1a7-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="da1a7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da1a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da1a7-134">CommonParameters</span></span>
<span data-ttu-id="da1a7-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da1a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da1a7-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da1a7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da1a7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da1a7-137">INPUTS</span></span>

### <span data-ttu-id="da1a7-138">Нет</span><span class="sxs-lookup"><span data-stu-id="da1a7-138">None</span></span>

## <span data-ttu-id="da1a7-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da1a7-139">OUTPUTS</span></span>

### <span data-ttu-id="da1a7-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="da1a7-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="da1a7-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da1a7-141">NOTES</span></span>

## <span data-ttu-id="da1a7-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da1a7-142">RELATED LINKS</span></span>
