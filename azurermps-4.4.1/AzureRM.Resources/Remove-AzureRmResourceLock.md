---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c45d78b815586e54c9f39cfd536fed5a26c2eb19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567059"
---
# <span data-ttu-id="9cb24-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9cb24-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="9cb24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cb24-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb24-103">Удаление блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="9cb24-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cb24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cb24-104">SYNTAX</span></span>

### <span data-ttu-id="9cb24-105">Блокировка по идентификатору. (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9cb24-105">A lock, by Id. (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb24-106">Блокировка в области действия группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9cb24-106">A lock at the resource group scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb24-107">Блокировка в области ресурсов "Группа ресурсов".</span><span class="sxs-lookup"><span data-stu-id="9cb24-107">A lock at the resource group resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cb24-108">Блокировка на указанном уровне.</span><span class="sxs-lookup"><span data-stu-id="9cb24-108">A lock at the specified scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb24-109">Блокировка в области подписки.</span><span class="sxs-lookup"><span data-stu-id="9cb24-109">A lock at the subscription scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb24-110">Блокировка в области ресурсов подписки.</span><span class="sxs-lookup"><span data-stu-id="9cb24-110">A lock at the subscription resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cb24-111">Блокировка в области ресурсов клиента.</span><span class="sxs-lookup"><span data-stu-id="9cb24-111">A lock at the tenant resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cb24-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cb24-112">DESCRIPTION</span></span>
<span data-ttu-id="9cb24-113">Командлет **Remove-AzureRmResourceLock** удаляет блокировку ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb24-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="9cb24-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cb24-114">EXAMPLES</span></span>

### <span data-ttu-id="9cb24-115">Пример 1: снятие блокировки</span><span class="sxs-lookup"><span data-stu-id="9cb24-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="9cb24-116">Эта команда удаляет блокировку с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="9cb24-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="9cb24-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cb24-117">PARAMETERS</span></span>

### <span data-ttu-id="9cb24-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9cb24-118">-ApiVersion</span></span>
<span data-ttu-id="9cb24-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9cb24-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9cb24-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="9cb24-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9cb24-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9cb24-121">-Force</span></span>
<span data-ttu-id="9cb24-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9cb24-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9cb24-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9cb24-123">-InformationAction</span></span>
<span data-ttu-id="9cb24-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="9cb24-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9cb24-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9cb24-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9cb24-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="9cb24-126">Continue</span></span>
- <span data-ttu-id="9cb24-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="9cb24-127">Ignore</span></span>
- <span data-ttu-id="9cb24-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="9cb24-128">Inquire</span></span>
- <span data-ttu-id="9cb24-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9cb24-129">SilentlyContinue</span></span>
- <span data-ttu-id="9cb24-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="9cb24-130">Stop</span></span>
- <span data-ttu-id="9cb24-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="9cb24-131">Suspend</span></span>

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

### <span data-ttu-id="9cb24-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9cb24-132">-InformationVariable</span></span>
<span data-ttu-id="9cb24-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="9cb24-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9cb24-134">-LockId</span><span class="sxs-lookup"><span data-stu-id="9cb24-134">-LockId</span></span>
<span data-ttu-id="9cb24-135">Указывает идентификатор блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cb24-135">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9cb24-136">-LockName</span><span class="sxs-lookup"><span data-stu-id="9cb24-136">-LockName</span></span>
<span data-ttu-id="9cb24-137">Указывает имя блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cb24-137">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb24-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="9cb24-138">-Pre</span></span>
<span data-ttu-id="9cb24-139">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="9cb24-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9cb24-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb24-140">-ResourceGroupName</span></span>
<span data-ttu-id="9cb24-141">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="9cb24-141">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="9cb24-142">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9cb24-142">-ResourceName</span></span>
<span data-ttu-id="9cb24-143">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="9cb24-143">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="9cb24-144">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="9cb24-144">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="9cb24-145">`/`База данных сервера</span><span class="sxs-lookup"><span data-stu-id="9cb24-145">Server`/`Database</span></span>

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

### <span data-ttu-id="9cb24-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9cb24-146">-ResourceType</span></span>
<span data-ttu-id="9cb24-147">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="9cb24-147">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="9cb24-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="9cb24-148">-Scope</span></span>
<span data-ttu-id="9cb24-149">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="9cb24-149">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="9cb24-150">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9cb24-150">-TenantLevel</span></span>
<span data-ttu-id="9cb24-151">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="9cb24-151">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="9cb24-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cb24-152">-Confirm</span></span>
<span data-ttu-id="9cb24-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9cb24-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb24-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb24-154">-WhatIf</span></span>
<span data-ttu-id="9cb24-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9cb24-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb24-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9cb24-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb24-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb24-157">-DefaultProfile</span></span>
<span data-ttu-id="9cb24-158">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb24-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cb24-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb24-159">CommonParameters</span></span>
<span data-ttu-id="9cb24-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cb24-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb24-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cb24-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb24-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cb24-162">INPUTS</span></span>

## <span data-ttu-id="9cb24-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cb24-163">OUTPUTS</span></span>

### <span data-ttu-id="9cb24-164">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9cb24-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9cb24-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cb24-165">NOTES</span></span>

## <span data-ttu-id="9cb24-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cb24-166">RELATED LINKS</span></span>

[<span data-ttu-id="9cb24-167">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9cb24-167">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="9cb24-168">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9cb24-168">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="9cb24-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9cb24-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


