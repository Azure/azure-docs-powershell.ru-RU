---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078063"
---
# <span data-ttu-id="dd734-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="dd734-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="dd734-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd734-102">SYNOPSIS</span></span>
<span data-ttu-id="dd734-103">Добавляет пользователя в существующую группу AD.</span><span class="sxs-lookup"><span data-stu-id="dd734-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="dd734-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd734-104">SYNTAX</span></span>

### <span data-ttu-id="dd734-105">MemberObjectIdWithGroupObjectId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd734-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd734-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="dd734-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd734-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="dd734-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd734-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd734-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd734-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd734-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd734-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd734-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd734-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd734-111">DESCRIPTION</span></span>
<span data-ttu-id="dd734-112">Добавляет пользователя в существующую группу AD.</span><span class="sxs-lookup"><span data-stu-id="dd734-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="dd734-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd734-113">EXAMPLES</span></span>

### <span data-ttu-id="dd734-114">Пример 1: Добавление пользователя в группу по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="dd734-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="dd734-115">Добавляет пользователя с идентификатором объекта "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" в группу с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="dd734-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="dd734-116">Пример 2: Добавление пользователя в группу с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="dd734-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="dd734-117">Получает группу с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE" и добавляет ее в командлет Add-AzADGroupMember, чтобы добавить пользователя в эту группу.</span><span class="sxs-lookup"><span data-stu-id="dd734-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="dd734-118">Пример 3: Добавление пользователя в группу по имени участника</span><span class="sxs-lookup"><span data-stu-id="dd734-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="dd734-119">Добавляет пользователя в группу и выдает список участников группы.</span><span class="sxs-lookup"><span data-stu-id="dd734-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="dd734-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd734-120">PARAMETERS</span></span>

### <span data-ttu-id="dd734-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd734-121">-DefaultProfile</span></span>
<span data-ttu-id="dd734-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd734-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd734-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="dd734-123">-MemberObjectId</span></span>
<span data-ttu-id="dd734-124">Идентификатор объекта для элемента.</span><span class="sxs-lookup"><span data-stu-id="dd734-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd734-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="dd734-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="dd734-126">UPN участника, которого нужно добавить в группу.</span><span class="sxs-lookup"><span data-stu-id="dd734-126">The UPN of the member(s) to add to the group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd734-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd734-127">-PassThru</span></span>
<span data-ttu-id="dd734-128">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dd734-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="dd734-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="dd734-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="dd734-130">Отображаемое имя группы, в которую нужно добавить участника (-ей).</span><span class="sxs-lookup"><span data-stu-id="dd734-130">The display name of the group to add the member(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd734-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="dd734-131">-TargetGroupObject</span></span>
<span data-ttu-id="dd734-132">Объектное представление группы, в которую нужно добавить членов.</span><span class="sxs-lookup"><span data-stu-id="dd734-132">The object representation of the group to add the member(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd734-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="dd734-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="dd734-134">Идентификатор объекта группы, в которую нужно добавить участника (-ей).</span><span class="sxs-lookup"><span data-stu-id="dd734-134">The object id of the group to add the member(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd734-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd734-135">-Confirm</span></span>
<span data-ttu-id="dd734-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd734-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd734-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd734-137">-WhatIf</span></span>
<span data-ttu-id="dd734-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd734-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd734-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd734-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd734-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd734-140">CommonParameters</span></span>
<span data-ttu-id="dd734-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd734-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd734-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd734-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd734-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd734-143">INPUTS</span></span>

### <span data-ttu-id="dd734-144">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="dd734-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="dd734-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd734-145">OUTPUTS</span></span>

### <span data-ttu-id="dd734-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd734-146">System.Boolean</span></span>

## <span data-ttu-id="dd734-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd734-147">NOTES</span></span>

## <span data-ttu-id="dd734-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd734-148">RELATED LINKS</span></span>
