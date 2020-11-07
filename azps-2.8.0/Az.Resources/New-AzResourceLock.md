---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: a0d796d49114cc11fcc50aef85a3ab502593dc35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905566"
---
# <span data-ttu-id="ba14c-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba14c-101">New-AzResourceLock</span></span>

## <span data-ttu-id="ba14c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba14c-102">SYNOPSIS</span></span>
<span data-ttu-id="ba14c-103">Создание блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="ba14c-103">Creates a resource lock.</span></span>

## <span data-ttu-id="ba14c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba14c-104">SYNTAX</span></span>

### <span data-ttu-id="ba14c-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba14c-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba14c-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ba14c-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba14c-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="ba14c-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba14c-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="ba14c-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba14c-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="ba14c-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba14c-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ba14c-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba14c-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="ba14c-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba14c-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba14c-112">DESCRIPTION</span></span>
<span data-ttu-id="ba14c-113">Командлет **New-AzResourceLock** создает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="ba14c-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="ba14c-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba14c-114">EXAMPLES</span></span>

### <span data-ttu-id="ba14c-115">Пример 1: создание блокировки ресурса на веб-сайте</span><span class="sxs-lookup"><span data-stu-id="ba14c-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="ba14c-116">Эта команда создает блокировку ресурса на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="ba14c-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="ba14c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba14c-117">PARAMETERS</span></span>

### <span data-ttu-id="ba14c-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ba14c-118">-ApiVersion</span></span>
<span data-ttu-id="ba14c-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba14c-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ba14c-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="ba14c-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ba14c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba14c-121">-DefaultProfile</span></span>
<span data-ttu-id="ba14c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba14c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba14c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ba14c-123">-Force</span></span>
<span data-ttu-id="ba14c-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ba14c-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba14c-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="ba14c-125">-LockId</span></span>
<span data-ttu-id="ba14c-126">Указывает идентификатор блокировки.</span><span class="sxs-lookup"><span data-stu-id="ba14c-126">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="ba14c-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="ba14c-127">-LockLevel</span></span>
<span data-ttu-id="ba14c-128">Задает уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="ba14c-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="ba14c-129">В настоящее время допустимые значения: CanNotDelete (только для чтения).</span><span class="sxs-lookup"><span data-stu-id="ba14c-129">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="ba14c-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="ba14c-130">-LockName</span></span>
<span data-ttu-id="ba14c-131">Указывает имя блокировки.</span><span class="sxs-lookup"><span data-stu-id="ba14c-131">Specifies the name of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba14c-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="ba14c-132">-LockNotes</span></span>
<span data-ttu-id="ba14c-133">Задает заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="ba14c-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="ba14c-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="ba14c-134">-Pre</span></span>
<span data-ttu-id="ba14c-135">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="ba14c-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ba14c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba14c-136">-ResourceGroupName</span></span>
<span data-ttu-id="ba14c-137">Указывает имя группы ресурсов, к которой применяется блокировка, или содержит группу ресурсов, для которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="ba14c-137">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="ba14c-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ba14c-138">-ResourceName</span></span>
<span data-ttu-id="ba14c-139">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="ba14c-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="ba14c-140">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ba14c-140">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba14c-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ba14c-141">-ResourceType</span></span>
<span data-ttu-id="ba14c-142">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="ba14c-142">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba14c-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="ba14c-143">-Scope</span></span>
<span data-ttu-id="ba14c-144">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="ba14c-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="ba14c-145">Например, чтобы указать базу данных, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки имя `/providers/Microsoft.Sql/servers/` сервера `/databases/` базы данных. чтобы указать группу ресурсов, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="ba14c-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="ba14c-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ba14c-146">-TenantLevel</span></span>
<span data-ttu-id="ba14c-147">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="ba14c-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba14c-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba14c-148">-Confirm</span></span>
<span data-ttu-id="ba14c-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba14c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba14c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba14c-150">-WhatIf</span></span>
<span data-ttu-id="ba14c-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba14c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba14c-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba14c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba14c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba14c-153">CommonParameters</span></span>
<span data-ttu-id="ba14c-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba14c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba14c-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba14c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba14c-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba14c-156">INPUTS</span></span>

### <span data-ttu-id="ba14c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="ba14c-157">System.String</span></span>

### <span data-ttu-id="ba14c-158">Microsoft. Azure. Commands. ResourceManager. командлеты. Entities. locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="ba14c-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="ba14c-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba14c-159">OUTPUTS</span></span>

### <span data-ttu-id="ba14c-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ba14c-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ba14c-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba14c-161">NOTES</span></span>

## <span data-ttu-id="ba14c-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba14c-162">RELATED LINKS</span></span>

[<span data-ttu-id="ba14c-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba14c-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="ba14c-164">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba14c-164">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="ba14c-165">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba14c-165">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


