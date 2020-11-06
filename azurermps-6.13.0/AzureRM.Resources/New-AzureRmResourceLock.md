---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: cf1f245b06e607bc96a8e23429d15954ce7b69f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558300"
---
# <span data-ttu-id="95a95-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="95a95-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="95a95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95a95-102">SYNOPSIS</span></span>
<span data-ttu-id="95a95-103">Создание блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="95a95-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95a95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95a95-104">SYNTAX</span></span>

### <span data-ttu-id="95a95-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95a95-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95a95-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95a95-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95a95-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="95a95-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95a95-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="95a95-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95a95-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="95a95-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95a95-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="95a95-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95a95-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="95a95-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95a95-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95a95-112">DESCRIPTION</span></span>
<span data-ttu-id="95a95-113">Командлет **New-AzureRmResourceLock** создает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="95a95-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="95a95-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95a95-114">EXAMPLES</span></span>

### <span data-ttu-id="95a95-115">Пример 1: создание блокировки ресурса на веб-сайте</span><span class="sxs-lookup"><span data-stu-id="95a95-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="95a95-116">Эта команда создает блокировку ресурса на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="95a95-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="95a95-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95a95-117">PARAMETERS</span></span>

### <span data-ttu-id="95a95-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="95a95-118">-ApiVersion</span></span>
<span data-ttu-id="95a95-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95a95-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="95a95-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="95a95-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="95a95-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a95-121">-DefaultProfile</span></span>
<span data-ttu-id="95a95-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="95a95-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95a95-123">-Force</span><span class="sxs-lookup"><span data-stu-id="95a95-123">-Force</span></span>
<span data-ttu-id="95a95-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="95a95-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95a95-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="95a95-125">-InformationAction</span></span>
<span data-ttu-id="95a95-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="95a95-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="95a95-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="95a95-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95a95-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="95a95-128">Continue</span></span>
- <span data-ttu-id="95a95-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="95a95-129">Ignore</span></span>
- <span data-ttu-id="95a95-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="95a95-130">Inquire</span></span>
- <span data-ttu-id="95a95-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="95a95-131">SilentlyContinue</span></span>
- <span data-ttu-id="95a95-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="95a95-132">Stop</span></span>
- <span data-ttu-id="95a95-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="95a95-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95a95-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="95a95-134">-InformationVariable</span></span>
<span data-ttu-id="95a95-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="95a95-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95a95-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="95a95-136">-LockId</span></span>
<span data-ttu-id="95a95-137">Указывает идентификатор блокировки.</span><span class="sxs-lookup"><span data-stu-id="95a95-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="95a95-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="95a95-138">-LockLevel</span></span>
<span data-ttu-id="95a95-139">Задает уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="95a95-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="95a95-140">В настоящее время допустимые значения: CanNotDelete (только для чтения).</span><span class="sxs-lookup"><span data-stu-id="95a95-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a95-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="95a95-141">-LockName</span></span>
<span data-ttu-id="95a95-142">Указывает имя блокировки.</span><span class="sxs-lookup"><span data-stu-id="95a95-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="95a95-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="95a95-143">-LockNotes</span></span>
<span data-ttu-id="95a95-144">Задает заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="95a95-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="95a95-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="95a95-145">-Pre</span></span>
<span data-ttu-id="95a95-146">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="95a95-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="95a95-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95a95-147">-ResourceGroupName</span></span>
<span data-ttu-id="95a95-148">Указывает имя группы ресурсов, к которой применяется блокировка, или содержит группу ресурсов, для которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="95a95-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="95a95-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="95a95-149">-ResourceName</span></span>
<span data-ttu-id="95a95-150">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="95a95-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="95a95-151">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="95a95-151">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="95a95-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="95a95-152">-ResourceType</span></span>
<span data-ttu-id="95a95-153">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="95a95-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="95a95-154">-Scope</span><span class="sxs-lookup"><span data-stu-id="95a95-154">-Scope</span></span>
<span data-ttu-id="95a95-155">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="95a95-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="95a95-156">Например, чтобы указать базу данных, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки имя `/providers/Microsoft.Sql/servers/` сервера `/databases/` базы данных. чтобы указать группу ресурсов, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="95a95-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="95a95-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="95a95-157">-TenantLevel</span></span>
<span data-ttu-id="95a95-158">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="95a95-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="95a95-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95a95-159">-Confirm</span></span>
<span data-ttu-id="95a95-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95a95-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a95-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95a95-161">-WhatIf</span></span>
<span data-ttu-id="95a95-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95a95-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95a95-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95a95-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a95-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a95-164">CommonParameters</span></span>
<span data-ttu-id="95a95-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95a95-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a95-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a95-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a95-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95a95-167">INPUTS</span></span>

## <span data-ttu-id="95a95-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95a95-168">OUTPUTS</span></span>

## <span data-ttu-id="95a95-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="95a95-169">NOTES</span></span>

## <span data-ttu-id="95a95-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95a95-170">RELATED LINKS</span></span>

[<span data-ttu-id="95a95-171">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="95a95-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="95a95-172">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="95a95-172">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="95a95-173">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="95a95-173">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


