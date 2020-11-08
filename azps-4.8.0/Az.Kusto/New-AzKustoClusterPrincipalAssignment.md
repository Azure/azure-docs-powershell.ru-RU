---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243548"
---
# <span data-ttu-id="b2003-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="b2003-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="b2003-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2003-102">SYNOPSIS</span></span>
<span data-ttu-id="b2003-103">Создание principalAssignment кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="b2003-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="b2003-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2003-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b2003-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2003-105">DESCRIPTION</span></span>
<span data-ttu-id="b2003-106">Создание principalAssignment кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="b2003-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="b2003-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2003-107">EXAMPLES</span></span>

### <span data-ttu-id="b2003-108">Пример 1: создание Kusto кластера principalAssignment</span><span class="sxs-lookup"><span data-stu-id="b2003-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="b2003-109">В приведенной выше команде создается кластер Kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="b2003-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="b2003-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2003-110">PARAMETERS</span></span>

### <span data-ttu-id="b2003-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2003-111">-AsJob</span></span>
<span data-ttu-id="b2003-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b2003-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b2003-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="b2003-113">-ClusterName</span></span>
<span data-ttu-id="b2003-114">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="b2003-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b2003-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2003-115">-DefaultProfile</span></span>
<span data-ttu-id="b2003-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2003-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2003-117">-Wait</span><span class="sxs-lookup"><span data-stu-id="b2003-117">-NoWait</span></span>
<span data-ttu-id="b2003-118">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="b2003-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b2003-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b2003-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="b2003-120">Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="b2003-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="b2003-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="b2003-121">-PrincipalId</span></span>
<span data-ttu-id="b2003-122">Идентификатор участника, назначенный участнику кластера.</span><span class="sxs-lookup"><span data-stu-id="b2003-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="b2003-123">Это может быть адрес электронной почты пользователя, идентификатор приложения или имя группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="b2003-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="b2003-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="b2003-124">-PrincipalType</span></span>
<span data-ttu-id="b2003-125">Тип участника.</span><span class="sxs-lookup"><span data-stu-id="b2003-125">Principal type.</span></span>

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

### <span data-ttu-id="b2003-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2003-126">-ResourceGroupName</span></span>
<span data-ttu-id="b2003-127">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="b2003-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b2003-128">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="b2003-128">-Role</span></span>
<span data-ttu-id="b2003-129">Роль основного сервера кластера.</span><span class="sxs-lookup"><span data-stu-id="b2003-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="b2003-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2003-130">-SubscriptionId</span></span>
<span data-ttu-id="b2003-131">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b2003-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b2003-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b2003-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b2003-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="b2003-133">-TenantId</span></span>
<span data-ttu-id="b2003-134">Идентификатор клиента участника.</span><span class="sxs-lookup"><span data-stu-id="b2003-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="b2003-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2003-135">-Confirm</span></span>
<span data-ttu-id="b2003-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2003-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2003-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2003-137">-WhatIf</span></span>
<span data-ttu-id="b2003-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b2003-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2003-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b2003-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2003-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2003-140">CommonParameters</span></span>
<span data-ttu-id="b2003-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2003-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2003-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2003-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2003-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2003-143">INPUTS</span></span>

## <span data-ttu-id="b2003-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2003-144">OUTPUTS</span></span>

### <span data-ttu-id="b2003-145">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="b2003-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="b2003-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2003-146">NOTES</span></span>

<span data-ttu-id="b2003-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="b2003-147">ALIASES</span></span>

## <span data-ttu-id="b2003-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2003-148">RELATED LINKS</span></span>

