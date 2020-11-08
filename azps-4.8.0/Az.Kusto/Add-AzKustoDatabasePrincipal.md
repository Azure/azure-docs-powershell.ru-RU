---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoDatabasePrincipal.md
ms.openlocfilehash: d7af2877d4823f1da85f08e61035b386d57a9c2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236326"
---
# <span data-ttu-id="ad0bf-101">Add-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="ad0bf-101">Add-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="ad0bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad0bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0bf-103">Добавьте разрешения для участников базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-103">Add Database principals permissions.</span></span>

## <span data-ttu-id="ad0bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad0bf-104">SYNTAX</span></span>

### <span data-ttu-id="ad0bf-105">AddExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad0bf-105">AddExpanded (Default)</span></span>
```
Add-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ad0bf-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ad0bf-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ad0bf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad0bf-107">DESCRIPTION</span></span>
<span data-ttu-id="ad0bf-108">Добавьте разрешения для участников базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-108">Add Database principals permissions.</span></span>

## <span data-ttu-id="ad0bf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad0bf-109">EXAMPLES</span></span>

### <span data-ttu-id="ad0bf-110">Пример 1: Добавление участников базы данных с разрешениями</span><span class="sxs-lookup"><span data-stu-id="ad0bf-110">Example 1: Add Database principals permissions</span></span>
```powershell
PS C:\> Add-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="ad0bf-111">Приведенная выше команда добавляет разрешения участников базы данных</span><span class="sxs-lookup"><span data-stu-id="ad0bf-111">The above command adds Database principals permissions</span></span>

## <span data-ttu-id="ad0bf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad0bf-112">PARAMETERS</span></span>

### <span data-ttu-id="ad0bf-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ad0bf-113">-ClusterName</span></span>
<span data-ttu-id="ad0bf-114">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ad0bf-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad0bf-115">-DatabaseName</span></span>
<span data-ttu-id="ad0bf-116">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ad0bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0bf-117">-DefaultProfile</span></span>
<span data-ttu-id="ad0bf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad0bf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad0bf-119">-InputObject</span></span>
<span data-ttu-id="ad0bf-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad0bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad0bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad0bf-122">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ad0bf-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad0bf-123">-SubscriptionId</span></span>
<span data-ttu-id="ad0bf-124">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ad0bf-125">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ad0bf-126">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="ad0bf-126">-Value</span></span>
<span data-ttu-id="ad0bf-127">Список участников базы данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="ad0bf-128">Для конструирования ознакомьтесь с разделом "Заметки" для свойств значения и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad0bf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad0bf-129">-Confirm</span></span>
<span data-ttu-id="ad0bf-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad0bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad0bf-131">-WhatIf</span></span>
<span data-ttu-id="ad0bf-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad0bf-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad0bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0bf-134">CommonParameters</span></span>
<span data-ttu-id="ad0bf-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0bf-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad0bf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0bf-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad0bf-137">INPUTS</span></span>

### <span data-ttu-id="ad0bf-138">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ad0bf-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ad0bf-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad0bf-139">OUTPUTS</span></span>

### <span data-ttu-id="ad0bf-140">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="ad0bf-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="ad0bf-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad0bf-141">NOTES</span></span>

<span data-ttu-id="ad0bf-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ad0bf-142">ALIASES</span></span>

<span data-ttu-id="ad0bf-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ad0bf-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad0bf-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad0bf-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad0bf-146">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="ad0bf-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad0bf-147">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ad0bf-148">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ad0bf-149">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ad0bf-150">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ad0bf-151">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="ad0bf-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad0bf-152">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ad0bf-153">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ad0bf-154">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ad0bf-155">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ad0bf-156">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="ad0bf-157">VALUE (значение) <IDatabasePrincipal [] >: список участников базы данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="ad0bf-158">`Name <String>`: Имя участника базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="ad0bf-159">`Role <DatabasePrincipalRole>`: Роль участника базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="ad0bf-160">`Type <DatabasePrincipalType>`: Тип участника базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="ad0bf-161">`[AppId <String>]`: Идентификатор приложения — применяется только для типа участника приложения.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="ad0bf-162">`[Email <String>]`: Сообщение участника базы данных, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="ad0bf-163">`[Fqn <String>]`: Полное имя участника базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad0bf-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="ad0bf-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad0bf-164">RELATED LINKS</span></span>

