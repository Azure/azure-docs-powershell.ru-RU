---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: acf97f282e50d9c6f468e400cb2a5c598fe06659
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997128"
---
# <span data-ttu-id="4e440-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="4e440-101">Update-AzTag</span></span>

## <span data-ttu-id="4e440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e440-102">SYNOPSIS</span></span>

<span data-ttu-id="4e440-103">Выборочно обновляет набор тегов для ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="4e440-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="4e440-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e440-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOperation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="4e440-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e440-105">DESCRIPTION</span></span>

<span data-ttu-id="4e440-106">Командлет **Update-AzTag** с **кодом ResourceId** выборочно обновляет набор тегов для ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="4e440-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="4e440-107">Эта операция позволяет заменить, слияние или выборочно удалить теги для указанного ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="4e440-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="4e440-108">В конце операции у указанной сущности может быть не более 50 тегов.</span><span class="sxs-lookup"><span data-stu-id="4e440-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="4e440-109">Параметр "Заменить" заменяет весь набор существующих тегов новым.</span><span class="sxs-lookup"><span data-stu-id="4e440-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="4e440-110">Параметр "слияние" позволяет добавлять теги с новыми именами и обновлять значения тегов с существующими именами.</span><span class="sxs-lookup"><span data-stu-id="4e440-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="4e440-111">Параметр "Удалить" позволяет выборочно удалять теги на основе заданных имен или пар имен и значений.</span><span class="sxs-lookup"><span data-stu-id="4e440-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="4e440-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e440-112">EXAMPLES</span></span>

### <span data-ttu-id="4e440-113">Пример 1. Выборочно обновляет набор тегов для подписки с помощью операции слияния</span><span class="sxs-lookup"><span data-stu-id="4e440-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

<span data-ttu-id="4e440-114">Эта команда объединяет набор тегов подписки с {subId}.</span><span class="sxs-lookup"><span data-stu-id="4e440-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="4e440-115">Пример 2. Выборочно обновляет набор тегов для подписки с помощью операции "Заменить"</span><span class="sxs-lookup"><span data-stu-id="4e440-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

<span data-ttu-id="4e440-116">Эта команда повторно передает набор тегов для подписки {subId}.</span><span class="sxs-lookup"><span data-stu-id="4e440-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="4e440-117">Пример 3. Выборочно обновляет набор тегов в подписке с помощью операции "Удалить"</span><span class="sxs-lookup"><span data-stu-id="4e440-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

<span data-ttu-id="4e440-118">Эта команда удаляет набор тегов для подписки с {subId}.</span><span class="sxs-lookup"><span data-stu-id="4e440-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="4e440-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e440-119">PARAMETERS</span></span>

### <span data-ttu-id="4e440-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e440-120">-DefaultProfile</span></span>
<span data-ttu-id="4e440-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e440-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e440-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e440-122">-ResourceId</span></span>
<span data-ttu-id="4e440-123">Идентификатор ресурса для сущности с тегами.</span><span class="sxs-lookup"><span data-stu-id="4e440-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="4e440-124">Ресурс, группа ресурсов или подписка могут быть помечены тегами.</span><span class="sxs-lookup"><span data-stu-id="4e440-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e440-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e440-125">-Tag</span></span>
<span data-ttu-id="4e440-126">Набор тегов, которые нужно использовать для обновления.</span><span class="sxs-lookup"><span data-stu-id="4e440-126">The set of tags to use for update.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e440-127">-Operation</span><span class="sxs-lookup"><span data-stu-id="4e440-127">-Operation</span></span>
<span data-ttu-id="4e440-128">Операция обновления.</span><span class="sxs-lookup"><span data-stu-id="4e440-128">The update operation.</span></span> <span data-ttu-id="4e440-129">Доступны такие варианты: "Слияние", "Заменить" и "Удалить".</span><span class="sxs-lookup"><span data-stu-id="4e440-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOperation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e440-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e440-130">-Confirm</span></span>
<span data-ttu-id="4e440-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e440-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e440-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e440-132">-WhatIf</span></span>
<span data-ttu-id="4e440-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e440-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e440-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e440-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e440-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e440-135">CommonParameters</span></span>
<span data-ttu-id="4e440-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e440-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e440-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e440-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e440-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e440-138">INPUTS</span></span>

### <span data-ttu-id="4e440-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4e440-139">System.String</span></span>

### <span data-ttu-id="4e440-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span><span class="sxs-lookup"><span data-stu-id="4e440-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span></span>

### <span data-ttu-id="4e440-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4e440-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4e440-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e440-142">OUTPUTS</span></span>

### <span data-ttu-id="4e440-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="4e440-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="4e440-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e440-144">NOTES</span></span>

## <span data-ttu-id="4e440-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e440-145">RELATED LINKS</span></span>

[<span data-ttu-id="4e440-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="4e440-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="4e440-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="4e440-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="4e440-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="4e440-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
