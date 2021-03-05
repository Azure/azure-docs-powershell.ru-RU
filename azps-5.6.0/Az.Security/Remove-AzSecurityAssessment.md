---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: ff69cd6296dbd95f959beb48fef6e496866e54f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011688"
---
# <span data-ttu-id="5a8ac-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="5a8ac-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="5a8ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5a8ac-103">Удаляет результаты оценки безопасности из подписки.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="5a8ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a8ac-104">SYNTAX</span></span>

### <span data-ttu-id="5a8ac-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a8ac-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a8ac-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="5a8ac-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a8ac-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a8ac-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a8ac-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a8ac-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a8ac-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a8ac-109">DESCRIPTION</span></span>
<span data-ttu-id="5a8ac-110">Удаляет результаты оценки безопасности из подписки, обычно используемой при удалении реорента или когда оценка больше не релевантна для определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="5a8ac-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a8ac-111">EXAMPLES</span></span>

### <span data-ttu-id="5a8ac-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a8ac-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="5a8ac-113">Удаление результатов оценки в подписке</span><span class="sxs-lookup"><span data-stu-id="5a8ac-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="5a8ac-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a8ac-114">PARAMETERS</span></span>

### <span data-ttu-id="5a8ac-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="5a8ac-115">-AssessedResourceId</span></span>
<span data-ttu-id="5a8ac-116">Полный ИД ресурса, на основе который вычисляется оценка.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a8ac-117">-DefaultProfile</span></span>
<span data-ttu-id="5a8ac-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a8ac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a8ac-119">-InputObject</span></span>
<span data-ttu-id="5a8ac-120">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8ac-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5a8ac-121">-Name</span></span>
<span data-ttu-id="5a8ac-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8ac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a8ac-123">-PassThru</span></span>
<span data-ttu-id="5a8ac-124">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5a8ac-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a8ac-125">-ResourceId</span></span>
<span data-ttu-id="5a8ac-126">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5a8ac-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a8ac-127">-Confirm</span></span>
<span data-ttu-id="5a8ac-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a8ac-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a8ac-129">-WhatIf</span></span>
<span data-ttu-id="5a8ac-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a8ac-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a8ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a8ac-132">CommonParameters</span></span>
<span data-ttu-id="5a8ac-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a8ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a8ac-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a8ac-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a8ac-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a8ac-135">INPUTS</span></span>

### <span data-ttu-id="5a8ac-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5a8ac-136">System.String</span></span>

### <span data-ttu-id="5a8ac-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="5a8ac-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="5a8ac-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a8ac-138">OUTPUTS</span></span>

### <span data-ttu-id="5a8ac-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a8ac-139">System.Boolean</span></span>

## <span data-ttu-id="5a8ac-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a8ac-140">NOTES</span></span>

## <span data-ttu-id="5a8ac-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a8ac-141">RELATED LINKS</span></span>
