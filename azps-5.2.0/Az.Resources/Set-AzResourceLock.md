---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405588"
---
# <span data-ttu-id="409bc-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="409bc-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="409bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="409bc-102">SYNOPSIS</span></span>
<span data-ttu-id="409bc-103">Изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="409bc-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="409bc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="409bc-104">SYNTAX</span></span>

### <span data-ttu-id="409bc-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="409bc-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="409bc-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="409bc-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="409bc-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="409bc-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="409bc-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="409bc-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="409bc-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="409bc-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="409bc-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="409bc-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="409bc-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="409bc-111">DESCRIPTION</span></span>
<span data-ttu-id="409bc-112">**Cmdlet Set-AzResourceLock** изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="409bc-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="409bc-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="409bc-113">EXAMPLES</span></span>

### <span data-ttu-id="409bc-114">Пример 1. Обновление заметок для блокировки</span><span class="sxs-lookup"><span data-stu-id="409bc-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="409bc-115">Эта команда обновляет заметку для блокировки ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="409bc-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="409bc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="409bc-116">PARAMETERS</span></span>

### <span data-ttu-id="409bc-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="409bc-117">-ApiVersion</span></span>
<span data-ttu-id="409bc-118">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="409bc-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="409bc-119">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="409bc-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="409bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="409bc-120">-DefaultProfile</span></span>
<span data-ttu-id="409bc-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="409bc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="409bc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="409bc-122">-Force</span></span>
<span data-ttu-id="409bc-123">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="409bc-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="409bc-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="409bc-124">-LockId</span></span>
<span data-ttu-id="409bc-125">Определяет код блокировки, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="409bc-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="409bc-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="409bc-126">-LockLevel</span></span>
<span data-ttu-id="409bc-127">Уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="409bc-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="409bc-128">В настоящее время единственным допустимым значением является CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="409bc-128">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="409bc-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="409bc-129">-LockName</span></span>
<span data-ttu-id="409bc-130">Указывает имя блокировки, которая изменяется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="409bc-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="409bc-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="409bc-131">-LockNotes</span></span>
<span data-ttu-id="409bc-132">Определяет заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="409bc-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="409bc-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="409bc-133">-Pre</span></span>
<span data-ttu-id="409bc-134">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="409bc-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="409bc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="409bc-135">-ResourceGroupName</span></span>
<span data-ttu-id="409bc-136">Имя группы ресурсов, для которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="409bc-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="409bc-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="409bc-137">-ResourceName</span></span>
<span data-ttu-id="409bc-138">Указывает имя ресурса, для которого применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="409bc-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="409bc-139">Например, чтобы указать базу данных, используйте следующий формат: "База данных `/` сервера"</span><span class="sxs-lookup"><span data-stu-id="409bc-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="409bc-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="409bc-140">-ResourceType</span></span>
<span data-ttu-id="409bc-141">Тип ресурса, для которого применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="409bc-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="409bc-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="409bc-142">-Scope</span></span>
<span data-ttu-id="409bc-143">Определяет область применения блокировки.</span><span class="sxs-lookup"><span data-stu-id="409bc-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="409bc-144">Например, чтобы указать базу данных, используйте следующий формат: имя сервера базы данных с ИД ресурса подписки. Чтобы указать группу ресурсов, используйте следующий формат: имя группы ресурсов «ИД `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` `/subscriptions/` `/resourceGroups/` подписки»</span><span class="sxs-lookup"><span data-stu-id="409bc-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="409bc-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="409bc-145">-Confirm</span></span>
<span data-ttu-id="409bc-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="409bc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="409bc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="409bc-147">-WhatIf</span></span>
<span data-ttu-id="409bc-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="409bc-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="409bc-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="409bc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="409bc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409bc-150">CommonParameters</span></span>
<span data-ttu-id="409bc-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="409bc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409bc-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="409bc-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409bc-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="409bc-153">INPUTS</span></span>

### <span data-ttu-id="409bc-154">System.String</span><span class="sxs-lookup"><span data-stu-id="409bc-154">System.String</span></span>

### <span data-ttu-id="409bc-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="409bc-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="409bc-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="409bc-156">OUTPUTS</span></span>

### <span data-ttu-id="409bc-157">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="409bc-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="409bc-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="409bc-158">NOTES</span></span>

## <span data-ttu-id="409bc-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="409bc-159">RELATED LINKS</span></span>

[<span data-ttu-id="409bc-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="409bc-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="409bc-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="409bc-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="409bc-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="409bc-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


