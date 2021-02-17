---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 984b5ef9a1ff19142ef044e1f3c919f8fb2a3dce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212969"
---
# <span data-ttu-id="9b6ab-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="9b6ab-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="9b6ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6ab-103">Список участников группы AD в текущем клиенте.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="9b6ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b6ab-104">SYNTAX</span></span>

### <span data-ttu-id="9b6ab-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b6ab-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9b6ab-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b6ab-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9b6ab-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b6ab-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="9b6ab-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b6ab-108">DESCRIPTION</span></span>
<span data-ttu-id="9b6ab-109">Список участников группы AD в текущем клиенте.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="9b6ab-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b6ab-110">EXAMPLES</span></span>

### <span data-ttu-id="9b6ab-111">Пример 1. Список участников по ИД объекта группы AD</span><span class="sxs-lookup"><span data-stu-id="9b6ab-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="9b6ab-112">Список участников группы AD с ид объекта '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="9b6ab-113">Пример 2. Список участников по ИД объекта группы AD с помощью разведки</span><span class="sxs-lookup"><span data-stu-id="9b6ab-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="9b6ab-114">Список первых 100 участников группы AD с ид объекта '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="9b6ab-115">Пример 3. Состав списка путем прокайки</span><span class="sxs-lookup"><span data-stu-id="9b6ab-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="9b6ab-116">Получает группу AD с ид объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE" и передает ее в Get-AzADGroupMember-Get-AzADGroupMember для списка всех участников этой группы.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="9b6ab-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b6ab-117">PARAMETERS</span></span>

### <span data-ttu-id="9b6ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6ab-118">-DefaultProfile</span></span>
<span data-ttu-id="9b6ab-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9b6ab-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b6ab-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="9b6ab-120">-GroupDisplayName</span></span>
<span data-ttu-id="9b6ab-121">Отображаемая группа.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-121">The display name of the group.</span></span>

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

### <span data-ttu-id="9b6ab-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="9b6ab-122">-GroupObject</span></span>
<span data-ttu-id="9b6ab-123">Объект группы, из который вы перечисляете участников.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-123">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="9b6ab-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="9b6ab-124">-GroupObjectId</span></span>
<span data-ttu-id="9b6ab-125">ИД объекта группы.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-125">Object Id of the group.</span></span>

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

### <span data-ttu-id="9b6ab-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="9b6ab-126">-IncludeTotalCount</span></span>
<span data-ttu-id="9b6ab-127">Отчет о количестве объектов в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="9b6ab-128">В настоящее время этот параметр не имеет никакого отношения.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="9b6ab-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="9b6ab-129">-Skip</span></span>
<span data-ttu-id="9b6ab-130">Игнорирует первые N объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="9b6ab-131">-First</span><span class="sxs-lookup"><span data-stu-id="9b6ab-131">-First</span></span>
<span data-ttu-id="9b6ab-132">Максимальное количество возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="9b6ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6ab-133">CommonParameters</span></span>
<span data-ttu-id="9b6ab-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6ab-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b6ab-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6ab-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b6ab-136">INPUTS</span></span>

### <span data-ttu-id="9b6ab-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9b6ab-137">System.String</span></span>

### <span data-ttu-id="9b6ab-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="9b6ab-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="9b6ab-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b6ab-139">OUTPUTS</span></span>

### <span data-ttu-id="9b6ab-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span><span class="sxs-lookup"><span data-stu-id="9b6ab-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="9b6ab-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b6ab-141">NOTES</span></span>

## <span data-ttu-id="9b6ab-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b6ab-142">RELATED LINKS</span></span>

[<span data-ttu-id="9b6ab-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9b6ab-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="9b6ab-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9b6ab-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

