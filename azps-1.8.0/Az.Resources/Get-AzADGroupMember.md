---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 25de035b853d1a17ee06a7efb6ac31631bd466f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729453"
---
# <span data-ttu-id="f3301-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="f3301-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="f3301-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3301-102">SYNOPSIS</span></span>
<span data-ttu-id="f3301-103">Список участников группы БАННЕРов в текущем клиенте.</span><span class="sxs-lookup"><span data-stu-id="f3301-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="f3301-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3301-104">SYNTAX</span></span>

### <span data-ttu-id="f3301-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3301-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f3301-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3301-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f3301-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3301-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="f3301-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3301-108">DESCRIPTION</span></span>
<span data-ttu-id="f3301-109">Список участников группы БАННЕРов в текущем клиенте.</span><span class="sxs-lookup"><span data-stu-id="f3301-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="f3301-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3301-110">EXAMPLES</span></span>

### <span data-ttu-id="f3301-111">Пример 1: члены списка по идентификатору объекта группы рекламы</span><span class="sxs-lookup"><span data-stu-id="f3301-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="f3301-112">Список участников группы Active Directory с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="f3301-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="f3301-113">Пример 2: члены списка по идентификатору объекта группы Active Directory с помощью разбиения по страницам</span><span class="sxs-lookup"><span data-stu-id="f3301-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="f3301-114">Список первых 100 участников группы Active Directory с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="f3301-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="f3301-115">Пример 3: список членов по конвейеру</span><span class="sxs-lookup"><span data-stu-id="f3301-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="f3301-116">Получает группу БАННЕРов с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE" и добавляет ее в командлет Get-AzADGroupMember, чтобы вывести список всех участников этой группы.</span><span class="sxs-lookup"><span data-stu-id="f3301-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="f3301-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3301-117">PARAMETERS</span></span>

### <span data-ttu-id="f3301-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3301-118">-DefaultProfile</span></span>
<span data-ttu-id="f3301-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f3301-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3301-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="f3301-120">-GroupDisplayName</span></span>
<span data-ttu-id="f3301-121">Отображаемое имя группы.</span><span class="sxs-lookup"><span data-stu-id="f3301-121">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3301-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="f3301-122">-GroupObject</span></span>
<span data-ttu-id="f3301-123">Объект Group, из которого вы перечислите элементы.</span><span class="sxs-lookup"><span data-stu-id="f3301-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3301-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="f3301-124">-GroupObjectId</span></span>
<span data-ttu-id="f3301-125">Идентификатор объекта группы.</span><span class="sxs-lookup"><span data-stu-id="f3301-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3301-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="f3301-126">-IncludeTotalCount</span></span>
<span data-ttu-id="f3301-127">Показывает количество объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="f3301-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="f3301-128">В настоящее время этот параметр не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="f3301-128">Currently, this parameter does nothing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3301-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="f3301-129">-Skip</span></span>
<span data-ttu-id="f3301-130">Пропускает первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="f3301-130">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3301-131">-First</span><span class="sxs-lookup"><span data-stu-id="f3301-131">-First</span></span>
<span data-ttu-id="f3301-132">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="f3301-132">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3301-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3301-133">CommonParameters</span></span>
<span data-ttu-id="f3301-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3301-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3301-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3301-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3301-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3301-136">INPUTS</span></span>

### <span data-ttu-id="f3301-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f3301-137">System.String</span></span>

### <span data-ttu-id="f3301-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="f3301-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="f3301-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3301-139">OUTPUTS</span></span>

### <span data-ttu-id="f3301-140">Microsoft. Azure. Commands. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="f3301-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="f3301-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3301-141">NOTES</span></span>

## <span data-ttu-id="f3301-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3301-142">RELATED LINKS</span></span>

[<span data-ttu-id="f3301-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f3301-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="f3301-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f3301-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

