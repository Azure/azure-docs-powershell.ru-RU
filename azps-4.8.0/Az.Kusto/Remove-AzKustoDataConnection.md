---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078215"
---
# <span data-ttu-id="67688-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="67688-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="67688-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67688-102">SYNOPSIS</span></span>
<span data-ttu-id="67688-103">Удаляет подключение к данным с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="67688-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="67688-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67688-104">SYNTAX</span></span>

### <span data-ttu-id="67688-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67688-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="67688-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="67688-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="67688-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67688-107">DESCRIPTION</span></span>
<span data-ttu-id="67688-108">Удаляет подключение к данным с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="67688-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="67688-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67688-109">EXAMPLES</span></span>

### <span data-ttu-id="67688-110">Пример 1: удаление существующего подключения к данным с помощью имени</span><span class="sxs-lookup"><span data-stu-id="67688-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="67688-111">Вышеприведенная команда удаляет подключение к данным "mykustodataconnection" в базе данных "mykustodatabase" существующего кластера "testnewkustocluster", обнаруженного в группе ресурсов "testrg"</span><span class="sxs-lookup"><span data-stu-id="67688-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="67688-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67688-112">PARAMETERS</span></span>

### <span data-ttu-id="67688-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67688-113">-AsJob</span></span>
<span data-ttu-id="67688-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="67688-114">Run the command as a job</span></span>

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

### <span data-ttu-id="67688-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="67688-115">-ClusterName</span></span>
<span data-ttu-id="67688-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="67688-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="67688-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67688-117">-DatabaseName</span></span>
<span data-ttu-id="67688-118">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="67688-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="67688-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67688-119">-DefaultProfile</span></span>
<span data-ttu-id="67688-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67688-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67688-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67688-121">-InputObject</span></span>
<span data-ttu-id="67688-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="67688-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="67688-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="67688-123">-Name</span></span>
<span data-ttu-id="67688-124">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="67688-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67688-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="67688-125">-NoWait</span></span>
<span data-ttu-id="67688-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="67688-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="67688-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67688-127">-PassThru</span></span>
<span data-ttu-id="67688-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="67688-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="67688-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67688-129">-ResourceGroupName</span></span>
<span data-ttu-id="67688-130">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="67688-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="67688-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67688-131">-SubscriptionId</span></span>
<span data-ttu-id="67688-132">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67688-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="67688-133">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="67688-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="67688-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67688-134">-Confirm</span></span>
<span data-ttu-id="67688-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67688-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67688-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67688-136">-WhatIf</span></span>
<span data-ttu-id="67688-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67688-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67688-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67688-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67688-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67688-139">CommonParameters</span></span>
<span data-ttu-id="67688-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67688-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67688-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67688-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67688-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67688-142">INPUTS</span></span>

### <span data-ttu-id="67688-143">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="67688-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="67688-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67688-144">OUTPUTS</span></span>

### <span data-ttu-id="67688-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67688-145">System.Boolean</span></span>

## <span data-ttu-id="67688-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="67688-146">NOTES</span></span>

<span data-ttu-id="67688-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="67688-147">ALIASES</span></span>

<span data-ttu-id="67688-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="67688-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67688-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="67688-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67688-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67688-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67688-151">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="67688-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67688-152">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="67688-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="67688-153">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="67688-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="67688-154">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="67688-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="67688-155">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="67688-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="67688-156">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="67688-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67688-157">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="67688-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="67688-158">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="67688-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="67688-159">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="67688-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="67688-160">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67688-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="67688-161">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="67688-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="67688-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67688-162">RELATED LINKS</span></span>

