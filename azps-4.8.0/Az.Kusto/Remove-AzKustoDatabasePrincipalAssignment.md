---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078213"
---
# <span data-ttu-id="0d476-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0d476-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="0d476-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d476-102">SYNOPSIS</span></span>
<span data-ttu-id="0d476-103">Удаление Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0d476-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="0d476-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d476-104">SYNTAX</span></span>

### <span data-ttu-id="0d476-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d476-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0d476-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d476-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d476-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d476-107">DESCRIPTION</span></span>
<span data-ttu-id="0d476-108">Удаление Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0d476-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="0d476-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d476-109">EXAMPLES</span></span>

### <span data-ttu-id="0d476-110">Пример 1: удаление существующей базы данных Kusto PrincipalAssignment по имени</span><span class="sxs-lookup"><span data-stu-id="0d476-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="0d476-111">В приведенной выше команде удаляется PrincipalAssignment с именем "kustoprincipal1" в базе данных Kusto "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="0d476-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="0d476-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d476-112">PARAMETERS</span></span>

### <span data-ttu-id="0d476-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d476-113">-AsJob</span></span>
<span data-ttu-id="0d476-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0d476-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0d476-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="0d476-115">-ClusterName</span></span>
<span data-ttu-id="0d476-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="0d476-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0d476-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d476-117">-DatabaseName</span></span>
<span data-ttu-id="0d476-118">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="0d476-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="0d476-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d476-119">-DefaultProfile</span></span>
<span data-ttu-id="0d476-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d476-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d476-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d476-121">-InputObject</span></span>
<span data-ttu-id="0d476-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="0d476-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0d476-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="0d476-123">-NoWait</span></span>
<span data-ttu-id="0d476-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="0d476-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0d476-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d476-125">-PassThru</span></span>
<span data-ttu-id="0d476-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0d476-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0d476-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0d476-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="0d476-128">Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0d476-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="0d476-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d476-129">-ResourceGroupName</span></span>
<span data-ttu-id="0d476-130">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="0d476-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0d476-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d476-131">-SubscriptionId</span></span>
<span data-ttu-id="0d476-132">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0d476-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0d476-133">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="0d476-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0d476-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d476-134">-Confirm</span></span>
<span data-ttu-id="0d476-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d476-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d476-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d476-136">-WhatIf</span></span>
<span data-ttu-id="0d476-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d476-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d476-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d476-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d476-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d476-139">CommonParameters</span></span>
<span data-ttu-id="0d476-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d476-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d476-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d476-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d476-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d476-142">INPUTS</span></span>

### <span data-ttu-id="0d476-143">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0d476-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0d476-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d476-144">OUTPUTS</span></span>

### <span data-ttu-id="0d476-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d476-145">System.Boolean</span></span>

## <span data-ttu-id="0d476-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d476-146">NOTES</span></span>

<span data-ttu-id="0d476-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0d476-147">ALIASES</span></span>

<span data-ttu-id="0d476-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0d476-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d476-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0d476-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d476-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d476-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d476-151">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="0d476-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d476-152">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="0d476-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0d476-153">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="0d476-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0d476-154">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="0d476-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0d476-155">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="0d476-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0d476-156">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="0d476-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d476-157">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="0d476-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0d476-158">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0d476-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0d476-159">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="0d476-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0d476-160">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0d476-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0d476-161">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="0d476-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0d476-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d476-162">RELATED LINKS</span></span>

