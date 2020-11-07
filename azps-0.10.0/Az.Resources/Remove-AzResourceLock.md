---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 6b9a0b792b1a8a5572ce26561202284f3103d764
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910844"
---
# <span data-ttu-id="2f8ab-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2f8ab-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="2f8ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="2f8ab-103">Удаление блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-103">Removes a resource lock.</span></span>

## <span data-ttu-id="2f8ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f8ab-104">SYNTAX</span></span>

### <span data-ttu-id="2f8ab-105">ByLockId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f8ab-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f8ab-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2f8ab-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f8ab-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="2f8ab-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f8ab-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="2f8ab-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f8ab-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="2f8ab-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f8ab-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="2f8ab-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f8ab-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="2f8ab-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f8ab-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f8ab-112">DESCRIPTION</span></span>
<span data-ttu-id="2f8ab-113">Командлет **Remove-AzResourceLock** удаляет блокировку ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="2f8ab-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f8ab-114">EXAMPLES</span></span>

### <span data-ttu-id="2f8ab-115">Пример 1: снятие блокировки</span><span class="sxs-lookup"><span data-stu-id="2f8ab-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="2f8ab-116">Эта команда удаляет блокировку с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="2f8ab-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f8ab-117">PARAMETERS</span></span>

### <span data-ttu-id="2f8ab-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2f8ab-118">-ApiVersion</span></span>
<span data-ttu-id="2f8ab-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2f8ab-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2f8ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f8ab-121">-DefaultProfile</span></span>
<span data-ttu-id="2f8ab-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2f8ab-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f8ab-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2f8ab-123">-Force</span></span>
<span data-ttu-id="2f8ab-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2f8ab-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2f8ab-125">-InformationAction</span></span>
<span data-ttu-id="2f8ab-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="2f8ab-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2f8ab-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f8ab-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="2f8ab-128">Continue</span></span>
- <span data-ttu-id="2f8ab-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="2f8ab-129">Ignore</span></span>
- <span data-ttu-id="2f8ab-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="2f8ab-130">Inquire</span></span>
- <span data-ttu-id="2f8ab-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2f8ab-131">SilentlyContinue</span></span>
- <span data-ttu-id="2f8ab-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="2f8ab-132">Stop</span></span>
- <span data-ttu-id="2f8ab-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="2f8ab-133">Suspend</span></span>

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

### <span data-ttu-id="2f8ab-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2f8ab-134">-InformationVariable</span></span>
<span data-ttu-id="2f8ab-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2f8ab-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="2f8ab-136">-LockId</span></span>
<span data-ttu-id="2f8ab-137">Указывает идентификатор блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f8ab-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="2f8ab-138">-LockName</span></span>
<span data-ttu-id="2f8ab-139">Указывает имя блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-139">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f8ab-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="2f8ab-140">-Pre</span></span>
<span data-ttu-id="2f8ab-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2f8ab-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f8ab-142">-ResourceGroupName</span></span>
<span data-ttu-id="2f8ab-143">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="2f8ab-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2f8ab-144">-ResourceName</span></span>
<span data-ttu-id="2f8ab-145">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="2f8ab-146">Например, чтобы указать базу данных, используйте следующий формат: `/` база данных сервера</span><span class="sxs-lookup"><span data-stu-id="2f8ab-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="2f8ab-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2f8ab-147">-ResourceType</span></span>
<span data-ttu-id="2f8ab-148">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="2f8ab-149">-Scope</span><span class="sxs-lookup"><span data-stu-id="2f8ab-149">-Scope</span></span>
<span data-ttu-id="2f8ab-150">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="2f8ab-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="2f8ab-151">-TenantLevel</span></span>
<span data-ttu-id="2f8ab-152">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="2f8ab-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f8ab-153">-Confirm</span></span>
<span data-ttu-id="2f8ab-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f8ab-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f8ab-155">-WhatIf</span></span>
<span data-ttu-id="2f8ab-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f8ab-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f8ab-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f8ab-158">CommonParameters</span></span>
<span data-ttu-id="2f8ab-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f8ab-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f8ab-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f8ab-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f8ab-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f8ab-161">INPUTS</span></span>

## <span data-ttu-id="2f8ab-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f8ab-162">OUTPUTS</span></span>

## <span data-ttu-id="2f8ab-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f8ab-163">NOTES</span></span>

## <span data-ttu-id="2f8ab-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f8ab-164">RELATED LINKS</span></span>

[<span data-ttu-id="2f8ab-165">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2f8ab-165">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="2f8ab-166">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2f8ab-166">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="2f8ab-167">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2f8ab-167">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


