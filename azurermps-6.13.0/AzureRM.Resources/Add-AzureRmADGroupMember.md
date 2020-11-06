---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/add-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
ms.openlocfilehash: 333a56a59c28482c2da228e3e9c0f8c2f1c21f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560720"
---
# <span data-ttu-id="352b5-101">Add-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="352b5-101">Add-AzureRmADGroupMember</span></span>

## <span data-ttu-id="352b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="352b5-102">SYNOPSIS</span></span>
<span data-ttu-id="352b5-103">Добавляет пользователя в существующую группу AD.</span><span class="sxs-lookup"><span data-stu-id="352b5-103">Adds a user to an existing AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="352b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="352b5-104">SYNTAX</span></span>

### <span data-ttu-id="352b5-105">MemberObjectIdWithGroupObjectId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="352b5-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352b5-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="352b5-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352b5-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="352b5-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352b5-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="352b5-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352b5-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="352b5-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352b5-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="352b5-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="352b5-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="352b5-111">DESCRIPTION</span></span>
<span data-ttu-id="352b5-112">Добавляет пользователя в существующую группу AD.</span><span class="sxs-lookup"><span data-stu-id="352b5-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="352b5-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="352b5-113">EXAMPLES</span></span>

### <span data-ttu-id="352b5-114">Пример 1: Добавление пользователя в группу по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="352b5-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="352b5-115">Добавляет пользователя с идентификатором объекта "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" в группу с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="352b5-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="352b5-116">Пример 2. Добавление пользователя в группу с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="352b5-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="352b5-117">Получает группу с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE" и добавляет ее в командлет Add-AzureRmADGroupMember, чтобы добавить пользователя в эту группу.</span><span class="sxs-lookup"><span data-stu-id="352b5-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzureRmADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="352b5-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="352b5-118">PARAMETERS</span></span>

### <span data-ttu-id="352b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="352b5-119">-DefaultProfile</span></span>
<span data-ttu-id="352b5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="352b5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="352b5-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="352b5-121">-MemberObjectId</span></span>
<span data-ttu-id="352b5-122">Идентификатор объекта для элемента.</span><span class="sxs-lookup"><span data-stu-id="352b5-122">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="352b5-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="352b5-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="352b5-124">UPN участника, которого нужно добавить в группу.</span><span class="sxs-lookup"><span data-stu-id="352b5-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="352b5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="352b5-125">-PassThru</span></span>
<span data-ttu-id="352b5-126">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="352b5-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="352b5-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="352b5-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="352b5-128">Отображаемое имя группы, в которую нужно добавить участника (-ей).</span><span class="sxs-lookup"><span data-stu-id="352b5-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="352b5-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="352b5-129">-TargetGroupObject</span></span>
<span data-ttu-id="352b5-130">Объектное представление группы, в которую нужно добавить членов.</span><span class="sxs-lookup"><span data-stu-id="352b5-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="352b5-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="352b5-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="352b5-132">Идентификатор объекта группы, в которую нужно добавить участника (-ей).</span><span class="sxs-lookup"><span data-stu-id="352b5-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="352b5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="352b5-133">-Confirm</span></span>
<span data-ttu-id="352b5-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="352b5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="352b5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="352b5-135">-WhatIf</span></span>
<span data-ttu-id="352b5-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="352b5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="352b5-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="352b5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="352b5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="352b5-138">CommonParameters</span></span>
<span data-ttu-id="352b5-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="352b5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="352b5-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="352b5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="352b5-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="352b5-141">INPUTS</span></span>

### <span data-ttu-id="352b5-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="352b5-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="352b5-143">Параметры: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="352b5-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="352b5-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="352b5-144">OUTPUTS</span></span>

### <span data-ttu-id="352b5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="352b5-145">System.Boolean</span></span>

## <span data-ttu-id="352b5-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="352b5-146">NOTES</span></span>

## <span data-ttu-id="352b5-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="352b5-147">RELATED LINKS</span></span>
