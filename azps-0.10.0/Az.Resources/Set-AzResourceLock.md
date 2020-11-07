---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: fdf9f91570fc598806427b6812f52e397fb19322
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910817"
---
# <span data-ttu-id="22f4b-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="22f4b-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="22f4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="22f4b-103">Изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="22f4b-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="22f4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22f4b-104">SYNTAX</span></span>

### <span data-ttu-id="22f4b-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22f4b-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22f4b-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22f4b-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22f4b-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="22f4b-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22f4b-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="22f4b-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22f4b-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="22f4b-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22f4b-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="22f4b-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22f4b-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="22f4b-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22f4b-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22f4b-112">DESCRIPTION</span></span>
<span data-ttu-id="22f4b-113">Командлет **Set-AzResourceLock** изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="22f4b-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="22f4b-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22f4b-114">EXAMPLES</span></span>

### <span data-ttu-id="22f4b-115">Пример 1: обновление заметок для блокировки</span><span class="sxs-lookup"><span data-stu-id="22f4b-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="22f4b-116">Эта команда обновляет Примечание для блокировки с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="22f4b-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="22f4b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22f4b-117">PARAMETERS</span></span>

### <span data-ttu-id="22f4b-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22f4b-118">-ApiVersion</span></span>
<span data-ttu-id="22f4b-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22f4b-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="22f4b-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="22f4b-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="22f4b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f4b-121">-DefaultProfile</span></span>
<span data-ttu-id="22f4b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="22f4b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22f4b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="22f4b-123">-Force</span></span>
<span data-ttu-id="22f4b-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="22f4b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22f4b-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="22f4b-125">-InformationAction</span></span>
<span data-ttu-id="22f4b-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="22f4b-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="22f4b-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="22f4b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22f4b-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="22f4b-128">Continue</span></span>
- <span data-ttu-id="22f4b-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="22f4b-129">Ignore</span></span>
- <span data-ttu-id="22f4b-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="22f4b-130">Inquire</span></span>
- <span data-ttu-id="22f4b-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="22f4b-131">SilentlyContinue</span></span>
- <span data-ttu-id="22f4b-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="22f4b-132">Stop</span></span>
- <span data-ttu-id="22f4b-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="22f4b-133">Suspend</span></span>

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

### <span data-ttu-id="22f4b-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="22f4b-134">-InformationVariable</span></span>
<span data-ttu-id="22f4b-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="22f4b-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="22f4b-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="22f4b-136">-LockId</span></span>
<span data-ttu-id="22f4b-137">Указывает идентификатор блокировки, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="22f4b-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="22f4b-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="22f4b-138">-LockLevel</span></span>
<span data-ttu-id="22f4b-139">Задает уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="22f4b-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="22f4b-140">В настоящее время единственным допустимым значением является CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="22f4b-140">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="22f4b-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="22f4b-141">-LockName</span></span>
<span data-ttu-id="22f4b-142">Указывает имя блокировки, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="22f4b-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="22f4b-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="22f4b-143">-LockNotes</span></span>
<span data-ttu-id="22f4b-144">Задает заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="22f4b-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="22f4b-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="22f4b-145">-Pre</span></span>
<span data-ttu-id="22f4b-146">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="22f4b-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="22f4b-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22f4b-147">-ResourceGroupName</span></span>
<span data-ttu-id="22f4b-148">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="22f4b-148">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="22f4b-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="22f4b-149">-ResourceName</span></span>
<span data-ttu-id="22f4b-150">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="22f4b-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="22f4b-151">Например, чтобы указать базу данных, используйте следующий формат: `/` база данных сервера</span><span class="sxs-lookup"><span data-stu-id="22f4b-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="22f4b-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="22f4b-152">-ResourceType</span></span>
<span data-ttu-id="22f4b-153">Указывает тип ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="22f4b-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="22f4b-154">-Scope</span><span class="sxs-lookup"><span data-stu-id="22f4b-154">-Scope</span></span>
<span data-ttu-id="22f4b-155">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="22f4b-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="22f4b-156">Например, чтобы указать базу данных, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки имя `/providers/Microsoft.Sql/servers/` сервера `/databases/` базы данных. чтобы указать группу ресурсов, используйте следующий формат: `/subscriptions/` `/resourceGroups/` имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="22f4b-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="22f4b-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="22f4b-157">-TenantLevel</span></span>
<span data-ttu-id="22f4b-158">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="22f4b-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="22f4b-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22f4b-159">-Confirm</span></span>
<span data-ttu-id="22f4b-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="22f4b-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22f4b-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22f4b-161">-WhatIf</span></span>
<span data-ttu-id="22f4b-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="22f4b-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22f4b-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="22f4b-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22f4b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f4b-164">CommonParameters</span></span>
<span data-ttu-id="22f4b-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22f4b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f4b-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22f4b-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f4b-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22f4b-167">INPUTS</span></span>

## <span data-ttu-id="22f4b-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22f4b-168">OUTPUTS</span></span>

## <span data-ttu-id="22f4b-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="22f4b-169">NOTES</span></span>

## <span data-ttu-id="22f4b-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22f4b-170">RELATED LINKS</span></span>

[<span data-ttu-id="22f4b-171">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="22f4b-171">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="22f4b-172">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="22f4b-172">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="22f4b-173">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="22f4b-173">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


