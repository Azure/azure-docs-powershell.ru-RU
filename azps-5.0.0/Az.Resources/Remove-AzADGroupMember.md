---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7450588905deeb900efbffffa253f5c06ae63272
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245885"
---
# <span data-ttu-id="9bd15-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="9bd15-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="9bd15-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bd15-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd15-103">Удаление пользователя из группы AD.</span><span class="sxs-lookup"><span data-stu-id="9bd15-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="9bd15-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bd15-104">SYNTAX</span></span>

### <span data-ttu-id="9bd15-105">ExplicitParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9bd15-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bd15-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="9bd15-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bd15-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="9bd15-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bd15-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="9bd15-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bd15-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd15-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bd15-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd15-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bd15-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd15-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bd15-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bd15-112">DESCRIPTION</span></span>
<span data-ttu-id="9bd15-113">Удаление пользователя из группы AD.</span><span class="sxs-lookup"><span data-stu-id="9bd15-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="9bd15-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bd15-114">EXAMPLES</span></span>

### <span data-ttu-id="9bd15-115">Пример 1: Удаление пользователя из группы по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="9bd15-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="9bd15-116">Удаляет пользователя с идентификатором объекта "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" из группы с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="9bd15-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="9bd15-117">Пример 2: Удаление пользователя из группы с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="9bd15-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="9bd15-118">Получает группу с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE" и добавляет ее в командлет Remove-AzADGroupMember, чтобы удалить пользователя в эту группу.</span><span class="sxs-lookup"><span data-stu-id="9bd15-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="9bd15-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bd15-119">PARAMETERS</span></span>

### <span data-ttu-id="9bd15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd15-120">-DefaultProfile</span></span>
<span data-ttu-id="9bd15-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd15-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd15-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="9bd15-122">-GroupDisplayName</span></span>
<span data-ttu-id="9bd15-123">Отображаемое имя группы, из которой нужно удалить участника (-ей).</span><span class="sxs-lookup"><span data-stu-id="9bd15-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="9bd15-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="9bd15-124">-GroupObject</span></span>
<span data-ttu-id="9bd15-125">Объектное представление группы, из которой нужно удалить участника.</span><span class="sxs-lookup"><span data-stu-id="9bd15-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="9bd15-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="9bd15-126">-GroupObjectId</span></span>
<span data-ttu-id="9bd15-127">Идентификатор объекта группы, из которой нужно удалить участника.</span><span class="sxs-lookup"><span data-stu-id="9bd15-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="9bd15-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="9bd15-128">-MemberObjectId</span></span>
<span data-ttu-id="9bd15-129">Идентификатор объекта для элемента.</span><span class="sxs-lookup"><span data-stu-id="9bd15-129">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd15-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9bd15-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="9bd15-131">UPN участника, которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9bd15-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="9bd15-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bd15-132">-PassThru</span></span>
<span data-ttu-id="9bd15-133">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9bd15-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9bd15-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bd15-134">-Confirm</span></span>
<span data-ttu-id="9bd15-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9bd15-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd15-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd15-136">-WhatIf</span></span>
<span data-ttu-id="9bd15-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9bd15-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bd15-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9bd15-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bd15-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd15-139">CommonParameters</span></span>
<span data-ttu-id="9bd15-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bd15-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd15-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bd15-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd15-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bd15-142">INPUTS</span></span>

### <span data-ttu-id="9bd15-143">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="9bd15-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="9bd15-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bd15-144">OUTPUTS</span></span>

### <span data-ttu-id="9bd15-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bd15-145">System.Boolean</span></span>

## <span data-ttu-id="9bd15-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bd15-146">NOTES</span></span>

## <span data-ttu-id="9bd15-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bd15-147">RELATED LINKS</span></span>
