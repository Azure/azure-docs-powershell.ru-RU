---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/add-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c01d481b5ee9351de0b099a144a709c89a3990ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964579"
---
# <span data-ttu-id="cc765-101">Add-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="cc765-101">Add-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="cc765-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc765-102">SYNOPSIS</span></span>
<span data-ttu-id="cc765-103">"Добавить разрешения для основной базы данных".</span><span class="sxs-lookup"><span data-stu-id="cc765-103">Add Database principals permissions.</span></span>

## <span data-ttu-id="cc765-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc765-104">SYNTAX</span></span>

### <span data-ttu-id="cc765-105">AddExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc765-105">AddExpanded (Default)</span></span>
```
Add-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cc765-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cc765-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc765-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc765-107">DESCRIPTION</span></span>
<span data-ttu-id="cc765-108">"Добавить разрешения для основной базы данных".</span><span class="sxs-lookup"><span data-stu-id="cc765-108">Add Database principals permissions.</span></span>

## <span data-ttu-id="cc765-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc765-109">EXAMPLES</span></span>

### <span data-ttu-id="cc765-110">Пример 1. Добавление разрешений для основной базы данных</span><span class="sxs-lookup"><span data-stu-id="cc765-110">Example 1: Add Database principals permissions</span></span>
```powershell
PS C:\> Add-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="cc765-111">Вышеуказанная команда добавляет разрешения "Основные манды базы данных"</span><span class="sxs-lookup"><span data-stu-id="cc765-111">The above command adds Database principals permissions</span></span>

## <span data-ttu-id="cc765-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc765-112">PARAMETERS</span></span>

### <span data-ttu-id="cc765-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cc765-113">-ClusterName</span></span>
<span data-ttu-id="cc765-114">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="cc765-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc765-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc765-115">-DatabaseName</span></span>
<span data-ttu-id="cc765-116">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="cc765-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc765-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc765-117">-DefaultProfile</span></span>
<span data-ttu-id="cc765-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc765-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc765-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc765-119">-InputObject</span></span>
<span data-ttu-id="cc765-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="cc765-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc765-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc765-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc765-122">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="cc765-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc765-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc765-123">-SubscriptionId</span></span>
<span data-ttu-id="cc765-124">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc765-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cc765-125">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="cc765-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc765-126">-Значение</span><span class="sxs-lookup"><span data-stu-id="cc765-126">-Value</span></span>
<span data-ttu-id="cc765-127">Список глав баз данных "Кузто".</span><span class="sxs-lookup"><span data-stu-id="cc765-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="cc765-128">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств VALUE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="cc765-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc765-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc765-129">-Confirm</span></span>
<span data-ttu-id="cc765-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cc765-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc765-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc765-131">-WhatIf</span></span>
<span data-ttu-id="cc765-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc765-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc765-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc765-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc765-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc765-134">CommonParameters</span></span>
<span data-ttu-id="cc765-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc765-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc765-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc765-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc765-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc765-137">INPUTS</span></span>

### <span data-ttu-id="cc765-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cc765-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cc765-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc765-139">OUTPUTS</span></span>

### <span data-ttu-id="cc765-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="cc765-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="cc765-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc765-141">NOTES</span></span>

<span data-ttu-id="cc765-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cc765-142">ALIASES</span></span>

<span data-ttu-id="cc765-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="cc765-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc765-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="cc765-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc765-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc765-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc765-146">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="cc765-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cc765-147">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc765-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cc765-148">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="cc765-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cc765-149">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="cc765-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cc765-150">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="cc765-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cc765-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="cc765-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc765-152">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="cc765-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cc765-153">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="cc765-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cc765-154">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="cc765-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cc765-155">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc765-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cc765-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="cc765-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="cc765-157">VALUE <IDatabasePrincipal[]>: список основных лиц базы данных "Кузто".</span><span class="sxs-lookup"><span data-stu-id="cc765-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="cc765-158">`Name <String>`: имя основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc765-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="cc765-159">`Role <DatabasePrincipalRole>`: роль основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc765-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="cc765-160">`Type <DatabasePrincipalType>`: Тип основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc765-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="cc765-161">`[AppId <String>]`: Application id — релевантный только для типа основной программы.</span><span class="sxs-lookup"><span data-stu-id="cc765-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="cc765-162">`[Email <String>]`: адрес электронной почты основной базы данных, если он существует.</span><span class="sxs-lookup"><span data-stu-id="cc765-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="cc765-163">`[Fqn <String>]`: полное имя основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc765-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="cc765-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc765-164">RELATED LINKS</span></span>

