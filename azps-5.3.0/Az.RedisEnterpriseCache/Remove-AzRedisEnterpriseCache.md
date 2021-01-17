---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: 22d0fed7c72aa5754b7393cdf06fb58a4bfc0db3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421167"
---
# <span data-ttu-id="1ace1-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="1ace1-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="1ace1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ace1-102">SYNOPSIS</span></span>
<span data-ttu-id="1ace1-103">Удаляет кластер кэша RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1ace1-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="1ace1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ace1-104">SYNTAX</span></span>

### <span data-ttu-id="1ace1-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1ace1-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1ace1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1ace1-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ace1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ace1-107">DESCRIPTION</span></span>
<span data-ttu-id="1ace1-108">Удаляет кластер кэша RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1ace1-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="1ace1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ace1-109">EXAMPLES</span></span>

### <span data-ttu-id="1ace1-110">Пример 1. Удаление корпоративного кэша Redis и возврат результата</span><span class="sxs-lookup"><span data-stu-id="1ace1-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="1ace1-111">Эта команда удаляет кэш Redis Enterprise и показывает, успешно ли операция.</span><span class="sxs-lookup"><span data-stu-id="1ace1-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="1ace1-112">Пример 2. Удаление корпоративного кэша Redis без отображения результата</span><span class="sxs-lookup"><span data-stu-id="1ace1-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="1ace1-113">Эта команда удаляет кэш Redis Enterprise.</span><span class="sxs-lookup"><span data-stu-id="1ace1-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="1ace1-114">Так как параметр PassThru не указан, результат операции не отображается.</span><span class="sxs-lookup"><span data-stu-id="1ace1-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="1ace1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ace1-115">PARAMETERS</span></span>

### <span data-ttu-id="1ace1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ace1-116">-AsJob</span></span>
<span data-ttu-id="1ace1-117">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="1ace1-117">Run the command as a job</span></span>

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

### <span data-ttu-id="1ace1-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1ace1-118">-ClusterName</span></span>
<span data-ttu-id="1ace1-119">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1ace1-119">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ace1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ace1-120">-DefaultProfile</span></span>
<span data-ttu-id="1ace1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ace1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ace1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ace1-122">-InputObject</span></span>
<span data-ttu-id="1ace1-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="1ace1-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ace1-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1ace1-124">-NoWait</span></span>
<span data-ttu-id="1ace1-125">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="1ace1-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1ace1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ace1-126">-PassThru</span></span>
<span data-ttu-id="1ace1-127">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="1ace1-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1ace1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ace1-128">-ResourceGroupName</span></span>
<span data-ttu-id="1ace1-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ace1-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ace1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ace1-130">-SubscriptionId</span></span>
<span data-ttu-id="1ace1-131">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ace1-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ace1-132">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1ace1-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ace1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ace1-133">-Confirm</span></span>
<span data-ttu-id="1ace1-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ace1-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ace1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ace1-135">-WhatIf</span></span>
<span data-ttu-id="1ace1-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ace1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ace1-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1ace1-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ace1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ace1-138">CommonParameters</span></span>
<span data-ttu-id="1ace1-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ace1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ace1-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ace1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ace1-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ace1-141">INPUTS</span></span>

### <span data-ttu-id="1ace1-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="1ace1-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="1ace1-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ace1-143">OUTPUTS</span></span>

### <span data-ttu-id="1ace1-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ace1-144">System.Boolean</span></span>

## <span data-ttu-id="1ace1-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ace1-145">NOTES</span></span>

<span data-ttu-id="1ace1-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1ace1-146">ALIASES</span></span>

<span data-ttu-id="1ace1-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1ace1-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ace1-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="1ace1-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ace1-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1ace1-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ace1-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="1ace1-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ace1-151">`[ClusterName <String>]`: Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1ace1-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="1ace1-152">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="1ace1-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1ace1-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="1ace1-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ace1-154">`[Location <String>]`Регион, в который она веется.</span><span class="sxs-lookup"><span data-stu-id="1ace1-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="1ace1-155">`[OperationId <String>]`: уникальный идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="1ace1-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="1ace1-156">`[PrivateEndpointConnectionName <String>]`: имя подключения частной конечной точки, связанного с ресурсом Azure</span><span class="sxs-lookup"><span data-stu-id="1ace1-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="1ace1-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ace1-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1ace1-158">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ace1-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="1ace1-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1ace1-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1ace1-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ace1-160">RELATED LINKS</span></span>

