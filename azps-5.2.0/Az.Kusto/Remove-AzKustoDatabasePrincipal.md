---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 495561794485e259d81b2e611658be461233d36d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399303"
---
# <span data-ttu-id="dd588-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="dd588-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="dd588-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd588-102">SYNOPSIS</span></span>
<span data-ttu-id="dd588-103">Удаление разрешений для основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd588-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="dd588-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dd588-104">SYNTAX</span></span>

### <span data-ttu-id="dd588-105">RemoveExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd588-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="dd588-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dd588-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd588-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd588-107">DESCRIPTION</span></span>
<span data-ttu-id="dd588-108">Удаление разрешений для основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd588-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="dd588-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dd588-109">EXAMPLES</span></span>

### <span data-ttu-id="dd588-110">Пример 1. Удаление разрешений для основной базы данных</span><span class="sxs-lookup"><span data-stu-id="dd588-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="dd588-111">С использованием этой команды удаляются разрешения уровня "Основные манды базы данных".</span><span class="sxs-lookup"><span data-stu-id="dd588-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="dd588-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd588-112">PARAMETERS</span></span>

### <span data-ttu-id="dd588-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dd588-113">-ClusterName</span></span>
<span data-ttu-id="dd588-114">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="dd588-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd588-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd588-115">-DatabaseName</span></span>
<span data-ttu-id="dd588-116">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="dd588-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd588-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd588-117">-DefaultProfile</span></span>
<span data-ttu-id="dd588-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd588-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd588-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd588-119">-InputObject</span></span>
<span data-ttu-id="dd588-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="dd588-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd588-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd588-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd588-122">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="dd588-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd588-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd588-123">-SubscriptionId</span></span>
<span data-ttu-id="dd588-124">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dd588-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd588-125">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="dd588-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd588-126">-Value</span><span class="sxs-lookup"><span data-stu-id="dd588-126">-Value</span></span>
<span data-ttu-id="dd588-127">Список глав баз данных "Кузто".</span><span class="sxs-lookup"><span data-stu-id="dd588-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="dd588-128">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств VALUE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="dd588-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd588-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd588-129">-Confirm</span></span>
<span data-ttu-id="dd588-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dd588-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd588-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd588-131">-WhatIf</span></span>
<span data-ttu-id="dd588-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd588-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd588-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dd588-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd588-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd588-134">CommonParameters</span></span>
<span data-ttu-id="dd588-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd588-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd588-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd588-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd588-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd588-137">INPUTS</span></span>

### <span data-ttu-id="dd588-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="dd588-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="dd588-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd588-139">OUTPUTS</span></span>

### <span data-ttu-id="dd588-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="dd588-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="dd588-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dd588-141">NOTES</span></span>

<span data-ttu-id="dd588-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dd588-142">ALIASES</span></span>

<span data-ttu-id="dd588-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="dd588-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd588-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="dd588-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd588-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd588-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd588-146">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="dd588-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd588-147">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd588-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="dd588-148">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="dd588-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="dd588-149">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="dd588-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="dd588-150">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="dd588-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="dd588-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="dd588-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd588-152">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="dd588-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="dd588-153">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="dd588-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="dd588-154">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="dd588-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="dd588-155">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dd588-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dd588-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="dd588-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="dd588-157">VALUE <IDatabasePrincipal[]>: список глав баз данных Кусто.</span><span class="sxs-lookup"><span data-stu-id="dd588-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="dd588-158">`Name <String>`: имя основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd588-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="dd588-159">`Role <DatabasePrincipalRole>`: роль основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd588-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="dd588-160">`Type <DatabasePrincipalType>`: Тип основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd588-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="dd588-161">`[AppId <String>]`: Application id — релевантный только для типа основной программы.</span><span class="sxs-lookup"><span data-stu-id="dd588-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="dd588-162">`[Email <String>]`: адрес электронной почты основной базы данных, если он существует.</span><span class="sxs-lookup"><span data-stu-id="dd588-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="dd588-163">`[Fqn <String>]`: полное имя основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd588-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="dd588-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd588-164">RELATED LINKS</span></span>

