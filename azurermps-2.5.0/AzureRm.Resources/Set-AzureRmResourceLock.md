---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: ccb491742d9a66a7e6eb300d7e75be0dcfac687e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913265"
---
# <span data-ttu-id="186fd-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="186fd-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="186fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="186fd-102">SYNOPSIS</span></span>
<span data-ttu-id="186fd-103">Изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="186fd-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="186fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="186fd-104">SYNTAX</span></span>

### <span data-ttu-id="186fd-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="186fd-105">BySpecifiedScope (Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="186fd-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="186fd-106">ByResourceGroup</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="186fd-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="186fd-107">ByResourceGroupLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186fd-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="186fd-108">BySubscription</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="186fd-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="186fd-109">BySubscriptionLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186fd-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="186fd-110">ByTenantLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186fd-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="186fd-111">ByLockId</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="186fd-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="186fd-112">DESCRIPTION</span></span>
<span data-ttu-id="186fd-113">Командлет **Set-AzureRmResourceLock** изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="186fd-113">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="186fd-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="186fd-114">EXAMPLES</span></span>

### <span data-ttu-id="186fd-115">Пример 1: обновление заметок для блокировки</span><span class="sxs-lookup"><span data-stu-id="186fd-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="186fd-116">Эта команда обновляет Примечание для блокировки с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="186fd-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="186fd-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="186fd-117">PARAMETERS</span></span>

### <span data-ttu-id="186fd-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="186fd-118">-ApiVersion</span></span>
<span data-ttu-id="186fd-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="186fd-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="186fd-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="186fd-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="186fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186fd-121">-DefaultProfile</span></span>
<span data-ttu-id="186fd-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="186fd-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="186fd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="186fd-123">-Force</span></span>
<span data-ttu-id="186fd-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="186fd-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="186fd-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="186fd-125">-InformationAction</span></span>
<span data-ttu-id="186fd-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="186fd-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="186fd-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="186fd-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="186fd-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="186fd-128">Continue</span></span>
- <span data-ttu-id="186fd-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="186fd-129">Ignore</span></span>
- <span data-ttu-id="186fd-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="186fd-130">Inquire</span></span>
- <span data-ttu-id="186fd-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="186fd-131">SilentlyContinue</span></span>
- <span data-ttu-id="186fd-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="186fd-132">Stop</span></span>
- <span data-ttu-id="186fd-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="186fd-133">Suspend</span></span>

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

### <span data-ttu-id="186fd-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="186fd-134">-InformationVariable</span></span>
<span data-ttu-id="186fd-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="186fd-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="186fd-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="186fd-136">-LockId</span></span>
<span data-ttu-id="186fd-137">Указывает идентификатор блокировки, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="186fd-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="186fd-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="186fd-138">-LockLevel</span></span>
<span data-ttu-id="186fd-139">Задает уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="186fd-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="186fd-140">В настоящее время единственным допустимым значением является CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="186fd-140">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="186fd-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="186fd-141">-LockName</span></span>
<span data-ttu-id="186fd-142">Указывает имя блокировки, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="186fd-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="186fd-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="186fd-143">-LockNotes</span></span>
<span data-ttu-id="186fd-144">Задает заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="186fd-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="186fd-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="186fd-145">-Pre</span></span>
<span data-ttu-id="186fd-146">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="186fd-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="186fd-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="186fd-147">-ResourceGroupName</span></span>
<span data-ttu-id="186fd-148">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="186fd-148">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="186fd-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="186fd-149">-ResourceName</span></span>
<span data-ttu-id="186fd-150">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="186fd-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="186fd-151">Например, чтобы указать базу данных, используйте следующий формат: `/` база данных сервера</span><span class="sxs-lookup"><span data-stu-id="186fd-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="186fd-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="186fd-152">-ResourceType</span></span>
<span data-ttu-id="186fd-153">Указывает тип ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="186fd-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="186fd-154">-Scope</span><span class="sxs-lookup"><span data-stu-id="186fd-154">-Scope</span></span>
<span data-ttu-id="186fd-155">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="186fd-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="186fd-156">Например, чтобы указать базу данных, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки имя `/providers/Microsoft.Sql/servers/` сервера `/databases/` базы данных. чтобы указать группу ресурсов, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="186fd-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="186fd-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="186fd-157">-TenantLevel</span></span>
<span data-ttu-id="186fd-158">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="186fd-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="186fd-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="186fd-159">-Confirm</span></span>
<span data-ttu-id="186fd-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="186fd-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="186fd-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="186fd-161">-WhatIf</span></span>
<span data-ttu-id="186fd-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="186fd-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="186fd-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="186fd-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="186fd-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186fd-164">CommonParameters</span></span>
<span data-ttu-id="186fd-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="186fd-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186fd-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="186fd-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186fd-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="186fd-167">INPUTS</span></span>

## <span data-ttu-id="186fd-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="186fd-168">OUTPUTS</span></span>

## <span data-ttu-id="186fd-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="186fd-169">NOTES</span></span>

## <span data-ttu-id="186fd-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="186fd-170">RELATED LINKS</span></span>

[<span data-ttu-id="186fd-171">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="186fd-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="186fd-172">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="186fd-172">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="186fd-173">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="186fd-173">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


