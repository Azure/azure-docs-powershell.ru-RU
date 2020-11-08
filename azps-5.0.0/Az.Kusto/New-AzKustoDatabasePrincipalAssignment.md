---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 8bfcb3a96ee8db53a6a869a01441739ee9c503bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248991"
---
# <span data-ttu-id="48c1c-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="48c1c-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="48c1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="48c1c-103">Создание Kusto базы данных кластера principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="48c1c-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="48c1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48c1c-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="48c1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="48c1c-106">Создание Kusto базы данных кластера principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="48c1c-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="48c1c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="48c1c-108">Пример 1: создание базы данных Kusto кластера principalAssignment</span><span class="sxs-lookup"><span data-stu-id="48c1c-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="48c1c-109">Вышеприведенная команда создает базу данных Kusto кластера principalAssignment</span><span class="sxs-lookup"><span data-stu-id="48c1c-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="48c1c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48c1c-110">PARAMETERS</span></span>

### <span data-ttu-id="48c1c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48c1c-111">-AsJob</span></span>
<span data-ttu-id="48c1c-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="48c1c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="48c1c-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="48c1c-113">-ClusterName</span></span>
<span data-ttu-id="48c1c-114">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="48c1c-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="48c1c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="48c1c-115">-DatabaseName</span></span>
<span data-ttu-id="48c1c-116">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="48c1c-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="48c1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c1c-117">-DefaultProfile</span></span>
<span data-ttu-id="48c1c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48c1c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48c1c-119">-Wait</span><span class="sxs-lookup"><span data-stu-id="48c1c-119">-NoWait</span></span>
<span data-ttu-id="48c1c-120">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="48c1c-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="48c1c-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="48c1c-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="48c1c-122">Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="48c1c-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="48c1c-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="48c1c-123">-PrincipalId</span></span>
<span data-ttu-id="48c1c-124">Идентификатор участника, назначенный участнику базы данных.</span><span class="sxs-lookup"><span data-stu-id="48c1c-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="48c1c-125">Это может быть адрес электронной почты пользователя, идентификатор приложения или имя группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="48c1c-125">It can be a user email, application ID, or security group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c1c-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="48c1c-126">-PrincipalType</span></span>
<span data-ttu-id="48c1c-127">Тип участника.</span><span class="sxs-lookup"><span data-stu-id="48c1c-127">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c1c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48c1c-128">-ResourceGroupName</span></span>
<span data-ttu-id="48c1c-129">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="48c1c-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="48c1c-130">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="48c1c-130">-Role</span></span>
<span data-ttu-id="48c1c-131">Роль участника базы данных.</span><span class="sxs-lookup"><span data-stu-id="48c1c-131">Database principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DatabasePrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c1c-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48c1c-132">-SubscriptionId</span></span>
<span data-ttu-id="48c1c-133">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="48c1c-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="48c1c-134">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="48c1c-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c1c-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="48c1c-135">-TenantId</span></span>
<span data-ttu-id="48c1c-136">Идентификатор клиента участника.</span><span class="sxs-lookup"><span data-stu-id="48c1c-136">The tenant id of the principal</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c1c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48c1c-137">-Confirm</span></span>
<span data-ttu-id="48c1c-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48c1c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48c1c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48c1c-139">-WhatIf</span></span>
<span data-ttu-id="48c1c-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48c1c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48c1c-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48c1c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48c1c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c1c-142">CommonParameters</span></span>
<span data-ttu-id="48c1c-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48c1c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c1c-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48c1c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c1c-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48c1c-145">INPUTS</span></span>

## <span data-ttu-id="48c1c-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48c1c-146">OUTPUTS</span></span>

### <span data-ttu-id="48c1c-147">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="48c1c-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="48c1c-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="48c1c-148">NOTES</span></span>

<span data-ttu-id="48c1c-149">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="48c1c-149">ALIASES</span></span>

## <span data-ttu-id="48c1c-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48c1c-150">RELATED LINKS</span></span>

