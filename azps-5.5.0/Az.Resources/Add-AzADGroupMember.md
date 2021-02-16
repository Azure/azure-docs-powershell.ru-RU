---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226857"
---
# <span data-ttu-id="745eb-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="745eb-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="745eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="745eb-102">SYNOPSIS</span></span>
<span data-ttu-id="745eb-103">Добавляет пользователя в существующую группу AD.</span><span class="sxs-lookup"><span data-stu-id="745eb-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="745eb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="745eb-104">SYNTAX</span></span>

### <span data-ttu-id="745eb-105">MemberObjectIdWithGroupObjectId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="745eb-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="745eb-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="745eb-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="745eb-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="745eb-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="745eb-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="745eb-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="745eb-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="745eb-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="745eb-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="745eb-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="745eb-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="745eb-111">DESCRIPTION</span></span>
<span data-ttu-id="745eb-112">Добавляет пользователя в существующую группу AD.</span><span class="sxs-lookup"><span data-stu-id="745eb-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="745eb-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="745eb-113">EXAMPLES</span></span>

### <span data-ttu-id="745eb-114">Пример 1. Добавление пользователя в группу по ид объекта</span><span class="sxs-lookup"><span data-stu-id="745eb-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="745eb-115">Добавляет пользователя с ид объекта 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' в группу с ид объекта '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="745eb-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="745eb-116">Пример 2. Добавление пользователя в группу путем перенастройки</span><span class="sxs-lookup"><span data-stu-id="745eb-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="745eb-117">Получает группу с ид объекта '85F89C90-780E-4AA6-9F4F-6F268D322EEE' и передает ее в Add-AzADGroupMember-млет, чтобы добавить пользователя в эту группу.</span><span class="sxs-lookup"><span data-stu-id="745eb-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="745eb-118">Пример 3. Добавление пользователя в группу по имени директора</span><span class="sxs-lookup"><span data-stu-id="745eb-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="745eb-119">Добавляет пользователя в группу и перечисляет ее участников.</span><span class="sxs-lookup"><span data-stu-id="745eb-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="745eb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="745eb-120">PARAMETERS</span></span>

### <span data-ttu-id="745eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745eb-121">-DefaultProfile</span></span>
<span data-ttu-id="745eb-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="745eb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="745eb-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="745eb-123">-MemberObjectId</span></span>
<span data-ttu-id="745eb-124">ИД объекта участника.</span><span class="sxs-lookup"><span data-stu-id="745eb-124">The object id of the member.</span></span>

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

### <span data-ttu-id="745eb-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="745eb-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="745eb-126">UpN членов, которые нужно добавить в группу.</span><span class="sxs-lookup"><span data-stu-id="745eb-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="745eb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="745eb-127">-PassThru</span></span>
<span data-ttu-id="745eb-128">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="745eb-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="745eb-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="745eb-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="745eb-130">Отображаемая группа, в которая нужно добавить членов.</span><span class="sxs-lookup"><span data-stu-id="745eb-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="745eb-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="745eb-131">-TargetGroupObject</span></span>
<span data-ttu-id="745eb-132">Объектное представление группы, в которые нужно добавить членов.</span><span class="sxs-lookup"><span data-stu-id="745eb-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="745eb-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="745eb-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="745eb-134">ИД объекта группы, в который нужно добавить ее участника.</span><span class="sxs-lookup"><span data-stu-id="745eb-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="745eb-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="745eb-135">-Confirm</span></span>
<span data-ttu-id="745eb-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="745eb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="745eb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="745eb-137">-WhatIf</span></span>
<span data-ttu-id="745eb-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="745eb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="745eb-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="745eb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="745eb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745eb-140">CommonParameters</span></span>
<span data-ttu-id="745eb-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="745eb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="745eb-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="745eb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745eb-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="745eb-143">INPUTS</span></span>

### <span data-ttu-id="745eb-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="745eb-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="745eb-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="745eb-145">OUTPUTS</span></span>

### <span data-ttu-id="745eb-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="745eb-146">System.Boolean</span></span>

## <span data-ttu-id="745eb-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="745eb-147">NOTES</span></span>

## <span data-ttu-id="745eb-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="745eb-148">RELATED LINKS</span></span>
