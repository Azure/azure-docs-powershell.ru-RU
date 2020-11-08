---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235396"
---
# <span data-ttu-id="7ff60-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7ff60-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="7ff60-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ff60-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff60-103">Изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="7ff60-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="7ff60-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ff60-104">SYNTAX</span></span>

### <span data-ttu-id="7ff60-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7ff60-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ff60-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7ff60-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ff60-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="7ff60-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ff60-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="7ff60-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ff60-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="7ff60-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ff60-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="7ff60-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ff60-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ff60-111">DESCRIPTION</span></span>
<span data-ttu-id="7ff60-112">Командлет **Set-AzResourceLock** изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="7ff60-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="7ff60-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ff60-113">EXAMPLES</span></span>

### <span data-ttu-id="7ff60-114">Пример 1: обновление заметок для блокировки</span><span class="sxs-lookup"><span data-stu-id="7ff60-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7ff60-115">Эта команда обновляет Примечание для блокировки с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="7ff60-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="7ff60-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ff60-116">PARAMETERS</span></span>

### <span data-ttu-id="7ff60-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7ff60-117">-ApiVersion</span></span>
<span data-ttu-id="7ff60-118">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7ff60-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7ff60-119">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="7ff60-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7ff60-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff60-120">-DefaultProfile</span></span>
<span data-ttu-id="7ff60-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7ff60-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ff60-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7ff60-122">-Force</span></span>
<span data-ttu-id="7ff60-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7ff60-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ff60-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="7ff60-124">-LockId</span></span>
<span data-ttu-id="7ff60-125">Указывает идентификатор блокировки, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7ff60-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7ff60-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="7ff60-126">-LockLevel</span></span>
<span data-ttu-id="7ff60-127">Задает уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="7ff60-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="7ff60-128">В настоящее время единственным допустимым значением является CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="7ff60-128">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="7ff60-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="7ff60-129">-LockName</span></span>
<span data-ttu-id="7ff60-130">Указывает имя блокировки, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7ff60-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7ff60-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="7ff60-131">-LockNotes</span></span>
<span data-ttu-id="7ff60-132">Задает заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="7ff60-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="7ff60-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="7ff60-133">-Pre</span></span>
<span data-ttu-id="7ff60-134">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="7ff60-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7ff60-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ff60-135">-ResourceGroupName</span></span>
<span data-ttu-id="7ff60-136">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="7ff60-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="7ff60-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7ff60-137">-ResourceName</span></span>
<span data-ttu-id="7ff60-138">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="7ff60-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="7ff60-139">Например, чтобы указать базу данных, используйте следующий формат: `/` база данных сервера</span><span class="sxs-lookup"><span data-stu-id="7ff60-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="7ff60-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7ff60-140">-ResourceType</span></span>
<span data-ttu-id="7ff60-141">Указывает тип ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="7ff60-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="7ff60-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="7ff60-142">-Scope</span></span>
<span data-ttu-id="7ff60-143">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="7ff60-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="7ff60-144">Например, чтобы указать базу данных, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки имя `/providers/Microsoft.Sql/servers/` сервера `/databases/` базы данных. чтобы указать группу ресурсов, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="7ff60-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="7ff60-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ff60-145">-Confirm</span></span>
<span data-ttu-id="7ff60-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7ff60-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ff60-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ff60-147">-WhatIf</span></span>
<span data-ttu-id="7ff60-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7ff60-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ff60-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7ff60-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ff60-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff60-150">CommonParameters</span></span>
<span data-ttu-id="7ff60-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ff60-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff60-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ff60-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff60-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ff60-153">INPUTS</span></span>

### <span data-ttu-id="7ff60-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7ff60-154">System.String</span></span>

### <span data-ttu-id="7ff60-155">Microsoft. Azure. Commands. ResourceManager. командлеты. Entities. locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="7ff60-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="7ff60-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ff60-156">OUTPUTS</span></span>

### <span data-ttu-id="7ff60-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7ff60-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7ff60-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ff60-158">NOTES</span></span>

## <span data-ttu-id="7ff60-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ff60-159">RELATED LINKS</span></span>

[<span data-ttu-id="7ff60-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7ff60-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="7ff60-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7ff60-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="7ff60-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="7ff60-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

