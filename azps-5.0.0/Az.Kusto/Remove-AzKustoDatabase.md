---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248976"
---
# <span data-ttu-id="3e311-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="3e311-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="3e311-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e311-102">SYNOPSIS</span></span>
<span data-ttu-id="3e311-103">Удаляет базу данных с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="3e311-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="3e311-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e311-104">SYNTAX</span></span>

### <span data-ttu-id="3e311-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e311-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3e311-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3e311-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3e311-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e311-107">DESCRIPTION</span></span>
<span data-ttu-id="3e311-108">Удаляет базу данных с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="3e311-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="3e311-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e311-109">EXAMPLES</span></span>

### <span data-ttu-id="3e311-110">Пример 1: удаление существующей базы данных Kusto по имени</span><span class="sxs-lookup"><span data-stu-id="3e311-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="3e311-111">Вышеприведенная команда удаляет базу данных Kusto с именем "mykustodatabase" в кластере "testnewkustocluster", обнаруженную в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="3e311-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="3e311-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e311-112">PARAMETERS</span></span>

### <span data-ttu-id="3e311-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e311-113">-AsJob</span></span>
<span data-ttu-id="3e311-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3e311-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3e311-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="3e311-115">-ClusterName</span></span>
<span data-ttu-id="3e311-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="3e311-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3e311-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e311-117">-DefaultProfile</span></span>
<span data-ttu-id="3e311-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e311-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e311-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e311-119">-InputObject</span></span>
<span data-ttu-id="3e311-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3e311-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3e311-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e311-121">-Name</span></span>
<span data-ttu-id="3e311-122">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="3e311-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e311-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="3e311-123">-NoWait</span></span>
<span data-ttu-id="3e311-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="3e311-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3e311-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e311-125">-PassThru</span></span>
<span data-ttu-id="3e311-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3e311-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3e311-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e311-127">-ResourceGroupName</span></span>
<span data-ttu-id="3e311-128">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="3e311-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3e311-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e311-129">-SubscriptionId</span></span>
<span data-ttu-id="3e311-130">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e311-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e311-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3e311-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3e311-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e311-132">-Confirm</span></span>
<span data-ttu-id="3e311-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e311-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e311-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e311-134">-WhatIf</span></span>
<span data-ttu-id="3e311-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e311-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e311-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e311-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e311-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e311-137">CommonParameters</span></span>
<span data-ttu-id="3e311-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e311-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e311-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e311-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e311-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e311-140">INPUTS</span></span>

### <span data-ttu-id="3e311-141">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3e311-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3e311-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e311-142">OUTPUTS</span></span>

### <span data-ttu-id="3e311-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e311-143">System.Boolean</span></span>

## <span data-ttu-id="3e311-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e311-144">NOTES</span></span>

<span data-ttu-id="3e311-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3e311-145">ALIASES</span></span>

<span data-ttu-id="3e311-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3e311-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3e311-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e311-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e311-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e311-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3e311-149">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="3e311-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e311-150">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3e311-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3e311-151">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="3e311-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3e311-152">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="3e311-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3e311-153">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="3e311-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3e311-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="3e311-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e311-155">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="3e311-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3e311-156">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="3e311-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3e311-157">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="3e311-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3e311-158">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e311-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3e311-159">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3e311-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3e311-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e311-160">RELATED LINKS</span></span>

