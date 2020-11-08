---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243967"
---
# <span data-ttu-id="a8642-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="a8642-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="a8642-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8642-102">SYNOPSIS</span></span>
<span data-ttu-id="a8642-103">Удаление метаданных оценки безопасности из подписки.</span><span class="sxs-lookup"><span data-stu-id="a8642-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="a8642-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8642-104">SYNTAX</span></span>

### <span data-ttu-id="a8642-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8642-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8642-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8642-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8642-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a8642-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8642-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8642-108">DESCRIPTION</span></span>
<span data-ttu-id="a8642-109">Удаление метаданных оценки безопасности из подписки.</span><span class="sxs-lookup"><span data-stu-id="a8642-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="a8642-110">Это действие удалит тип оценки и все необходимые результаты оценки подписки.</span><span class="sxs-lookup"><span data-stu-id="a8642-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="a8642-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8642-111">EXAMPLES</span></span>

### <span data-ttu-id="a8642-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a8642-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="a8642-113">Удаление типа оценки из подписки</span><span class="sxs-lookup"><span data-stu-id="a8642-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="a8642-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8642-114">PARAMETERS</span></span>

### <span data-ttu-id="a8642-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8642-115">-DefaultProfile</span></span>
<span data-ttu-id="a8642-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8642-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8642-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8642-117">-InputObject</span></span>
<span data-ttu-id="a8642-118">Объект input.</span><span class="sxs-lookup"><span data-stu-id="a8642-118">Input Object.</span></span>

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

### <span data-ttu-id="a8642-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a8642-119">-Name</span></span>
<span data-ttu-id="a8642-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a8642-120">Resource name.</span></span>

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

### <span data-ttu-id="a8642-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8642-121">-PassThru</span></span>
<span data-ttu-id="a8642-122">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a8642-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a8642-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8642-123">-ResourceId</span></span>
<span data-ttu-id="a8642-124">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="a8642-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a8642-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8642-125">-Confirm</span></span>
<span data-ttu-id="a8642-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a8642-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8642-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8642-127">-WhatIf</span></span>
<span data-ttu-id="a8642-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a8642-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8642-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a8642-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8642-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8642-130">CommonParameters</span></span>
<span data-ttu-id="a8642-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8642-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8642-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8642-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8642-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8642-133">INPUTS</span></span>

### <span data-ttu-id="a8642-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a8642-134">System.String</span></span>

### <span data-ttu-id="a8642-135">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="a8642-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="a8642-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8642-136">OUTPUTS</span></span>

### <span data-ttu-id="a8642-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8642-137">System.Boolean</span></span>

## <span data-ttu-id="a8642-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8642-138">NOTES</span></span>

## <span data-ttu-id="a8642-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8642-139">RELATED LINKS</span></span>
