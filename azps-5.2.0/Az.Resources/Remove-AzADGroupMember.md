---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7450588905deeb900efbffffa253f5c06ae63272
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412500"
---
# <span data-ttu-id="fb355-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="fb355-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="fb355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb355-102">SYNOPSIS</span></span>
<span data-ttu-id="fb355-103">Удаляет пользователя из группы AD.</span><span class="sxs-lookup"><span data-stu-id="fb355-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="fb355-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fb355-104">SYNTAX</span></span>

### <span data-ttu-id="fb355-105">ExplicitParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb355-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb355-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="fb355-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb355-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="fb355-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb355-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="fb355-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb355-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb355-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb355-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb355-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb355-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb355-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb355-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb355-112">DESCRIPTION</span></span>
<span data-ttu-id="fb355-113">Удаляет пользователя из группы AD.</span><span class="sxs-lookup"><span data-stu-id="fb355-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="fb355-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fb355-114">EXAMPLES</span></span>

### <span data-ttu-id="fb355-115">Пример 1. Удаление пользователя из группы по ид объекта</span><span class="sxs-lookup"><span data-stu-id="fb355-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="fb355-116">Удаляет пользователя с ид объекта 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' из группы с ид объекта '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="fb355-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="fb355-117">Пример 2. Удаление пользователя из группы с помощью piping</span><span class="sxs-lookup"><span data-stu-id="fb355-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="fb355-118">Получает группу с ид объекта '85F89C90-780E-4AA6-9F4F-6F268D322EEE' и передает ее в Remove-AzADGroupMember-Remove-AzADGroupMember, чтобы удалить пользователя в эту группу.</span><span class="sxs-lookup"><span data-stu-id="fb355-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="fb355-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb355-119">PARAMETERS</span></span>

### <span data-ttu-id="fb355-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb355-120">-DefaultProfile</span></span>
<span data-ttu-id="fb355-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb355-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb355-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="fb355-122">-GroupDisplayName</span></span>
<span data-ttu-id="fb355-123">Отображаемая группа, из нее удаляются ее члены.</span><span class="sxs-lookup"><span data-stu-id="fb355-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="fb355-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="fb355-124">-GroupObject</span></span>
<span data-ttu-id="fb355-125">Объектное представление группы, из группы для удаления участника.</span><span class="sxs-lookup"><span data-stu-id="fb355-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="fb355-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="fb355-126">-GroupObjectId</span></span>
<span data-ttu-id="fb355-127">Object id of the group to remove the member from.</span><span class="sxs-lookup"><span data-stu-id="fb355-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="fb355-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="fb355-128">-MemberObjectId</span></span>
<span data-ttu-id="fb355-129">ИД объекта участника.</span><span class="sxs-lookup"><span data-stu-id="fb355-129">The object id of the member.</span></span>

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

### <span data-ttu-id="fb355-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fb355-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="fb355-131">UpN участника, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="fb355-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="fb355-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb355-132">-PassThru</span></span>
<span data-ttu-id="fb355-133">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="fb355-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="fb355-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb355-134">-Confirm</span></span>
<span data-ttu-id="fb355-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb355-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb355-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb355-136">-WhatIf</span></span>
<span data-ttu-id="fb355-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb355-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb355-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fb355-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb355-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb355-139">CommonParameters</span></span>
<span data-ttu-id="fb355-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb355-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb355-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb355-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb355-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb355-142">INPUTS</span></span>

### <span data-ttu-id="fb355-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="fb355-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="fb355-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb355-144">OUTPUTS</span></span>

### <span data-ttu-id="fb355-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb355-145">System.Boolean</span></span>

## <span data-ttu-id="fb355-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fb355-146">NOTES</span></span>

## <span data-ttu-id="fb355-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb355-147">RELATED LINKS</span></span>
