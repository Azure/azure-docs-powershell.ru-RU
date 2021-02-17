---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212828"
---
# <span data-ttu-id="75bbc-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="75bbc-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="75bbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="75bbc-103">Изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="75bbc-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="75bbc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75bbc-104">SYNTAX</span></span>

### <span data-ttu-id="75bbc-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75bbc-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75bbc-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="75bbc-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75bbc-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="75bbc-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75bbc-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="75bbc-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75bbc-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="75bbc-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75bbc-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="75bbc-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75bbc-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75bbc-111">DESCRIPTION</span></span>
<span data-ttu-id="75bbc-112">**Cmdlet Set-AzResourceLock** изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="75bbc-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="75bbc-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75bbc-113">EXAMPLES</span></span>

### <span data-ttu-id="75bbc-114">Пример 1. Обновление заметок для блокировки</span><span class="sxs-lookup"><span data-stu-id="75bbc-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="75bbc-115">Эта команда обновляет заметку для блокировки ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="75bbc-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="75bbc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75bbc-116">PARAMETERS</span></span>

### <span data-ttu-id="75bbc-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="75bbc-117">-ApiVersion</span></span>
<span data-ttu-id="75bbc-118">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75bbc-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="75bbc-119">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="75bbc-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bbc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75bbc-120">-DefaultProfile</span></span>
<span data-ttu-id="75bbc-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="75bbc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75bbc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="75bbc-122">-Force</span></span>
<span data-ttu-id="75bbc-123">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="75bbc-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75bbc-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="75bbc-124">-LockId</span></span>
<span data-ttu-id="75bbc-125">Определяет код блокировки, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75bbc-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bbc-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="75bbc-126">-LockLevel</span></span>
<span data-ttu-id="75bbc-127">Уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="75bbc-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="75bbc-128">В настоящее время единственным допустимым значением является CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="75bbc-128">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bbc-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="75bbc-129">-LockName</span></span>
<span data-ttu-id="75bbc-130">Указывает имя блокировки, которая изменяется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75bbc-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bbc-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="75bbc-131">-LockNotes</span></span>
<span data-ttu-id="75bbc-132">Определяет заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="75bbc-132">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bbc-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="75bbc-133">-Pre</span></span>
<span data-ttu-id="75bbc-134">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="75bbc-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="75bbc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75bbc-135">-ResourceGroupName</span></span>
<span data-ttu-id="75bbc-136">Имя группы ресурсов, для которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="75bbc-136">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bbc-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="75bbc-137">-ResourceName</span></span>
<span data-ttu-id="75bbc-138">Указывает имя ресурса, для которого применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="75bbc-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="75bbc-139">Например, чтобы указать базу данных, используйте следующий формат: "База данных `/` сервера".</span><span class="sxs-lookup"><span data-stu-id="75bbc-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bbc-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="75bbc-140">-ResourceType</span></span>
<span data-ttu-id="75bbc-141">Тип ресурса, для которого применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="75bbc-141">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bbc-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="75bbc-142">-Scope</span></span>
<span data-ttu-id="75bbc-143">Определяет область применения блокировки.</span><span class="sxs-lookup"><span data-stu-id="75bbc-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="75bbc-144">Например, чтобы указать базу данных, используйте следующий формат: имя базы данных "Имя сервера имен сервера имен ресурсов" группы ресурсов "ИД подписки". Чтобы указать группу ресурсов, используйте следующий формат: имя группы ресурсов "ИД `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` `/subscriptions/` `/resourceGroups/` подписки".</span><span class="sxs-lookup"><span data-stu-id="75bbc-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bbc-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75bbc-145">-Confirm</span></span>
<span data-ttu-id="75bbc-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="75bbc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75bbc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75bbc-147">-WhatIf</span></span>
<span data-ttu-id="75bbc-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75bbc-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75bbc-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="75bbc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75bbc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75bbc-150">CommonParameters</span></span>
<span data-ttu-id="75bbc-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75bbc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75bbc-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75bbc-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75bbc-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75bbc-153">INPUTS</span></span>

### <span data-ttu-id="75bbc-154">System.String</span><span class="sxs-lookup"><span data-stu-id="75bbc-154">System.String</span></span>

### <span data-ttu-id="75bbc-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="75bbc-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="75bbc-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75bbc-156">OUTPUTS</span></span>

### <span data-ttu-id="75bbc-157">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="75bbc-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="75bbc-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75bbc-158">NOTES</span></span>

## <span data-ttu-id="75bbc-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75bbc-159">RELATED LINKS</span></span>

[<span data-ttu-id="75bbc-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="75bbc-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="75bbc-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="75bbc-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="75bbc-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="75bbc-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


