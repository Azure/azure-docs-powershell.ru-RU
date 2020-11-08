---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 495561794485e259d81b2e611658be461233d36d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248977"
---
# <span data-ttu-id="3c270-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="3c270-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="3c270-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c270-102">SYNOPSIS</span></span>
<span data-ttu-id="3c270-103">Удалить разрешения участников базы данных.</span><span class="sxs-lookup"><span data-stu-id="3c270-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="3c270-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c270-104">SYNTAX</span></span>

### <span data-ttu-id="3c270-105">RemoveExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c270-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3c270-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3c270-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c270-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c270-107">DESCRIPTION</span></span>
<span data-ttu-id="3c270-108">Удалить разрешения участников базы данных.</span><span class="sxs-lookup"><span data-stu-id="3c270-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="3c270-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c270-109">EXAMPLES</span></span>

### <span data-ttu-id="3c270-110">Пример 1: удаление разрешений для базы данных</span><span class="sxs-lookup"><span data-stu-id="3c270-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="3c270-111">В приведенной выше команде удаляются разрешения участников базы данных</span><span class="sxs-lookup"><span data-stu-id="3c270-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="3c270-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c270-112">PARAMETERS</span></span>

### <span data-ttu-id="3c270-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="3c270-113">-ClusterName</span></span>
<span data-ttu-id="3c270-114">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c270-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3c270-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3c270-115">-DatabaseName</span></span>
<span data-ttu-id="3c270-116">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c270-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="3c270-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c270-117">-DefaultProfile</span></span>
<span data-ttu-id="3c270-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c270-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c270-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c270-119">-InputObject</span></span>
<span data-ttu-id="3c270-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3c270-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c270-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c270-121">-ResourceGroupName</span></span>
<span data-ttu-id="3c270-122">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c270-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3c270-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c270-123">-SubscriptionId</span></span>
<span data-ttu-id="3c270-124">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c270-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3c270-125">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3c270-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3c270-126">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="3c270-126">-Value</span></span>
<span data-ttu-id="3c270-127">Список участников базы данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c270-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="3c270-128">Для конструирования ознакомьтесь с разделом "Заметки" для свойств значения и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3c270-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c270-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c270-129">-Confirm</span></span>
<span data-ttu-id="3c270-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c270-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c270-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c270-131">-WhatIf</span></span>
<span data-ttu-id="3c270-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c270-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c270-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c270-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c270-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c270-134">CommonParameters</span></span>
<span data-ttu-id="3c270-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c270-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c270-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c270-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c270-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c270-137">INPUTS</span></span>

### <span data-ttu-id="3c270-138">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3c270-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3c270-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c270-139">OUTPUTS</span></span>

### <span data-ttu-id="3c270-140">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="3c270-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="3c270-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c270-141">NOTES</span></span>

<span data-ttu-id="3c270-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3c270-142">ALIASES</span></span>

<span data-ttu-id="3c270-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3c270-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c270-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3c270-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c270-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c270-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c270-146">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="3c270-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c270-147">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3c270-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3c270-148">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c270-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3c270-149">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="3c270-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3c270-150">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c270-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3c270-151">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="3c270-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c270-152">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="3c270-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3c270-153">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="3c270-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3c270-154">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c270-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3c270-155">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c270-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3c270-156">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3c270-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="3c270-157">VALUE (значение) <IDatabasePrincipal [] >: список участников базы данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="3c270-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="3c270-158">`Name <String>`: Имя участника базы данных.</span><span class="sxs-lookup"><span data-stu-id="3c270-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="3c270-159">`Role <DatabasePrincipalRole>`: Роль участника базы данных.</span><span class="sxs-lookup"><span data-stu-id="3c270-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="3c270-160">`Type <DatabasePrincipalType>`: Тип участника базы данных.</span><span class="sxs-lookup"><span data-stu-id="3c270-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="3c270-161">`[AppId <String>]`: Идентификатор приложения — применяется только для типа участника приложения.</span><span class="sxs-lookup"><span data-stu-id="3c270-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="3c270-162">`[Email <String>]`: Сообщение участника базы данных, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="3c270-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="3c270-163">`[Fqn <String>]`: Полное имя участника базы данных.</span><span class="sxs-lookup"><span data-stu-id="3c270-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="3c270-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c270-164">RELATED LINKS</span></span>

