---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248989"
---
# <span data-ttu-id="34f9b-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="34f9b-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="34f9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="34f9b-103">Удаляет конфигурацию присоединенной базы данных с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="34f9b-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="34f9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34f9b-104">SYNTAX</span></span>

### <span data-ttu-id="34f9b-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34f9b-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="34f9b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="34f9b-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34f9b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34f9b-107">DESCRIPTION</span></span>
<span data-ttu-id="34f9b-108">Удаляет конфигурацию присоединенной базы данных с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="34f9b-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="34f9b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34f9b-109">EXAMPLES</span></span>

### <span data-ttu-id="34f9b-110">Пример 1: удаление существующего AttachedDatabaseConfiguration по имени</span><span class="sxs-lookup"><span data-stu-id="34f9b-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="34f9b-111">Вышеприведенная команда удаляет базу данных, которая определена в AttachedDatabaseConfiguration "myfollowerconfiguration" из кластера "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="34f9b-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="34f9b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34f9b-112">PARAMETERS</span></span>

### <span data-ttu-id="34f9b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34f9b-113">-AsJob</span></span>
<span data-ttu-id="34f9b-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="34f9b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="34f9b-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="34f9b-115">-ClusterName</span></span>
<span data-ttu-id="34f9b-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="34f9b-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="34f9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f9b-117">-DefaultProfile</span></span>
<span data-ttu-id="34f9b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34f9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34f9b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34f9b-119">-InputObject</span></span>
<span data-ttu-id="34f9b-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="34f9b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34f9b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34f9b-121">-Name</span></span>
<span data-ttu-id="34f9b-122">Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="34f9b-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f9b-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="34f9b-123">-NoWait</span></span>
<span data-ttu-id="34f9b-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="34f9b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="34f9b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34f9b-125">-PassThru</span></span>
<span data-ttu-id="34f9b-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="34f9b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="34f9b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f9b-127">-ResourceGroupName</span></span>
<span data-ttu-id="34f9b-128">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="34f9b-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="34f9b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34f9b-129">-SubscriptionId</span></span>
<span data-ttu-id="34f9b-130">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="34f9b-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="34f9b-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="34f9b-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="34f9b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34f9b-132">-Confirm</span></span>
<span data-ttu-id="34f9b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34f9b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34f9b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f9b-134">-WhatIf</span></span>
<span data-ttu-id="34f9b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34f9b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f9b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34f9b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34f9b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f9b-137">CommonParameters</span></span>
<span data-ttu-id="34f9b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34f9b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f9b-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34f9b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f9b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34f9b-140">INPUTS</span></span>

### <span data-ttu-id="34f9b-141">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="34f9b-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="34f9b-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34f9b-142">OUTPUTS</span></span>

### <span data-ttu-id="34f9b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34f9b-143">System.Boolean</span></span>

## <span data-ttu-id="34f9b-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="34f9b-144">NOTES</span></span>

<span data-ttu-id="34f9b-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="34f9b-145">ALIASES</span></span>

<span data-ttu-id="34f9b-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="34f9b-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34f9b-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="34f9b-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34f9b-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34f9b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34f9b-149">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="34f9b-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34f9b-150">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="34f9b-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="34f9b-151">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="34f9b-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="34f9b-152">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="34f9b-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="34f9b-153">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="34f9b-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="34f9b-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="34f9b-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34f9b-155">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="34f9b-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="34f9b-156">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="34f9b-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="34f9b-157">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="34f9b-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="34f9b-158">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="34f9b-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="34f9b-159">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="34f9b-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="34f9b-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34f9b-160">RELATED LINKS</span></span>
