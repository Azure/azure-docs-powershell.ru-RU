---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
ms.openlocfilehash: 515591660abf34399caa5643c05478fd4295141a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732452"
---
# <span data-ttu-id="aba0e-101">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="aba0e-101">Remove-AzureRmADGroupMember</span></span>

## <span data-ttu-id="aba0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aba0e-102">SYNOPSIS</span></span>
<span data-ttu-id="aba0e-103">Удаление пользователя из группы AD.</span><span class="sxs-lookup"><span data-stu-id="aba0e-103">Removes a user from an AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aba0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aba0e-104">SYNTAX</span></span>

### <span data-ttu-id="aba0e-105">ExplicitParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aba0e-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzureRmADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aba0e-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="aba0e-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba0e-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="aba0e-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba0e-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="aba0e-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba0e-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aba0e-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba0e-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aba0e-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba0e-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aba0e-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aba0e-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aba0e-112">DESCRIPTION</span></span>
<span data-ttu-id="aba0e-113">Удаление пользователя из группы AD.</span><span class="sxs-lookup"><span data-stu-id="aba0e-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="aba0e-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aba0e-114">EXAMPLES</span></span>

### <span data-ttu-id="aba0e-115">Пример 1: Удаление пользователя из группы по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="aba0e-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="aba0e-116">Удаляет пользователя с идентификатором объекта "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" из группы с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="aba0e-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="aba0e-117">Пример 2: Удаление пользователя из группы с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="aba0e-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="aba0e-118">Получает группу с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE" и добавляет ее в командлет Remove-AzureRmADGroupMember, чтобы удалить пользователя в эту группу.</span><span class="sxs-lookup"><span data-stu-id="aba0e-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzureRmADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="aba0e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aba0e-119">PARAMETERS</span></span>

### <span data-ttu-id="aba0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba0e-120">-DefaultProfile</span></span>
<span data-ttu-id="aba0e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aba0e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba0e-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="aba0e-122">-GroupDisplayName</span></span>
<span data-ttu-id="aba0e-123">Отображаемое имя группы, из которой нужно удалить участника (-ей).</span><span class="sxs-lookup"><span data-stu-id="aba0e-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="aba0e-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="aba0e-124">-GroupObject</span></span>
<span data-ttu-id="aba0e-125">Объектное представление группы, из которой нужно удалить участника.</span><span class="sxs-lookup"><span data-stu-id="aba0e-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aba0e-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="aba0e-126">-GroupObjectId</span></span>
<span data-ttu-id="aba0e-127">Идентификатор объекта группы, из которой нужно удалить участника.</span><span class="sxs-lookup"><span data-stu-id="aba0e-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba0e-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="aba0e-128">-MemberObjectId</span></span>
<span data-ttu-id="aba0e-129">Идентификатор объекта для элемента.</span><span class="sxs-lookup"><span data-stu-id="aba0e-129">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba0e-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="aba0e-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="aba0e-131">UPN участника, которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="aba0e-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="aba0e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aba0e-132">-PassThru</span></span>
<span data-ttu-id="aba0e-133">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="aba0e-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="aba0e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aba0e-134">-Confirm</span></span>
<span data-ttu-id="aba0e-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aba0e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aba0e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aba0e-136">-WhatIf</span></span>
<span data-ttu-id="aba0e-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aba0e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aba0e-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aba0e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aba0e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba0e-139">CommonParameters</span></span>
<span data-ttu-id="aba0e-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aba0e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba0e-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba0e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba0e-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aba0e-142">INPUTS</span></span>

### <span data-ttu-id="aba0e-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="aba0e-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="aba0e-144">Параметры: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aba0e-144">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="aba0e-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aba0e-145">OUTPUTS</span></span>

### <span data-ttu-id="aba0e-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aba0e-146">System.Boolean</span></span>

## <span data-ttu-id="aba0e-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="aba0e-147">NOTES</span></span>

## <span data-ttu-id="aba0e-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aba0e-148">RELATED LINKS</span></span>
