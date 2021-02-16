---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242349"
---
# <span data-ttu-id="23751-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="23751-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="23751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23751-102">SYNOPSIS</span></span>
<span data-ttu-id="23751-103">Удаляет метаданные оценки безопасности из подписки.</span><span class="sxs-lookup"><span data-stu-id="23751-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="23751-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23751-104">SYNTAX</span></span>

### <span data-ttu-id="23751-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23751-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23751-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="23751-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23751-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="23751-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23751-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23751-108">DESCRIPTION</span></span>
<span data-ttu-id="23751-109">Удаляет метаданные оценки безопасности из подписки.</span><span class="sxs-lookup"><span data-stu-id="23751-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="23751-110">Это действие удалит тип оценки и все соответствующие результаты оценки из подписки.</span><span class="sxs-lookup"><span data-stu-id="23751-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="23751-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23751-111">EXAMPLES</span></span>

### <span data-ttu-id="23751-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23751-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="23751-113">Удаление типа оценки из подписки</span><span class="sxs-lookup"><span data-stu-id="23751-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="23751-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23751-114">PARAMETERS</span></span>

### <span data-ttu-id="23751-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23751-115">-DefaultProfile</span></span>
<span data-ttu-id="23751-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23751-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23751-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23751-117">-InputObject</span></span>
<span data-ttu-id="23751-118">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="23751-118">Input Object.</span></span>

```yaml
Type: PSSecurityAssessmentMetadata
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23751-119">-Name</span><span class="sxs-lookup"><span data-stu-id="23751-119">-Name</span></span>
<span data-ttu-id="23751-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="23751-120">Resource name.</span></span>

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

### <span data-ttu-id="23751-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23751-121">-PassThru</span></span>
<span data-ttu-id="23751-122">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="23751-122">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23751-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23751-123">-ResourceId</span></span>
<span data-ttu-id="23751-124">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="23751-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="23751-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23751-125">-Confirm</span></span>
<span data-ttu-id="23751-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="23751-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23751-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23751-127">-WhatIf</span></span>
<span data-ttu-id="23751-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23751-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23751-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="23751-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23751-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23751-130">CommonParameters</span></span>
<span data-ttu-id="23751-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23751-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23751-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23751-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23751-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23751-133">INPUTS</span></span>

### <span data-ttu-id="23751-134">System.String</span><span class="sxs-lookup"><span data-stu-id="23751-134">System.String</span></span>

### <span data-ttu-id="23751-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="23751-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="23751-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23751-136">OUTPUTS</span></span>

### <span data-ttu-id="23751-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="23751-137">System.Boolean</span></span>

## <span data-ttu-id="23751-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23751-138">NOTES</span></span>

## <span data-ttu-id="23751-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23751-139">RELATED LINKS</span></span>
