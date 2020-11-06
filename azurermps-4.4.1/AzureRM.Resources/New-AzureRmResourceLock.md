---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: c363279c0cbb6dc20b0ddcc7bae32266a848fb3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569215"
---
# <span data-ttu-id="a4981-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a4981-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="a4981-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4981-102">SYNOPSIS</span></span>
<span data-ttu-id="a4981-103">Создание блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="a4981-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4981-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4981-104">SYNTAX</span></span>

### <span data-ttu-id="a4981-105">Блокировка на указанном уровне.</span><span class="sxs-lookup"><span data-stu-id="a4981-105">A lock at the specified scope.</span></span> <span data-ttu-id="a4981-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a4981-106">(Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4981-107">Блокировка в области действия группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4981-107">A lock at the resource group scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4981-108">Блокировка в области ресурсов "Группа ресурсов".</span><span class="sxs-lookup"><span data-stu-id="a4981-108">A lock at the resource group resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4981-109">Блокировка в области подписки.</span><span class="sxs-lookup"><span data-stu-id="a4981-109">A lock at the subscription scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4981-110">Блокировка в области ресурсов подписки.</span><span class="sxs-lookup"><span data-stu-id="a4981-110">A lock at the subscription resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4981-111">Блокировка в области ресурсов клиента.</span><span class="sxs-lookup"><span data-stu-id="a4981-111">A lock at the tenant resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4981-112">Блокировка по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="a4981-112">A lock, by Id.</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4981-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4981-113">DESCRIPTION</span></span>
<span data-ttu-id="a4981-114">Командлет **New-AzureRmResourceLock** создает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="a4981-114">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="a4981-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4981-115">EXAMPLES</span></span>

### <span data-ttu-id="a4981-116">Пример 1: создание блокировки ресурса на веб-сайте</span><span class="sxs-lookup"><span data-stu-id="a4981-116">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="a4981-117">Эта команда создает блокировку ресурса на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="a4981-117">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="a4981-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4981-118">PARAMETERS</span></span>

### <span data-ttu-id="a4981-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a4981-119">-ApiVersion</span></span>
<span data-ttu-id="a4981-120">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4981-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a4981-121">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="a4981-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a4981-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a4981-122">-Force</span></span>
<span data-ttu-id="a4981-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4981-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4981-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a4981-124">-InformationAction</span></span>
<span data-ttu-id="a4981-125">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a4981-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a4981-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a4981-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a4981-127">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a4981-127">Continue</span></span>
- <span data-ttu-id="a4981-128">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a4981-128">Ignore</span></span>
- <span data-ttu-id="a4981-129">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a4981-129">Inquire</span></span>
- <span data-ttu-id="a4981-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a4981-130">SilentlyContinue</span></span>
- <span data-ttu-id="a4981-131">Остановить</span><span class="sxs-lookup"><span data-stu-id="a4981-131">Stop</span></span>
- <span data-ttu-id="a4981-132">Рвать</span><span class="sxs-lookup"><span data-stu-id="a4981-132">Suspend</span></span>

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

### <span data-ttu-id="a4981-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a4981-133">-InformationVariable</span></span>
<span data-ttu-id="a4981-134">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a4981-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a4981-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="a4981-135">-LockId</span></span>
<span data-ttu-id="a4981-136">Указывает идентификатор блокировки.</span><span class="sxs-lookup"><span data-stu-id="a4981-136">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="a4981-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="a4981-137">-LockLevel</span></span>
<span data-ttu-id="a4981-138">Задает уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="a4981-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="a4981-139">В настоящее время единственным допустимым значением является CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="a4981-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="a4981-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="a4981-140">-LockName</span></span>
<span data-ttu-id="a4981-141">Указывает имя блокировки.</span><span class="sxs-lookup"><span data-stu-id="a4981-141">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="a4981-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="a4981-142">-LockNotes</span></span>
<span data-ttu-id="a4981-143">Задает заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="a4981-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="a4981-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="a4981-144">-Pre</span></span>
<span data-ttu-id="a4981-145">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="a4981-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a4981-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4981-146">-ResourceGroupName</span></span>
<span data-ttu-id="a4981-147">Указывает имя группы ресурсов, к которой применяется блокировка, или содержит группу ресурсов, для которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="a4981-147">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="a4981-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a4981-148">-ResourceName</span></span>
<span data-ttu-id="a4981-149">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="a4981-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="a4981-150">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="a4981-150">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

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

### <span data-ttu-id="a4981-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a4981-151">-ResourceType</span></span>
<span data-ttu-id="a4981-152">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="a4981-152">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="a4981-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="a4981-153">-Scope</span></span>
<span data-ttu-id="a4981-154">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="a4981-154">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="a4981-155">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="a4981-155">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="a4981-156">`/subscriptions/`Идентификатор подписки имя `/resourceGroups/` группы ресурсов имя `/providers/Microsoft.Sql/servers/` сервера `/databases/` базы данных</span><span class="sxs-lookup"><span data-stu-id="a4981-156">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="a4981-157">Чтобы указать группу ресурсов, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="a4981-157">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="a4981-158">`/subscriptions/``/resourceGroups/`имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="a4981-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="a4981-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a4981-159">-TenantLevel</span></span>
<span data-ttu-id="a4981-160">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="a4981-160">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a4981-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4981-161">-Confirm</span></span>
<span data-ttu-id="a4981-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4981-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4981-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4981-163">-WhatIf</span></span>
<span data-ttu-id="a4981-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4981-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4981-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4981-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4981-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4981-166">-DefaultProfile</span></span>
<span data-ttu-id="a4981-167">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4981-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4981-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4981-168">CommonParameters</span></span>
<span data-ttu-id="a4981-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4981-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4981-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4981-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4981-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4981-171">INPUTS</span></span>

## <span data-ttu-id="a4981-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4981-172">OUTPUTS</span></span>

### <span data-ttu-id="a4981-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a4981-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a4981-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4981-174">NOTES</span></span>

## <span data-ttu-id="a4981-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4981-175">RELATED LINKS</span></span>

[<span data-ttu-id="a4981-176">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a4981-176">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="a4981-177">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a4981-177">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="a4981-178">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a4981-178">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


