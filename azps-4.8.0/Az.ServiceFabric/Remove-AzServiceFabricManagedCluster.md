---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243307"
---
# <span data-ttu-id="88de0-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="88de0-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="88de0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88de0-102">SYNOPSIS</span></span>
<span data-ttu-id="88de0-103">Удалите ресурс кластера.</span><span class="sxs-lookup"><span data-stu-id="88de0-103">Remove cluster resource.</span></span>

## <span data-ttu-id="88de0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88de0-104">SYNTAX</span></span>

### <span data-ttu-id="88de0-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88de0-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88de0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="88de0-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88de0-107">ById</span><span class="sxs-lookup"><span data-stu-id="88de0-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88de0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88de0-108">DESCRIPTION</span></span>
<span data-ttu-id="88de0-109">Удалить кластер это также приведет к удалению всех типов узлов в кластере.</span><span class="sxs-lookup"><span data-stu-id="88de0-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="88de0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88de0-110">EXAMPLES</span></span>

### <span data-ttu-id="88de0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88de0-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="88de0-112">Удалите кластер.</span><span class="sxs-lookup"><span data-stu-id="88de0-112">Remove cluster.</span></span>

### <span data-ttu-id="88de0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88de0-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="88de0-114">Удаление кластера с помощью трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="88de0-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="88de0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88de0-115">PARAMETERS</span></span>

### <span data-ttu-id="88de0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88de0-116">-AsJob</span></span>
<span data-ttu-id="88de0-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="88de0-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="88de0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88de0-118">-DefaultProfile</span></span>
<span data-ttu-id="88de0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88de0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88de0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88de0-120">-InputObject</span></span>
<span data-ttu-id="88de0-121">Управляемый ресурс кластера</span><span class="sxs-lookup"><span data-stu-id="88de0-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88de0-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88de0-122">-Name</span></span>
<span data-ttu-id="88de0-123">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="88de0-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88de0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88de0-124">-PassThru</span></span>
<span data-ttu-id="88de0-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="88de0-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="88de0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88de0-126">-ResourceGroupName</span></span>
<span data-ttu-id="88de0-127">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88de0-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88de0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88de0-128">-ResourceId</span></span>
<span data-ttu-id="88de0-129">Идентификатор ресурса управляемого кластера</span><span class="sxs-lookup"><span data-stu-id="88de0-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88de0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88de0-130">-Confirm</span></span>
<span data-ttu-id="88de0-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88de0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88de0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88de0-132">-WhatIf</span></span>
<span data-ttu-id="88de0-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88de0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88de0-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88de0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88de0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88de0-135">CommonParameters</span></span>
<span data-ttu-id="88de0-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88de0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88de0-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88de0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88de0-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88de0-138">INPUTS</span></span>

### <span data-ttu-id="88de0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="88de0-139">System.String</span></span>

## <span data-ttu-id="88de0-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88de0-140">OUTPUTS</span></span>

### <span data-ttu-id="88de0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88de0-141">System.Boolean</span></span>

## <span data-ttu-id="88de0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="88de0-142">NOTES</span></span>

## <span data-ttu-id="88de0-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88de0-143">RELATED LINKS</span></span>
