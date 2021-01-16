---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 80ab75e2361cf052e88377e9d7a393fb36627ae7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425804"
---
# <span data-ttu-id="8d4c5-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="8d4c5-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="8d4c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8d4c5-103">Создание базы данных "Кузто" principalAssignment базы данных "Кузто".</span><span class="sxs-lookup"><span data-stu-id="8d4c5-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="8d4c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d4c5-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d4c5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d4c5-105">DESCRIPTION</span></span>
<span data-ttu-id="8d4c5-106">Создание базы данных "Кузто" principalAssignment базы данных "Кузто".</span><span class="sxs-lookup"><span data-stu-id="8d4c5-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="8d4c5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d4c5-107">EXAMPLES</span></span>

### <span data-ttu-id="8d4c5-108">Пример 1. Создание базы данных "Кузто" principalAssignment</span><span class="sxs-lookup"><span data-stu-id="8d4c5-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="8d4c5-109">С этой командой создается кластер базы данных "Кузто" principalAssignment</span><span class="sxs-lookup"><span data-stu-id="8d4c5-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="8d4c5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d4c5-110">PARAMETERS</span></span>

### <span data-ttu-id="8d4c5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d4c5-111">-AsJob</span></span>
<span data-ttu-id="8d4c5-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="8d4c5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8d4c5-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8d4c5-113">-ClusterName</span></span>
<span data-ttu-id="8d4c5-114">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8d4c5-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8d4c5-115">-DatabaseName</span></span>
<span data-ttu-id="8d4c5-116">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="8d4c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d4c5-117">-DefaultProfile</span></span>
<span data-ttu-id="8d4c5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d4c5-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8d4c5-119">-NoWait</span></span>
<span data-ttu-id="8d4c5-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="8d4c5-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8d4c5-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="8d4c5-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="8d4c5-122">Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="8d4c5-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="8d4c5-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="8d4c5-123">-PrincipalId</span></span>
<span data-ttu-id="8d4c5-124">Основной ИД, присвоенный основной базе данных.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="8d4c5-125">Это может быть адрес электронной почты пользователя, ИД приложения или имя группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="8d4c5-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="8d4c5-126">-PrincipalType</span></span>
<span data-ttu-id="8d4c5-127">Тип principal.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-127">Principal type.</span></span>

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

### <span data-ttu-id="8d4c5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d4c5-128">-ResourceGroupName</span></span>
<span data-ttu-id="8d4c5-129">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8d4c5-130">-Роль</span><span class="sxs-lookup"><span data-stu-id="8d4c5-130">-Role</span></span>
<span data-ttu-id="8d4c5-131">Роль основного сайта базы данных.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-131">Database principal role.</span></span>

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

### <span data-ttu-id="8d4c5-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d4c5-132">-SubscriptionId</span></span>
<span data-ttu-id="8d4c5-133">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8d4c5-134">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8d4c5-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="8d4c5-135">-TenantId</span></span>
<span data-ttu-id="8d4c5-136">The tenant id of the principal</span><span class="sxs-lookup"><span data-stu-id="8d4c5-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="8d4c5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d4c5-137">-Confirm</span></span>
<span data-ttu-id="8d4c5-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d4c5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d4c5-139">-WhatIf</span></span>
<span data-ttu-id="8d4c5-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d4c5-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d4c5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d4c5-142">CommonParameters</span></span>
<span data-ttu-id="8d4c5-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d4c5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d4c5-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d4c5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d4c5-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d4c5-145">INPUTS</span></span>

## <span data-ttu-id="8d4c5-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d4c5-146">OUTPUTS</span></span>

### <span data-ttu-id="8d4c5-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="8d4c5-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="8d4c5-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d4c5-148">NOTES</span></span>

<span data-ttu-id="8d4c5-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8d4c5-149">ALIASES</span></span>

## <span data-ttu-id="8d4c5-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d4c5-150">RELATED LINKS</span></span>
