---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733623"
---
# <span data-ttu-id="ba4a4-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba4a4-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="ba4a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba4a4-103">Изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba4a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba4a4-104">SYNTAX</span></span>

### <span data-ttu-id="ba4a4-105">Блокировка на указанном уровне.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-105">A lock at the specified scope.</span></span> <span data-ttu-id="ba4a4-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ba4a4-106">(Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba4a4-107">Блокировка в области действия группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-107">A lock at the resource group scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba4a4-108">Блокировка в области ресурсов "Группа ресурсов".</span><span class="sxs-lookup"><span data-stu-id="ba4a4-108">A lock at the resource group resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba4a4-109">Блокировка в области подписки.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-109">A lock at the subscription scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba4a4-110">Блокировка в области ресурсов подписки.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-110">A lock at the subscription resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba4a4-111">Блокировка в области ресурсов клиента.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-111">A lock at the tenant resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba4a4-112">Блокировка по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-112">A lock, by Id.</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba4a4-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba4a4-113">DESCRIPTION</span></span>
<span data-ttu-id="ba4a4-114">Командлет **Set-AzureRmResourceLock** изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-114">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="ba4a4-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba4a4-115">EXAMPLES</span></span>

### <span data-ttu-id="ba4a4-116">Пример 1: обновление заметок для блокировки</span><span class="sxs-lookup"><span data-stu-id="ba4a4-116">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ba4a4-117">Эта команда обновляет Примечание для блокировки с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-117">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="ba4a4-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba4a4-118">PARAMETERS</span></span>

### <span data-ttu-id="ba4a4-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ba4a4-119">-ApiVersion</span></span>
<span data-ttu-id="ba4a4-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ba4a4-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ba4a4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ba4a4-122">-Force</span></span>
<span data-ttu-id="ba4a4-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba4a4-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ba4a4-124">-InformationAction</span></span>
<span data-ttu-id="ba4a4-125">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ba4a4-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ba4a4-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba4a4-127">Продолжал</span><span class="sxs-lookup"><span data-stu-id="ba4a4-127">Continue</span></span>
- <span data-ttu-id="ba4a4-128">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="ba4a4-128">Ignore</span></span>
- <span data-ttu-id="ba4a4-129">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="ba4a4-129">Inquire</span></span>
- <span data-ttu-id="ba4a4-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ba4a4-130">SilentlyContinue</span></span>
- <span data-ttu-id="ba4a4-131">Остановить</span><span class="sxs-lookup"><span data-stu-id="ba4a4-131">Stop</span></span>
- <span data-ttu-id="ba4a4-132">Рвать</span><span class="sxs-lookup"><span data-stu-id="ba4a4-132">Suspend</span></span>

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

### <span data-ttu-id="ba4a4-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ba4a4-133">-InformationVariable</span></span>
<span data-ttu-id="ba4a4-134">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ba4a4-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="ba4a4-135">-LockId</span></span>
<span data-ttu-id="ba4a4-136">Указывает идентификатор блокировки, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-136">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4a4-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="ba4a4-137">-LockLevel</span></span>
<span data-ttu-id="ba4a4-138">Задает уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="ba4a4-139">В настоящее время единственным допустимым значением является CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="ba4a4-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="ba4a4-140">-LockName</span></span>
<span data-ttu-id="ba4a4-141">Указывает имя блокировки, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-141">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4a4-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="ba4a4-142">-LockNotes</span></span>
<span data-ttu-id="ba4a4-143">Задает заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="ba4a4-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="ba4a4-144">-Pre</span></span>
<span data-ttu-id="ba4a4-145">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ba4a4-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba4a4-146">-ResourceGroupName</span></span>
<span data-ttu-id="ba4a4-147">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-147">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4a4-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ba4a4-148">-ResourceName</span></span>
<span data-ttu-id="ba4a4-149">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="ba4a4-150">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="ba4a4-150">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="ba4a4-151">`/`База данных сервера</span><span class="sxs-lookup"><span data-stu-id="ba4a4-151">Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4a4-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ba4a4-152">-ResourceType</span></span>
<span data-ttu-id="ba4a4-153">Указывает тип ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-153">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4a4-154">-Scope</span><span class="sxs-lookup"><span data-stu-id="ba4a4-154">-Scope</span></span>
<span data-ttu-id="ba4a4-155">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="ba4a4-156">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="ba4a4-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="ba4a4-157">`/subscriptions/`Идентификатор подписки имя `/resourceGroups/` группы ресурсов имя `/providers/Microsoft.Sql/servers/` сервера `/databases/` базы данных</span><span class="sxs-lookup"><span data-stu-id="ba4a4-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="ba4a4-158">Чтобы указать группу ресурсов, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="ba4a4-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="ba4a4-159">`/subscriptions/``/resourceGroups/`имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="ba4a4-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4a4-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ba4a4-160">-TenantLevel</span></span>
<span data-ttu-id="ba4a4-161">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba4a4-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba4a4-162">-Confirm</span></span>
<span data-ttu-id="ba4a4-163">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba4a4-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba4a4-164">-WhatIf</span></span>
<span data-ttu-id="ba4a4-165">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba4a4-166">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba4a4-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4a4-167">-DefaultProfile</span></span>
<span data-ttu-id="ba4a4-168">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba4a4-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4a4-169">CommonParameters</span></span>
<span data-ttu-id="ba4a4-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4a4-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba4a4-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4a4-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba4a4-172">INPUTS</span></span>

## <span data-ttu-id="ba4a4-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba4a4-173">OUTPUTS</span></span>

### <span data-ttu-id="ba4a4-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ba4a4-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ba4a4-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba4a4-175">NOTES</span></span>

## <span data-ttu-id="ba4a4-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba4a4-176">RELATED LINKS</span></span>

[<span data-ttu-id="ba4a4-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba4a4-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="ba4a4-178">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba4a4-178">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="ba4a4-179">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="ba4a4-179">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


