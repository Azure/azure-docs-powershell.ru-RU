---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/suspend-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
ms.openlocfilehash: 6eceaffb371226c9dda0099a32a309272d6bdb3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900018"
---
# <span data-ttu-id="c99b0-101">Suspend-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="c99b0-101">Suspend-AzKustoCluster</span></span>

## <span data-ttu-id="c99b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c99b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c99b0-103">Приостановить существующий кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="c99b0-103">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="c99b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c99b0-104">SYNTAX</span></span>

### <span data-ttu-id="c99b0-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c99b0-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c99b0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c99b0-106">ByResourceId</span></span>
```
Suspend-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c99b0-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c99b0-107">ByInputObject</span></span>
```
Suspend-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c99b0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c99b0-108">DESCRIPTION</span></span>
<span data-ttu-id="c99b0-109">Приостановить существующий кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="c99b0-109">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="c99b0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c99b0-110">EXAMPLES</span></span>

### <span data-ttu-id="c99b0-111">Пример 1. приостановить существующий кластер Kusto по имени</span><span class="sxs-lookup"><span data-stu-id="c99b0-111">Example 1 - Suspend an existing Kusto cluster by name</span></span>

```
PS C:\> Suspend-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="c99b0-112">Приведенная выше команда приостанавливает кластер Kusto с именем "mykustocluster", который находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="c99b0-112">The above command suspends the Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="c99b0-113">Пример 2. Приостановка существующего кластера Kusto с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="c99b0-113">Example 2 - Suspend an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Suspend-AzKustoCluster
```

<span data-ttu-id="c99b0-114">Вышеприведенная команда возвращает кластер Kusto с именем "mykustocluster", обнаруженный в группе ресурсов "testrg", с помощью `Get-AzKustoCluster` командлета, а затем `Suspend-AzKustoCluster` передается результат, чтобы приостановить его.</span><span class="sxs-lookup"><span data-stu-id="c99b0-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Suspend-AzKustoCluster` to suspend it.</span></span>

## <span data-ttu-id="c99b0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c99b0-115">PARAMETERS</span></span>

### <span data-ttu-id="c99b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99b0-116">-DefaultProfile</span></span>
<span data-ttu-id="c99b0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c99b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c99b0-118">-InputObject</span></span>
<span data-ttu-id="c99b0-119">Объект Cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c99b0-119">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c99b0-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c99b0-120">-Name</span></span>
<span data-ttu-id="c99b0-121">Имя кластера, который нужно приостановить.</span><span class="sxs-lookup"><span data-stu-id="c99b0-121">Name of cluster to be suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99b0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c99b0-122">-PassThru</span></span>
<span data-ttu-id="c99b0-123">Возвращают данные о том, был ли этот кластер успешно приостановлен или нет.</span><span class="sxs-lookup"><span data-stu-id="c99b0-123">Return whether the specified cluster was successfully suspended or not.</span></span>

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

### <span data-ttu-id="c99b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="c99b0-125">Имя группы ресурсов, в которой находится кластер.</span><span class="sxs-lookup"><span data-stu-id="c99b0-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99b0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c99b0-126">-ResourceId</span></span>
<span data-ttu-id="c99b0-127">Kusto Cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="c99b0-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99b0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c99b0-128">-Confirm</span></span>
<span data-ttu-id="c99b0-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c99b0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c99b0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c99b0-130">-WhatIf</span></span>
<span data-ttu-id="c99b0-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c99b0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c99b0-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c99b0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c99b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99b0-133">CommonParameters</span></span>
<span data-ttu-id="c99b0-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c99b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99b0-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c99b0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99b0-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c99b0-136">INPUTS</span></span>

### <span data-ttu-id="c99b0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c99b0-137">System.String</span></span>

### <span data-ttu-id="c99b0-138">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="c99b0-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="c99b0-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c99b0-139">OUTPUTS</span></span>

### <span data-ttu-id="c99b0-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c99b0-140">System.Boolean</span></span>

## <span data-ttu-id="c99b0-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="c99b0-141">NOTES</span></span>

## <span data-ttu-id="c99b0-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c99b0-142">RELATED LINKS</span></span>
