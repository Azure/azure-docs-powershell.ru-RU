---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: fdf60c029f260d30aae8983165cbfb4d20203824
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913968"
---
# <span data-ttu-id="01ea8-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="01ea8-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="01ea8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="01ea8-103">Удаление блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="01ea8-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01ea8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01ea8-104">SYNTAX</span></span>

### <span data-ttu-id="01ea8-105">ByLockId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01ea8-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01ea8-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="01ea8-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01ea8-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="01ea8-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01ea8-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="01ea8-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01ea8-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="01ea8-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01ea8-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="01ea8-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01ea8-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="01ea8-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01ea8-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01ea8-112">DESCRIPTION</span></span>
<span data-ttu-id="01ea8-113">Командлет **Remove-AzureRmResourceLock** удаляет блокировку ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="01ea8-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="01ea8-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01ea8-114">EXAMPLES</span></span>

### <span data-ttu-id="01ea8-115">Пример 1: снятие блокировки</span><span class="sxs-lookup"><span data-stu-id="01ea8-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="01ea8-116">Эта команда удаляет блокировку с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="01ea8-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="01ea8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01ea8-117">PARAMETERS</span></span>

### <span data-ttu-id="01ea8-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="01ea8-118">-ApiVersion</span></span>
<span data-ttu-id="01ea8-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01ea8-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="01ea8-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="01ea8-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="01ea8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ea8-121">-DefaultProfile</span></span>
<span data-ttu-id="01ea8-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="01ea8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01ea8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="01ea8-123">-Force</span></span>
<span data-ttu-id="01ea8-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="01ea8-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="01ea8-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="01ea8-125">-InformationAction</span></span>
<span data-ttu-id="01ea8-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="01ea8-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="01ea8-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="01ea8-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="01ea8-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="01ea8-128">Continue</span></span>
- <span data-ttu-id="01ea8-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="01ea8-129">Ignore</span></span>
- <span data-ttu-id="01ea8-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="01ea8-130">Inquire</span></span>
- <span data-ttu-id="01ea8-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="01ea8-131">SilentlyContinue</span></span>
- <span data-ttu-id="01ea8-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="01ea8-132">Stop</span></span>
- <span data-ttu-id="01ea8-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="01ea8-133">Suspend</span></span>

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

### <span data-ttu-id="01ea8-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="01ea8-134">-InformationVariable</span></span>
<span data-ttu-id="01ea8-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="01ea8-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="01ea8-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="01ea8-136">-LockId</span></span>
<span data-ttu-id="01ea8-137">Указывает идентификатор блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="01ea8-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="01ea8-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="01ea8-138">-LockName</span></span>
<span data-ttu-id="01ea8-139">Указывает имя блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="01ea8-139">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="01ea8-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="01ea8-140">-Pre</span></span>
<span data-ttu-id="01ea8-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="01ea8-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="01ea8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ea8-142">-ResourceGroupName</span></span>
<span data-ttu-id="01ea8-143">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="01ea8-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="01ea8-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="01ea8-144">-ResourceName</span></span>
<span data-ttu-id="01ea8-145">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="01ea8-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="01ea8-146">Например, чтобы указать базу данных, используйте следующий формат: `/` база данных сервера</span><span class="sxs-lookup"><span data-stu-id="01ea8-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="01ea8-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="01ea8-147">-ResourceType</span></span>
<span data-ttu-id="01ea8-148">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="01ea8-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="01ea8-149">-Scope</span><span class="sxs-lookup"><span data-stu-id="01ea8-149">-Scope</span></span>
<span data-ttu-id="01ea8-150">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="01ea8-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="01ea8-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="01ea8-151">-TenantLevel</span></span>
<span data-ttu-id="01ea8-152">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="01ea8-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="01ea8-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01ea8-153">-Confirm</span></span>
<span data-ttu-id="01ea8-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01ea8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01ea8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01ea8-155">-WhatIf</span></span>
<span data-ttu-id="01ea8-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01ea8-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01ea8-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01ea8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01ea8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ea8-158">CommonParameters</span></span>
<span data-ttu-id="01ea8-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01ea8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ea8-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01ea8-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ea8-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01ea8-161">INPUTS</span></span>

## <span data-ttu-id="01ea8-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01ea8-162">OUTPUTS</span></span>

## <span data-ttu-id="01ea8-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="01ea8-163">NOTES</span></span>

## <span data-ttu-id="01ea8-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01ea8-164">RELATED LINKS</span></span>

[<span data-ttu-id="01ea8-165">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="01ea8-165">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="01ea8-166">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="01ea8-166">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="01ea8-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="01ea8-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


