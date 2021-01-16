---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 7f21704783a9992cc0d1b0fdf3da50cb21656b0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409607"
---
# <span data-ttu-id="d80c1-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d80c1-101">New-AzResourceLock</span></span>

## <span data-ttu-id="d80c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d80c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d80c1-103">Создает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="d80c1-103">Creates a resource lock.</span></span>

## <span data-ttu-id="d80c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d80c1-104">SYNTAX</span></span>

### <span data-ttu-id="d80c1-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d80c1-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d80c1-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d80c1-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80c1-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="d80c1-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80c1-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="d80c1-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d80c1-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="d80c1-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80c1-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="d80c1-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d80c1-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d80c1-111">DESCRIPTION</span></span>
<span data-ttu-id="d80c1-112">Для **этого создается** блокировка ресурса.</span><span class="sxs-lookup"><span data-stu-id="d80c1-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="d80c1-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d80c1-113">EXAMPLES</span></span>

### <span data-ttu-id="d80c1-114">Пример 1. Создание блокировки ресурса на веб-сайте</span><span class="sxs-lookup"><span data-stu-id="d80c1-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="d80c1-115">Эта команда создает блокировку ресурса на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="d80c1-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="d80c1-116">Пример 2. Создание блокировки ресурса для базы данных</span><span class="sxs-lookup"><span data-stu-id="d80c1-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="d80c1-117">Эта команда создает блокировку ресурса для базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="d80c1-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="d80c1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d80c1-118">PARAMETERS</span></span>

### <span data-ttu-id="d80c1-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d80c1-119">-ApiVersion</span></span>
<span data-ttu-id="d80c1-120">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d80c1-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d80c1-121">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="d80c1-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d80c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80c1-122">-DefaultProfile</span></span>
<span data-ttu-id="d80c1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d80c1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d80c1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d80c1-124">-Force</span></span>
<span data-ttu-id="d80c1-125">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d80c1-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d80c1-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="d80c1-126">-LockId</span></span>
<span data-ttu-id="d80c1-127">Определяет ИД блокировки.</span><span class="sxs-lookup"><span data-stu-id="d80c1-127">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="d80c1-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="d80c1-128">-LockLevel</span></span>
<span data-ttu-id="d80c1-129">Уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="d80c1-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="d80c1-130">В настоящее время допустимые значения: CanNotDelete и ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="d80c1-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="d80c1-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="d80c1-131">-LockName</span></span>
<span data-ttu-id="d80c1-132">Указывает имя блокировки.</span><span class="sxs-lookup"><span data-stu-id="d80c1-132">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="d80c1-133">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="d80c1-133">-LockNotes</span></span>
<span data-ttu-id="d80c1-134">Определяет заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="d80c1-134">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="d80c1-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="d80c1-135">-Pre</span></span>
<span data-ttu-id="d80c1-136">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="d80c1-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d80c1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d80c1-137">-ResourceGroupName</span></span>
<span data-ttu-id="d80c1-138">Определяет имя группы ресурсов, для которой применяется блокировка, или группу ресурсов, для которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="d80c1-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="d80c1-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d80c1-139">-ResourceName</span></span>
<span data-ttu-id="d80c1-140">Указывает имя ресурса, для которого применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="d80c1-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="d80c1-141">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="d80c1-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="d80c1-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d80c1-142">-ResourceType</span></span>
<span data-ttu-id="d80c1-143">Определяет тип ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="d80c1-143">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="d80c1-144">-Scope</span><span class="sxs-lookup"><span data-stu-id="d80c1-144">-Scope</span></span>
<span data-ttu-id="d80c1-145">Определяет область применения блокировки.</span><span class="sxs-lookup"><span data-stu-id="d80c1-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="d80c1-146">Например, чтобы указать базу данных, используйте следующий формат: имя сервера базы данных с ИД ресурса подписки. Чтобы указать группу ресурсов, используйте следующий формат: имя группы ресурсов «ИД `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` `/subscriptions/` `/resourceGroups/` подписки»</span><span class="sxs-lookup"><span data-stu-id="d80c1-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="d80c1-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d80c1-147">-Confirm</span></span>
<span data-ttu-id="d80c1-148">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d80c1-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d80c1-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d80c1-149">-WhatIf</span></span>
<span data-ttu-id="d80c1-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d80c1-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d80c1-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d80c1-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d80c1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80c1-152">CommonParameters</span></span>
<span data-ttu-id="d80c1-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d80c1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80c1-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d80c1-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80c1-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d80c1-155">INPUTS</span></span>

### <span data-ttu-id="d80c1-156">System.String</span><span class="sxs-lookup"><span data-stu-id="d80c1-156">System.String</span></span>

### <span data-ttu-id="d80c1-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="d80c1-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="d80c1-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d80c1-158">OUTPUTS</span></span>

### <span data-ttu-id="d80c1-159">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="d80c1-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d80c1-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d80c1-160">NOTES</span></span>

## <span data-ttu-id="d80c1-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d80c1-161">RELATED LINKS</span></span>

[<span data-ttu-id="d80c1-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d80c1-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="d80c1-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d80c1-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="d80c1-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d80c1-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


