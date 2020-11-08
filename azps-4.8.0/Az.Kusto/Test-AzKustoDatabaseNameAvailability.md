---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: ab15d7a9da10e7e7a024d3af332f449cd011a290
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079580"
---
# <span data-ttu-id="78702-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="78702-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="78702-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78702-102">SYNOPSIS</span></span>
<span data-ttu-id="78702-103">Проверяет, является ли имя базы данных допустимым и еще не используется.</span><span class="sxs-lookup"><span data-stu-id="78702-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="78702-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78702-104">SYNTAX</span></span>

### <span data-ttu-id="78702-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78702-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="78702-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="78702-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="78702-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78702-107">DESCRIPTION</span></span>
<span data-ttu-id="78702-108">Проверяет, является ли имя базы данных допустимым и еще не используется.</span><span class="sxs-lookup"><span data-stu-id="78702-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="78702-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78702-109">EXAMPLES</span></span>

### <span data-ttu-id="78702-110">Пример 1: Проверка доступности имени базы данных Kusto, которое используется</span><span class="sxs-lookup"><span data-stu-id="78702-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="78702-111">Указанная выше команда возвращает значение, указывающее, существует ли база данных Kusto с именем "mykustodatabase" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="78702-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="78702-112">Пример 2: Проверка доступности имени базы данных Kusto, которое не используется</span><span class="sxs-lookup"><span data-stu-id="78702-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="78702-113">Указанная выше команда возвращает значение, указывающее, существует ли база данных Kusto с именем "mykustodatabase2" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="78702-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="78702-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78702-114">PARAMETERS</span></span>

### <span data-ttu-id="78702-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="78702-115">-ClusterName</span></span>
<span data-ttu-id="78702-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="78702-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="78702-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78702-117">-DefaultProfile</span></span>
<span data-ttu-id="78702-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78702-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78702-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78702-119">-InputObject</span></span>
<span data-ttu-id="78702-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="78702-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="78702-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78702-121">-Name</span></span>
<span data-ttu-id="78702-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="78702-122">Resource name.</span></span>

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

### <span data-ttu-id="78702-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78702-123">-ResourceGroupName</span></span>
<span data-ttu-id="78702-124">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="78702-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="78702-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78702-125">-SubscriptionId</span></span>
<span data-ttu-id="78702-126">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="78702-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="78702-127">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="78702-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="78702-128">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="78702-128">-Type</span></span>
<span data-ttu-id="78702-129">Тип ресурса (например, Microsoft. Kusto/Clusters/databases).</span><span class="sxs-lookup"><span data-stu-id="78702-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="78702-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78702-130">-Confirm</span></span>
<span data-ttu-id="78702-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78702-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78702-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78702-132">-WhatIf</span></span>
<span data-ttu-id="78702-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78702-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78702-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78702-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78702-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78702-135">CommonParameters</span></span>
<span data-ttu-id="78702-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78702-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78702-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78702-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78702-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78702-138">INPUTS</span></span>

### <span data-ttu-id="78702-139">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="78702-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="78702-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78702-140">OUTPUTS</span></span>

### <span data-ttu-id="78702-141">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="78702-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="78702-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="78702-142">NOTES</span></span>

<span data-ttu-id="78702-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="78702-143">ALIASES</span></span>

<span data-ttu-id="78702-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="78702-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="78702-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="78702-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78702-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="78702-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="78702-147">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="78702-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="78702-148">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="78702-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="78702-149">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="78702-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="78702-150">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="78702-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="78702-151">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="78702-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="78702-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="78702-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="78702-153">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="78702-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="78702-154">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="78702-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="78702-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="78702-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="78702-156">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="78702-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="78702-157">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="78702-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="78702-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78702-158">RELATED LINKS</span></span>

