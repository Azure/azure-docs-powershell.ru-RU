---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505819"
---
# <span data-ttu-id="505d8-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="505d8-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="505d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="505d8-102">SYNOPSIS</span></span>
<span data-ttu-id="505d8-103">Создание и обновление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="505d8-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="505d8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="505d8-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="505d8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="505d8-105">DESCRIPTION</span></span>
<span data-ttu-id="505d8-106">Создание и обновление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="505d8-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="505d8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="505d8-107">EXAMPLES</span></span>

### <span data-ttu-id="505d8-108">Пример 1. Создание кластера</span><span class="sxs-lookup"><span data-stu-id="505d8-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="505d8-109">Создание кластера</span><span class="sxs-lookup"><span data-stu-id="505d8-109">Create cluster</span></span>

## <span data-ttu-id="505d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="505d8-110">PARAMETERS</span></span>

### <span data-ttu-id="505d8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="505d8-111">-AsJob</span></span>
<span data-ttu-id="505d8-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="505d8-112">Run the command as a job</span></span>

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

### <span data-ttu-id="505d8-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="505d8-113">-ClusterSize</span></span>
<span data-ttu-id="505d8-114">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="505d8-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505d8-115">-DefaultProfile</span></span>
<span data-ttu-id="505d8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="505d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="505d8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="505d8-117">-Name</span></span>
<span data-ttu-id="505d8-118">Название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="505d8-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505d8-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="505d8-119">-NoWait</span></span>
<span data-ttu-id="505d8-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="505d8-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="505d8-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="505d8-121">-PrivateCloudName</span></span>
<span data-ttu-id="505d8-122">Имя закрытого облака.</span><span class="sxs-lookup"><span data-stu-id="505d8-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="505d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="505d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="505d8-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="505d8-124">The name of the resource group.</span></span>
<span data-ttu-id="505d8-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="505d8-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="505d8-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="505d8-126">-SkuName</span></span>
<span data-ttu-id="505d8-127">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="505d8-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="505d8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="505d8-128">-SubscriptionId</span></span>
<span data-ttu-id="505d8-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="505d8-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="505d8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="505d8-130">-Confirm</span></span>
<span data-ttu-id="505d8-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="505d8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="505d8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="505d8-132">-WhatIf</span></span>
<span data-ttu-id="505d8-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="505d8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="505d8-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="505d8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="505d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505d8-135">CommonParameters</span></span>
<span data-ttu-id="505d8-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="505d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505d8-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="505d8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505d8-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="505d8-138">INPUTS</span></span>

## <span data-ttu-id="505d8-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="505d8-139">OUTPUTS</span></span>

### <span data-ttu-id="505d8-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="505d8-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="505d8-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="505d8-141">NOTES</span></span>

<span data-ttu-id="505d8-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="505d8-142">ALIASES</span></span>

## <span data-ttu-id="505d8-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="505d8-143">RELATED LINKS</span></span>

