---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c719eee4800b404d691d478a989fdfdb3e7be09d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568409"
---
# <span data-ttu-id="7855b-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="7855b-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="7855b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7855b-102">SYNOPSIS</span></span>
<span data-ttu-id="7855b-103">Удаление блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="7855b-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7855b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7855b-104">SYNTAX</span></span>

### <span data-ttu-id="7855b-105">ByLockId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7855b-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7855b-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7855b-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7855b-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="7855b-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7855b-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="7855b-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7855b-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="7855b-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7855b-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="7855b-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7855b-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="7855b-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7855b-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7855b-112">DESCRIPTION</span></span>
<span data-ttu-id="7855b-113">Командлет **Remove-AzureRmResourceLock** удаляет блокировку ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="7855b-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="7855b-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7855b-114">EXAMPLES</span></span>

### <span data-ttu-id="7855b-115">Пример 1: снятие блокировки</span><span class="sxs-lookup"><span data-stu-id="7855b-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="7855b-116">Эта команда удаляет блокировку с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="7855b-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="7855b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7855b-117">PARAMETERS</span></span>

### <span data-ttu-id="7855b-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7855b-118">-ApiVersion</span></span>
<span data-ttu-id="7855b-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7855b-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7855b-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="7855b-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7855b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7855b-121">-DefaultProfile</span></span>
<span data-ttu-id="7855b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7855b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7855b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7855b-123">-Force</span></span>
<span data-ttu-id="7855b-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7855b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7855b-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7855b-125">-InformationAction</span></span>
<span data-ttu-id="7855b-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="7855b-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="7855b-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7855b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7855b-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="7855b-128">Continue</span></span>
- <span data-ttu-id="7855b-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="7855b-129">Ignore</span></span>
- <span data-ttu-id="7855b-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="7855b-130">Inquire</span></span>
- <span data-ttu-id="7855b-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7855b-131">SilentlyContinue</span></span>
- <span data-ttu-id="7855b-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="7855b-132">Stop</span></span>
- <span data-ttu-id="7855b-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="7855b-133">Suspend</span></span>

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

### <span data-ttu-id="7855b-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7855b-134">-InformationVariable</span></span>
<span data-ttu-id="7855b-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="7855b-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7855b-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="7855b-136">-LockId</span></span>
<span data-ttu-id="7855b-137">Указывает идентификатор блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7855b-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7855b-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="7855b-138">-LockName</span></span>
<span data-ttu-id="7855b-139">Указывает имя блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7855b-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7855b-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="7855b-140">-Pre</span></span>
<span data-ttu-id="7855b-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="7855b-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7855b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7855b-142">-ResourceGroupName</span></span>
<span data-ttu-id="7855b-143">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="7855b-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="7855b-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7855b-144">-ResourceName</span></span>
<span data-ttu-id="7855b-145">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="7855b-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="7855b-146">Например, чтобы указать базу данных, используйте следующий формат: `/` база данных сервера</span><span class="sxs-lookup"><span data-stu-id="7855b-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="7855b-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7855b-147">-ResourceType</span></span>
<span data-ttu-id="7855b-148">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="7855b-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="7855b-149">-Scope</span><span class="sxs-lookup"><span data-stu-id="7855b-149">-Scope</span></span>
<span data-ttu-id="7855b-150">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="7855b-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="7855b-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="7855b-151">-TenantLevel</span></span>
<span data-ttu-id="7855b-152">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="7855b-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="7855b-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7855b-153">-Confirm</span></span>
<span data-ttu-id="7855b-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7855b-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7855b-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7855b-155">-WhatIf</span></span>
<span data-ttu-id="7855b-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7855b-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7855b-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7855b-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7855b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7855b-158">CommonParameters</span></span>
<span data-ttu-id="7855b-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7855b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7855b-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7855b-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7855b-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7855b-161">INPUTS</span></span>

## <span data-ttu-id="7855b-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7855b-162">OUTPUTS</span></span>

## <span data-ttu-id="7855b-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="7855b-163">NOTES</span></span>

## <span data-ttu-id="7855b-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7855b-164">RELATED LINKS</span></span>

[<span data-ttu-id="7855b-165">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="7855b-165">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="7855b-166">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="7855b-166">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="7855b-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="7855b-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


