---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: dc0b4ea1616c916edacaf4d5a4a2b431e7f7d113
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248992"
---
# <span data-ttu-id="cd875-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="cd875-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="cd875-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd875-102">SYNOPSIS</span></span>
<span data-ttu-id="cd875-103">Создает или обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="cd875-103">Creates or updates a database.</span></span>

## <span data-ttu-id="cd875-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd875-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd875-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd875-105">DESCRIPTION</span></span>
<span data-ttu-id="cd875-106">Создает или обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="cd875-106">Creates or updates a database.</span></span>

## <span data-ttu-id="cd875-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd875-107">EXAMPLES</span></span>

### <span data-ttu-id="cd875-108">Пример 1: создание новой базы данных Kusto по имени</span><span class="sxs-lookup"><span data-stu-id="cd875-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="cd875-109">Вышеприведенная команда создает новую базу данных Kusto с именем "mykustodatabase" в существующем кластере "testnewkustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="cd875-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="cd875-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd875-110">PARAMETERS</span></span>

### <span data-ttu-id="cd875-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd875-111">-AsJob</span></span>
<span data-ttu-id="cd875-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="cd875-112">Run the command as a job</span></span>

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

### <span data-ttu-id="cd875-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="cd875-113">-ClusterName</span></span>
<span data-ttu-id="cd875-114">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="cd875-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cd875-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd875-115">-DefaultProfile</span></span>
<span data-ttu-id="cd875-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd875-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd875-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="cd875-117">-HotCachePeriod</span></span>
<span data-ttu-id="cd875-118">Время, в течение которого данные будут храниться в кэше для ускорения запросов в TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="cd875-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd875-119">-Видах</span><span class="sxs-lookup"><span data-stu-id="cd875-119">-Kind</span></span>
<span data-ttu-id="cd875-120">Ее вида</span><span class="sxs-lookup"><span data-stu-id="cd875-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd875-121">-Location</span><span class="sxs-lookup"><span data-stu-id="cd875-121">-Location</span></span>
<span data-ttu-id="cd875-122">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd875-122">Resource location.</span></span>

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

### <span data-ttu-id="cd875-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cd875-123">-Name</span></span>
<span data-ttu-id="cd875-124">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="cd875-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd875-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="cd875-125">-NoWait</span></span>
<span data-ttu-id="cd875-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="cd875-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd875-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd875-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd875-128">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="cd875-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cd875-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="cd875-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="cd875-130">Время, в течение которого данные будут храниться до того, как она станет доступна для запросов в TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="cd875-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd875-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd875-131">-SubscriptionId</span></span>
<span data-ttu-id="cd875-132">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cd875-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd875-133">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="cd875-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cd875-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd875-134">-Confirm</span></span>
<span data-ttu-id="cd875-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd875-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd875-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd875-136">-WhatIf</span></span>
<span data-ttu-id="cd875-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd875-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd875-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd875-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd875-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd875-139">CommonParameters</span></span>
<span data-ttu-id="cd875-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd875-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd875-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd875-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd875-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd875-142">INPUTS</span></span>

## <span data-ttu-id="cd875-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd875-143">OUTPUTS</span></span>

### <span data-ttu-id="cd875-144">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="cd875-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="cd875-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd875-145">NOTES</span></span>

<span data-ttu-id="cd875-146">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="cd875-146">ALIASES</span></span>

## <span data-ttu-id="cd875-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd875-147">RELATED LINKS</span></span>

