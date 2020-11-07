---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: 0b3498ba3107e2312b596143820036286b925b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732360"
---
# <span data-ttu-id="55301-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="55301-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="55301-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55301-102">SYNOPSIS</span></span>
<span data-ttu-id="55301-103">Создание блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="55301-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55301-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55301-104">SYNTAX</span></span>

### <span data-ttu-id="55301-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55301-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55301-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="55301-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55301-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="55301-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55301-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="55301-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55301-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="55301-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55301-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="55301-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55301-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="55301-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55301-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55301-112">DESCRIPTION</span></span>
<span data-ttu-id="55301-113">Командлет **New-AzureRmResourceLock** создает блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="55301-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="55301-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55301-114">EXAMPLES</span></span>

### <span data-ttu-id="55301-115">Пример 1: создание блокировки ресурса на веб-сайте</span><span class="sxs-lookup"><span data-stu-id="55301-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="55301-116">Эта команда создает блокировку ресурса на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="55301-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="55301-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55301-117">PARAMETERS</span></span>

### <span data-ttu-id="55301-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="55301-118">-ApiVersion</span></span>
<span data-ttu-id="55301-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55301-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="55301-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="55301-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55301-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55301-121">-DefaultProfile</span></span>
<span data-ttu-id="55301-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="55301-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55301-123">-Force</span><span class="sxs-lookup"><span data-stu-id="55301-123">-Force</span></span>
<span data-ttu-id="55301-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="55301-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55301-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="55301-125">-InformationAction</span></span>
<span data-ttu-id="55301-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="55301-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="55301-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="55301-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55301-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="55301-128">Continue</span></span>
- <span data-ttu-id="55301-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="55301-129">Ignore</span></span>
- <span data-ttu-id="55301-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="55301-130">Inquire</span></span>
- <span data-ttu-id="55301-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="55301-131">SilentlyContinue</span></span>
- <span data-ttu-id="55301-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="55301-132">Stop</span></span>
- <span data-ttu-id="55301-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="55301-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55301-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="55301-134">-InformationVariable</span></span>
<span data-ttu-id="55301-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="55301-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55301-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="55301-136">-LockId</span></span>
<span data-ttu-id="55301-137">Указывает идентификатор блокировки.</span><span class="sxs-lookup"><span data-stu-id="55301-137">Specifies the ID of the lock.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55301-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="55301-138">-LockLevel</span></span>
<span data-ttu-id="55301-139">Задает уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="55301-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="55301-140">В настоящее время допустимые значения: CanNotDelete (только для чтения).</span><span class="sxs-lookup"><span data-stu-id="55301-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

```yaml
Type: LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55301-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="55301-141">-LockName</span></span>
<span data-ttu-id="55301-142">Указывает имя блокировки.</span><span class="sxs-lookup"><span data-stu-id="55301-142">Specifies the name of the lock.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55301-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="55301-143">-LockNotes</span></span>
<span data-ttu-id="55301-144">Задает заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="55301-144">Specifies the notes for the lock.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55301-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="55301-145">-Pre</span></span>
<span data-ttu-id="55301-146">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="55301-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55301-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55301-147">-ResourceGroupName</span></span>
<span data-ttu-id="55301-148">Указывает имя группы ресурсов, к которой применяется блокировка, или содержит группу ресурсов, для которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="55301-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55301-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="55301-149">-ResourceName</span></span>
<span data-ttu-id="55301-150">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="55301-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="55301-151">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="55301-151">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55301-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="55301-152">-ResourceType</span></span>
<span data-ttu-id="55301-153">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="55301-153">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55301-154">-Scope</span><span class="sxs-lookup"><span data-stu-id="55301-154">-Scope</span></span>
<span data-ttu-id="55301-155">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="55301-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="55301-156">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="55301-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="55301-157">`/subscriptions/`Идентификатор подписки имя `/resourceGroups/` группы ресурсов имя `/providers/Microsoft.Sql/servers/` сервера `/databases/` базы данных</span><span class="sxs-lookup"><span data-stu-id="55301-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="55301-158">Чтобы указать группу ресурсов, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="55301-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="55301-159">`/subscriptions/``/resourceGroups/`имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="55301-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55301-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="55301-160">-TenantLevel</span></span>
<span data-ttu-id="55301-161">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="55301-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55301-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55301-162">-Confirm</span></span>
<span data-ttu-id="55301-163">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55301-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55301-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55301-164">-WhatIf</span></span>
<span data-ttu-id="55301-165">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55301-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55301-166">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55301-166">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55301-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55301-167">CommonParameters</span></span>
<span data-ttu-id="55301-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55301-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55301-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55301-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55301-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55301-170">INPUTS</span></span>

### <span data-ttu-id="55301-171">Ничего</span><span class="sxs-lookup"><span data-stu-id="55301-171">None</span></span>
<span data-ttu-id="55301-172">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="55301-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55301-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55301-173">OUTPUTS</span></span>

### <span data-ttu-id="55301-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="55301-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="55301-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="55301-175">NOTES</span></span>

## <span data-ttu-id="55301-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55301-176">RELATED LINKS</span></span>

[<span data-ttu-id="55301-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="55301-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="55301-178">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="55301-178">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="55301-179">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="55301-179">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


