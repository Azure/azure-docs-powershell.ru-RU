---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: dc0b4ea1616c916edacaf4d5a4a2b431e7f7d113
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394879"
---
# <span data-ttu-id="a6c6d-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="a6c6d-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="a6c6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c6d-103">Создает или обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-103">Creates or updates a database.</span></span>

## <span data-ttu-id="a6c6d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6c6d-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6c6d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6c6d-105">DESCRIPTION</span></span>
<span data-ttu-id="a6c6d-106">Создает или обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-106">Creates or updates a database.</span></span>

## <span data-ttu-id="a6c6d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6c6d-107">EXAMPLES</span></span>

### <span data-ttu-id="a6c6d-108">Пример 1. Создание базы данных "Кузто" по имени</span><span class="sxs-lookup"><span data-stu-id="a6c6d-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="a6c6d-109">С этой командой создается новая база данных "Кузто" с именем "mykustodatabase" в существующем кластере "testnewkustocluster", найденная в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="a6c6d-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="a6c6d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6c6d-110">PARAMETERS</span></span>

### <span data-ttu-id="a6c6d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6c6d-111">-AsJob</span></span>
<span data-ttu-id="a6c6d-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="a6c6d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a6c6d-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a6c6d-113">-ClusterName</span></span>
<span data-ttu-id="a6c6d-114">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="a6c6d-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a6c6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c6d-115">-DefaultProfile</span></span>
<span data-ttu-id="a6c6d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6c6d-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="a6c6d-117">-HotCachePeriod</span></span>
<span data-ttu-id="a6c6d-118">Время хранения данных в кэше для быстрых запросов в TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="a6c6d-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="a6c6d-119">-Kind</span></span>
<span data-ttu-id="a6c6d-120">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="a6c6d-120">Kind of the database</span></span>

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

### <span data-ttu-id="a6c6d-121">-Location</span><span class="sxs-lookup"><span data-stu-id="a6c6d-121">-Location</span></span>
<span data-ttu-id="a6c6d-122">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-122">Resource location.</span></span>

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

### <span data-ttu-id="a6c6d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a6c6d-123">-Name</span></span>
<span data-ttu-id="a6c6d-124">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-124">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="a6c6d-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a6c6d-125">-NoWait</span></span>
<span data-ttu-id="a6c6d-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="a6c6d-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a6c6d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c6d-127">-ResourceGroupName</span></span>
<span data-ttu-id="a6c6d-128">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a6c6d-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="a6c6d-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="a6c6d-130">Время хранения данных, прежде чем они перестают быть доступны для запросов в TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="a6c6d-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6c6d-131">-SubscriptionId</span></span>
<span data-ttu-id="a6c6d-132">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a6c6d-133">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a6c6d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6c6d-134">-Confirm</span></span>
<span data-ttu-id="a6c6d-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c6d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c6d-136">-WhatIf</span></span>
<span data-ttu-id="a6c6d-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c6d-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c6d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c6d-139">CommonParameters</span></span>
<span data-ttu-id="a6c6d-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c6d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c6d-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6c6d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c6d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6c6d-142">INPUTS</span></span>

## <span data-ttu-id="a6c6d-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6c6d-143">OUTPUTS</span></span>

### <span data-ttu-id="a6c6d-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span><span class="sxs-lookup"><span data-stu-id="a6c6d-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="a6c6d-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6c6d-145">NOTES</span></span>

<span data-ttu-id="a6c6d-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a6c6d-146">ALIASES</span></span>

## <span data-ttu-id="a6c6d-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6c6d-147">RELATED LINKS</span></span>

