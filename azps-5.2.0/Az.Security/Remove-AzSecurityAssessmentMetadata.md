---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391460"
---
# <span data-ttu-id="f3187-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="f3187-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="f3187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3187-102">SYNOPSIS</span></span>
<span data-ttu-id="f3187-103">Удаляет метаданные оценки безопасности из подписки.</span><span class="sxs-lookup"><span data-stu-id="f3187-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="f3187-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3187-104">SYNTAX</span></span>

### <span data-ttu-id="f3187-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3187-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3187-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3187-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3187-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f3187-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3187-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3187-108">DESCRIPTION</span></span>
<span data-ttu-id="f3187-109">Удаляет метаданные оценки безопасности из подписки.</span><span class="sxs-lookup"><span data-stu-id="f3187-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="f3187-110">Это действие удалит тип оценки и все соответствующие результаты оценки из подписки.</span><span class="sxs-lookup"><span data-stu-id="f3187-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="f3187-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3187-111">EXAMPLES</span></span>

### <span data-ttu-id="f3187-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3187-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="f3187-113">Удаление типа оценки из подписки</span><span class="sxs-lookup"><span data-stu-id="f3187-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="f3187-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3187-114">PARAMETERS</span></span>

### <span data-ttu-id="f3187-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3187-115">-DefaultProfile</span></span>
<span data-ttu-id="f3187-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3187-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3187-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3187-117">-InputObject</span></span>
<span data-ttu-id="f3187-118">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="f3187-118">Input Object.</span></span>

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

### <span data-ttu-id="f3187-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f3187-119">-Name</span></span>
<span data-ttu-id="f3187-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f3187-120">Resource name.</span></span>

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

### <span data-ttu-id="f3187-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3187-121">-PassThru</span></span>
<span data-ttu-id="f3187-122">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="f3187-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="f3187-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3187-123">-ResourceId</span></span>
<span data-ttu-id="f3187-124">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="f3187-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f3187-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3187-125">-Confirm</span></span>
<span data-ttu-id="f3187-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3187-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3187-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3187-127">-WhatIf</span></span>
<span data-ttu-id="f3187-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3187-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3187-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f3187-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3187-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3187-130">CommonParameters</span></span>
<span data-ttu-id="f3187-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3187-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3187-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3187-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3187-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3187-133">INPUTS</span></span>

### <span data-ttu-id="f3187-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f3187-134">System.String</span></span>

### <span data-ttu-id="f3187-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="f3187-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="f3187-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3187-136">OUTPUTS</span></span>

### <span data-ttu-id="f3187-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3187-137">System.Boolean</span></span>

## <span data-ttu-id="f3187-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3187-138">NOTES</span></span>

## <span data-ttu-id="f3187-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3187-139">RELATED LINKS</span></span>
