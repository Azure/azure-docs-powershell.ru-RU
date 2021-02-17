---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: fafc31700477de968c453002e903b52aa73967d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243301"
---
# <span data-ttu-id="0af08-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0af08-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="0af08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0af08-102">SYNOPSIS</span></span>
<span data-ttu-id="0af08-103">Создайте principalAssignment кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="0af08-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="0af08-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0af08-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0af08-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0af08-105">DESCRIPTION</span></span>
<span data-ttu-id="0af08-106">Создайте principalAssignment кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="0af08-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="0af08-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0af08-107">EXAMPLES</span></span>

### <span data-ttu-id="0af08-108">Пример 1. Создание кластера Кусто</span><span class="sxs-lookup"><span data-stu-id="0af08-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="0af08-109">С этой командой создается principalAssignment кластера Кусто</span><span class="sxs-lookup"><span data-stu-id="0af08-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="0af08-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0af08-110">PARAMETERS</span></span>

### <span data-ttu-id="0af08-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0af08-111">-AsJob</span></span>
<span data-ttu-id="0af08-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0af08-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0af08-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0af08-113">-ClusterName</span></span>
<span data-ttu-id="0af08-114">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="0af08-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0af08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af08-115">-DefaultProfile</span></span>
<span data-ttu-id="0af08-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0af08-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0af08-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0af08-117">-NoWait</span></span>
<span data-ttu-id="0af08-118">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="0af08-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0af08-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0af08-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="0af08-120">Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="0af08-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="0af08-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="0af08-121">-PrincipalId</span></span>
<span data-ttu-id="0af08-122">ИД основной суммы, присвоенный основной сумме кластера.</span><span class="sxs-lookup"><span data-stu-id="0af08-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="0af08-123">Это может быть адрес электронной почты пользователя, ИД приложения или имя группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="0af08-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="0af08-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="0af08-124">-PrincipalType</span></span>
<span data-ttu-id="0af08-125">Тип основной суммы.</span><span class="sxs-lookup"><span data-stu-id="0af08-125">Principal type.</span></span>

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

### <span data-ttu-id="0af08-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af08-126">-ResourceGroupName</span></span>
<span data-ttu-id="0af08-127">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="0af08-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0af08-128">-Роль</span><span class="sxs-lookup"><span data-stu-id="0af08-128">-Role</span></span>
<span data-ttu-id="0af08-129">Роль директора-кластера.</span><span class="sxs-lookup"><span data-stu-id="0af08-129">Cluster principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.ClusterPrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af08-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0af08-130">-SubscriptionId</span></span>
<span data-ttu-id="0af08-131">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0af08-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0af08-132">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="0af08-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0af08-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="0af08-133">-TenantId</span></span>
<span data-ttu-id="0af08-134">The tenant id of the principal</span><span class="sxs-lookup"><span data-stu-id="0af08-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="0af08-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0af08-135">-Confirm</span></span>
<span data-ttu-id="0af08-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0af08-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0af08-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0af08-137">-WhatIf</span></span>
<span data-ttu-id="0af08-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0af08-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0af08-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0af08-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0af08-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af08-140">CommonParameters</span></span>
<span data-ttu-id="0af08-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af08-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af08-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0af08-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af08-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0af08-143">INPUTS</span></span>

## <span data-ttu-id="0af08-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0af08-144">OUTPUTS</span></span>

### <span data-ttu-id="0af08-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0af08-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="0af08-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0af08-146">NOTES</span></span>

<span data-ttu-id="0af08-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0af08-147">ALIASES</span></span>

## <span data-ttu-id="0af08-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0af08-148">RELATED LINKS</span></span>

