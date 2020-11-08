---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 556e0a7662a91c5c82bab7727bf676adf88d45d6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250173"
---
# <span data-ttu-id="bf251-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="bf251-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="bf251-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf251-102">SYNOPSIS</span></span>
<span data-ttu-id="bf251-103">Проверка того, что имя подключения к данным является допустимым и еще не используется.</span><span class="sxs-lookup"><span data-stu-id="bf251-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="bf251-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf251-104">SYNTAX</span></span>

### <span data-ttu-id="bf251-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf251-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bf251-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bf251-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bf251-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf251-107">DESCRIPTION</span></span>
<span data-ttu-id="bf251-108">Проверка того, что имя подключения к данным является допустимым и еще не используется.</span><span class="sxs-lookup"><span data-stu-id="bf251-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="bf251-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf251-109">EXAMPLES</span></span>

### <span data-ttu-id="bf251-110">Пример 1: Проверка доступности имени подключения к данным</span><span class="sxs-lookup"><span data-stu-id="bf251-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="bf251-111">Приведенная выше команда возвращает информацию о том, существует ли подключение к данным "mykustodataconnection" в базе данных "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="bf251-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="bf251-112">Пример 2: Проверка доступности имени подключения к данным, которое не используется</span><span class="sxs-lookup"><span data-stu-id="bf251-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="bf251-113">Приведенная выше команда возвращает информацию о том, существует ли подключение к данным "mydataconnection" в базе данных "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="bf251-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="bf251-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf251-114">PARAMETERS</span></span>

### <span data-ttu-id="bf251-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="bf251-115">-ClusterName</span></span>
<span data-ttu-id="bf251-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="bf251-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf251-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bf251-117">-DatabaseName</span></span>
<span data-ttu-id="bf251-118">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="bf251-118">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf251-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf251-119">-DefaultProfile</span></span>
<span data-ttu-id="bf251-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf251-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf251-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf251-121">-InputObject</span></span>
<span data-ttu-id="bf251-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="bf251-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf251-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf251-123">-Name</span></span>
<span data-ttu-id="bf251-124">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="bf251-124">Data Connection name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf251-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf251-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf251-126">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="bf251-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf251-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf251-127">-SubscriptionId</span></span>
<span data-ttu-id="bf251-128">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bf251-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bf251-129">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="bf251-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf251-130">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="bf251-130">-Type</span></span>
<span data-ttu-id="bf251-131">Тип ресурсов (Microsoft. Kusto/Clusters/databases/соединения).</span><span class="sxs-lookup"><span data-stu-id="bf251-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf251-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf251-132">-Confirm</span></span>
<span data-ttu-id="bf251-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bf251-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf251-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf251-134">-WhatIf</span></span>
<span data-ttu-id="bf251-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bf251-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf251-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bf251-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf251-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf251-137">CommonParameters</span></span>
<span data-ttu-id="bf251-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf251-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf251-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf251-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf251-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf251-140">INPUTS</span></span>

### <span data-ttu-id="bf251-141">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="bf251-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="bf251-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf251-142">OUTPUTS</span></span>

### <span data-ttu-id="bf251-143">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="bf251-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="bf251-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf251-144">NOTES</span></span>

<span data-ttu-id="bf251-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="bf251-145">ALIASES</span></span>

<span data-ttu-id="bf251-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="bf251-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bf251-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bf251-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf251-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf251-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bf251-149">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="bf251-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bf251-150">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="bf251-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="bf251-151">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="bf251-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="bf251-152">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="bf251-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="bf251-153">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="bf251-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="bf251-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="bf251-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bf251-155">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="bf251-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="bf251-156">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="bf251-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="bf251-157">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="bf251-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="bf251-158">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bf251-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bf251-159">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="bf251-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bf251-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf251-160">RELATED LINKS</span></span>

