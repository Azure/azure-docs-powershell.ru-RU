---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: 94e5525b1d783eea794b7e98e76e809b9d7e0f3b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065593"
---
# <span data-ttu-id="d1e89-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d1e89-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="d1e89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1e89-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e89-103">Возобновление приостановленного кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="d1e89-103">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="d1e89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1e89-104">SYNTAX</span></span>

### <span data-ttu-id="d1e89-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d1e89-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1e89-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1e89-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1e89-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d1e89-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1e89-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1e89-108">DESCRIPTION</span></span>
<span data-ttu-id="d1e89-109">Возобновление приостановленного кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="d1e89-109">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="d1e89-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1e89-110">EXAMPLES</span></span>

### <span data-ttu-id="d1e89-111">Пример 1: возобновление приостановленного кластера Kusto с помощью имени</span><span class="sxs-lookup"><span data-stu-id="d1e89-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="d1e89-112">Эта команда возобновляет приостановленный кластер Kusto с именем "mykustocluster", который находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="d1e89-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="d1e89-113">Пример 2: возобновление приостановленного Kustoного кластера с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="d1e89-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="d1e89-114">В приведенной выше команде получается кластер Kusto с именем "mykustocluster", обнаруженный в группе ресурсов "testrg", с помощью `Get-AzKustoCluster` командлета, а затем `Resume-AzKustoCluster` продается результат для возобновления.</span><span class="sxs-lookup"><span data-stu-id="d1e89-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="d1e89-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1e89-115">PARAMETERS</span></span>

### <span data-ttu-id="d1e89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e89-116">-DefaultProfile</span></span>
<span data-ttu-id="d1e89-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1e89-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1e89-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1e89-118">-InputObject</span></span>
<span data-ttu-id="d1e89-119">Объект Cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d1e89-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="d1e89-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1e89-120">-Name</span></span>
<span data-ttu-id="d1e89-121">Имя кластера, который нужно возобновить.</span><span class="sxs-lookup"><span data-stu-id="d1e89-121">Name of cluster to be resume.</span></span>

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

### <span data-ttu-id="d1e89-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1e89-122">-PassThru</span></span>
<span data-ttu-id="d1e89-123">Возвращает значение, указывающее, успешно ли возобновлено выполнение указанного кластера.</span><span class="sxs-lookup"><span data-stu-id="d1e89-123">Return whether the specified cluster was successfully resumed or not.</span></span>

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

### <span data-ttu-id="d1e89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e89-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1e89-125">Имя группы ресурсов, в которой находится кластер.</span><span class="sxs-lookup"><span data-stu-id="d1e89-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e89-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1e89-126">-ResourceId</span></span>
<span data-ttu-id="d1e89-127">Kusto Cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="d1e89-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="d1e89-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1e89-128">-Confirm</span></span>
<span data-ttu-id="d1e89-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d1e89-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1e89-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1e89-130">-WhatIf</span></span>
<span data-ttu-id="d1e89-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d1e89-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1e89-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1e89-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1e89-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e89-133">CommonParameters</span></span>
<span data-ttu-id="d1e89-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1e89-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e89-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1e89-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e89-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1e89-136">INPUTS</span></span>

### <span data-ttu-id="d1e89-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d1e89-137">System.String</span></span>

### <span data-ttu-id="d1e89-138">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d1e89-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="d1e89-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1e89-139">OUTPUTS</span></span>

### <span data-ttu-id="d1e89-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1e89-140">System.Boolean</span></span>

## <span data-ttu-id="d1e89-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1e89-141">NOTES</span></span>

## <span data-ttu-id="d1e89-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1e89-142">RELATED LINKS</span></span>
