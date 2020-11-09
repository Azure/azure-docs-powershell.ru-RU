---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: df34b529a64e1c773c95a5234fd995944e8caac8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316307"
---
# <span data-ttu-id="d3701-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="d3701-101">Update-AzTag</span></span>

## <span data-ttu-id="d3701-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3701-102">SYNOPSIS</span></span>

<span data-ttu-id="d3701-103">Выборочно обновляет набор тегов на ресурсе или в подписке.</span><span class="sxs-lookup"><span data-stu-id="d3701-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="d3701-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3701-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="d3701-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3701-105">DESCRIPTION</span></span>

<span data-ttu-id="d3701-106">Командлет **Update-AzTag** с **ResourceId** , который выборочно обновляет набор тегов на ресурсе или подписке.</span><span class="sxs-lookup"><span data-stu-id="d3701-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="d3701-107">Эта операция позволяет заменять, объединять или выборочно удалять теги в указанном ресурсе или подписке.</span><span class="sxs-lookup"><span data-stu-id="d3701-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="d3701-108">В конце операции для указанной сущности может быть не более 50 тегов.</span><span class="sxs-lookup"><span data-stu-id="d3701-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="d3701-109">Параметр "заменить" заменяет весь набор существующих тегов новым набором.</span><span class="sxs-lookup"><span data-stu-id="d3701-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="d3701-110">С помощью параметра "слияние" можно добавлять теги с новыми именами и обновлять значения тегов с существующими именами.</span><span class="sxs-lookup"><span data-stu-id="d3701-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="d3701-111">Параметр "Удалить" позволяет выборочно удалять теги, основанные на указанных именах или парах "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="d3701-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="d3701-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3701-112">EXAMPLES</span></span>

### <span data-ttu-id="d3701-113">Пример 1: выборочное обновление набора тегов в подписке с помощью операции "слияние"</span><span class="sxs-lookup"><span data-stu-id="d3701-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

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

<span data-ttu-id="d3701-114">Эта команда объединяет набор тегов в подписке с помощью {subId}.</span><span class="sxs-lookup"><span data-stu-id="d3701-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="d3701-115">Пример 2: выборочное обновление набора тегов в подписке с помощью операции "заменить"</span><span class="sxs-lookup"><span data-stu-id="d3701-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

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

<span data-ttu-id="d3701-116">Эта команда Repalces набор тегов в подписке с помощью {subId}.</span><span class="sxs-lookup"><span data-stu-id="d3701-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="d3701-117">Пример 3: выборочное обновление набора тегов в подписке с помощью операции "Удалить"</span><span class="sxs-lookup"><span data-stu-id="d3701-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

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

<span data-ttu-id="d3701-118">Эта команда удаляет набор тегов в подписке с помощью {subId}.</span><span class="sxs-lookup"><span data-stu-id="d3701-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="d3701-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3701-119">PARAMETERS</span></span>

### <span data-ttu-id="d3701-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3701-120">-DefaultProfile</span></span>
<span data-ttu-id="d3701-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3701-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3701-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3701-122">-ResourceId</span></span>
<span data-ttu-id="d3701-123">Идентификатор ресурса для помеченной сущности.</span><span class="sxs-lookup"><span data-stu-id="d3701-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="d3701-124">Ресурс, Группа ресурсов или подписка может быть помечены.</span><span class="sxs-lookup"><span data-stu-id="d3701-124">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="d3701-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="d3701-125">-Tag</span></span>
<span data-ttu-id="d3701-126">Набор тегов, которые нужно использовать для обновления.</span><span class="sxs-lookup"><span data-stu-id="d3701-126">The set of tags to use for update.</span></span>

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

### <span data-ttu-id="d3701-127">-Эксплуатация</span><span class="sxs-lookup"><span data-stu-id="d3701-127">-Operation</span></span>
<span data-ttu-id="d3701-128">Операция обновления.</span><span class="sxs-lookup"><span data-stu-id="d3701-128">The update operation.</span></span> <span data-ttu-id="d3701-129">Параметры можно объединять, заменять и удалять.</span><span class="sxs-lookup"><span data-stu-id="d3701-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3701-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3701-130">-Confirm</span></span>
<span data-ttu-id="d3701-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d3701-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3701-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3701-132">-WhatIf</span></span>
<span data-ttu-id="d3701-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d3701-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3701-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d3701-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3701-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3701-135">CommonParameters</span></span>
<span data-ttu-id="d3701-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3701-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3701-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3701-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3701-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3701-138">INPUTS</span></span>

### <span data-ttu-id="d3701-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d3701-139">System.String</span></span>

### <span data-ttu-id="d3701-140">Microsoft. Azure. Commands. Tags. Model. TagPatchOpeation</span><span class="sxs-lookup"><span data-stu-id="d3701-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation</span></span>

### <span data-ttu-id="d3701-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d3701-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d3701-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3701-142">OUTPUTS</span></span>

### <span data-ttu-id="d3701-143">Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="d3701-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="d3701-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3701-144">NOTES</span></span>

## <span data-ttu-id="d3701-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3701-145">RELATED LINKS</span></span>

[<span data-ttu-id="d3701-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="d3701-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="d3701-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="d3701-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="d3701-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="d3701-148">Remove-AzTag</span></span>](./Remove-AzTag.md)