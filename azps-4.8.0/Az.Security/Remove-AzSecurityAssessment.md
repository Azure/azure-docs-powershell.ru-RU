---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243970"
---
# <span data-ttu-id="8bb44-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="8bb44-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="8bb44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bb44-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb44-103">Удаление результата оценки безопасности из подписки.</span><span class="sxs-lookup"><span data-stu-id="8bb44-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="8bb44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bb44-104">SYNTAX</span></span>

### <span data-ttu-id="8bb44-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bb44-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bb44-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="8bb44-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bb44-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bb44-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bb44-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="8bb44-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bb44-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bb44-109">DESCRIPTION</span></span>
<span data-ttu-id="8bb44-110">Удаление результата оценки безопасности из подписки (обычно используется при удалении resoruce или когда оценка более несущественна для определенного ресурса)</span><span class="sxs-lookup"><span data-stu-id="8bb44-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="8bb44-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bb44-111">EXAMPLES</span></span>

### <span data-ttu-id="8bb44-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8bb44-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="8bb44-113">Удаление результата оценки подписки</span><span class="sxs-lookup"><span data-stu-id="8bb44-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="8bb44-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bb44-114">PARAMETERS</span></span>

### <span data-ttu-id="8bb44-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="8bb44-115">-AssessedResourceId</span></span>
<span data-ttu-id="8bb44-116">Полный идентификатор ресурса, для которого рассчитывается оценка.</span><span class="sxs-lookup"><span data-stu-id="8bb44-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="8bb44-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb44-117">-DefaultProfile</span></span>
<span data-ttu-id="8bb44-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb44-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bb44-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bb44-119">-InputObject</span></span>
<span data-ttu-id="8bb44-120">Объект input.</span><span class="sxs-lookup"><span data-stu-id="8bb44-120">Input Object.</span></span>

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

### <span data-ttu-id="8bb44-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8bb44-121">-Name</span></span>
<span data-ttu-id="8bb44-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="8bb44-122">Resource name.</span></span>

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

### <span data-ttu-id="8bb44-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bb44-123">-PassThru</span></span>
<span data-ttu-id="8bb44-124">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8bb44-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="8bb44-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bb44-125">-ResourceId</span></span>
<span data-ttu-id="8bb44-126">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="8bb44-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="8bb44-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bb44-127">-Confirm</span></span>
<span data-ttu-id="8bb44-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8bb44-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bb44-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bb44-129">-WhatIf</span></span>
<span data-ttu-id="8bb44-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8bb44-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bb44-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8bb44-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bb44-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb44-132">CommonParameters</span></span>
<span data-ttu-id="8bb44-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bb44-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb44-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bb44-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb44-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bb44-135">INPUTS</span></span>

### <span data-ttu-id="8bb44-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8bb44-136">System.String</span></span>

### <span data-ttu-id="8bb44-137">Microsoft. Azure. Commands. Security. Models. оценивающие. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="8bb44-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="8bb44-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bb44-138">OUTPUTS</span></span>

### <span data-ttu-id="8bb44-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8bb44-139">System.Boolean</span></span>

## <span data-ttu-id="8bb44-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bb44-140">NOTES</span></span>

## <span data-ttu-id="8bb44-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bb44-141">RELATED LINKS</span></span>
