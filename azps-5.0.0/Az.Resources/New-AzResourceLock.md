---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 7f21704783a9992cc0d1b0fdf3da50cb21656b0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248203"
---
# <span data-ttu-id="a7884-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="a7884-101">New-AzResourceLock</span></span>

## <span data-ttu-id="a7884-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7884-102">SYNOPSIS</span></span>
<span data-ttu-id="a7884-103">Создание блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7884-103">Creates a resource lock.</span></span>

## <span data-ttu-id="a7884-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7884-104">SYNTAX</span></span>

### <span data-ttu-id="a7884-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7884-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7884-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a7884-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7884-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="a7884-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7884-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="a7884-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7884-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a7884-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7884-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="a7884-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7884-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7884-111">DESCRIPTION</span></span>
<span data-ttu-id="a7884-112">Командлет **New-AzResourceLock** создает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7884-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="a7884-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7884-113">EXAMPLES</span></span>

### <span data-ttu-id="a7884-114">Пример 1: создание блокировки ресурса на веб-сайте</span><span class="sxs-lookup"><span data-stu-id="a7884-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="a7884-115">Эта команда создает блокировку ресурса на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="a7884-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="a7884-116">Пример 2: создание блокировки ресурса для базы данных</span><span class="sxs-lookup"><span data-stu-id="a7884-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="a7884-117">Эта команда создает блокировку ресурса для базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a7884-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="a7884-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7884-118">PARAMETERS</span></span>

### <span data-ttu-id="a7884-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a7884-119">-ApiVersion</span></span>
<span data-ttu-id="a7884-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7884-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a7884-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="a7884-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a7884-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7884-122">-DefaultProfile</span></span>
<span data-ttu-id="a7884-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a7884-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7884-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a7884-124">-Force</span></span>
<span data-ttu-id="a7884-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7884-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7884-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="a7884-126">-LockId</span></span>
<span data-ttu-id="a7884-127">Указывает идентификатор блокировки.</span><span class="sxs-lookup"><span data-stu-id="a7884-127">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="a7884-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="a7884-128">-LockLevel</span></span>
<span data-ttu-id="a7884-129">Задает уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="a7884-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="a7884-130">В настоящее время допустимые значения: CanNotDelete (только для чтения).</span><span class="sxs-lookup"><span data-stu-id="a7884-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="a7884-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="a7884-131">-LockName</span></span>
<span data-ttu-id="a7884-132">Указывает имя блокировки.</span><span class="sxs-lookup"><span data-stu-id="a7884-132">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="a7884-133">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="a7884-133">-LockNotes</span></span>
<span data-ttu-id="a7884-134">Задает заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="a7884-134">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="a7884-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="a7884-135">-Pre</span></span>
<span data-ttu-id="a7884-136">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="a7884-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a7884-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7884-137">-ResourceGroupName</span></span>
<span data-ttu-id="a7884-138">Указывает имя группы ресурсов, к которой применяется блокировка, или содержит группу ресурсов, для которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="a7884-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="a7884-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a7884-139">-ResourceName</span></span>
<span data-ttu-id="a7884-140">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="a7884-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="a7884-141">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a7884-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a7884-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a7884-142">-ResourceType</span></span>
<span data-ttu-id="a7884-143">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="a7884-143">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="a7884-144">-Scope</span><span class="sxs-lookup"><span data-stu-id="a7884-144">-Scope</span></span>
<span data-ttu-id="a7884-145">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="a7884-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="a7884-146">Например, чтобы указать базу данных, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки имя `/providers/Microsoft.Sql/servers/` сервера `/databases/` базы данных. чтобы указать группу ресурсов, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="a7884-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="a7884-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7884-147">-Confirm</span></span>
<span data-ttu-id="a7884-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a7884-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7884-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7884-149">-WhatIf</span></span>
<span data-ttu-id="a7884-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a7884-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7884-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a7884-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7884-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7884-152">CommonParameters</span></span>
<span data-ttu-id="a7884-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7884-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7884-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7884-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7884-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7884-155">INPUTS</span></span>

### <span data-ttu-id="a7884-156">System. String</span><span class="sxs-lookup"><span data-stu-id="a7884-156">System.String</span></span>

### <span data-ttu-id="a7884-157">Microsoft. Azure. Commands. ResourceManager. командлеты. Entities. locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="a7884-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="a7884-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7884-158">OUTPUTS</span></span>

### <span data-ttu-id="a7884-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a7884-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a7884-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7884-160">NOTES</span></span>

## <span data-ttu-id="a7884-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7884-161">RELATED LINKS</span></span>

[<span data-ttu-id="a7884-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="a7884-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="a7884-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="a7884-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="a7884-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="a7884-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


