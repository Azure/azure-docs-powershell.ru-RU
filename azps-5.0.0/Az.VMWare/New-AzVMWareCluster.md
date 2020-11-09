---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316167"
---
# <span data-ttu-id="f14cf-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="f14cf-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="f14cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f14cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f14cf-103">Создание или обновление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="f14cf-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="f14cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f14cf-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f14cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f14cf-105">DESCRIPTION</span></span>
<span data-ttu-id="f14cf-106">Создание или обновление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="f14cf-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="f14cf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f14cf-107">EXAMPLES</span></span>

### <span data-ttu-id="f14cf-108">Пример 1: Создание кластера</span><span class="sxs-lookup"><span data-stu-id="f14cf-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="f14cf-109">Создать кластер</span><span class="sxs-lookup"><span data-stu-id="f14cf-109">Create cluster</span></span>

## <span data-ttu-id="f14cf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f14cf-110">PARAMETERS</span></span>

### <span data-ttu-id="f14cf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f14cf-111">-AsJob</span></span>
<span data-ttu-id="f14cf-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f14cf-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f14cf-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="f14cf-113">-ClusterSize</span></span>
<span data-ttu-id="f14cf-114">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="f14cf-114">The cluster size</span></span>

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

### <span data-ttu-id="f14cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14cf-115">-DefaultProfile</span></span>
<span data-ttu-id="f14cf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f14cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f14cf-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f14cf-117">-Name</span></span>
<span data-ttu-id="f14cf-118">Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="f14cf-118">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="f14cf-119">-Wait</span><span class="sxs-lookup"><span data-stu-id="f14cf-119">-NoWait</span></span>
<span data-ttu-id="f14cf-120">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="f14cf-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f14cf-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="f14cf-121">-PrivateCloudName</span></span>
<span data-ttu-id="f14cf-122">Имя частного облака.</span><span class="sxs-lookup"><span data-stu-id="f14cf-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="f14cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f14cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="f14cf-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f14cf-124">The name of the resource group.</span></span>
<span data-ttu-id="f14cf-125">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="f14cf-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f14cf-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f14cf-126">-SkuName</span></span>
<span data-ttu-id="f14cf-127">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="f14cf-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="f14cf-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f14cf-128">-SubscriptionId</span></span>
<span data-ttu-id="f14cf-129">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="f14cf-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f14cf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f14cf-130">-Confirm</span></span>
<span data-ttu-id="f14cf-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f14cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f14cf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f14cf-132">-WhatIf</span></span>
<span data-ttu-id="f14cf-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f14cf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f14cf-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f14cf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f14cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14cf-135">CommonParameters</span></span>
<span data-ttu-id="f14cf-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f14cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14cf-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f14cf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14cf-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f14cf-138">INPUTS</span></span>

## <span data-ttu-id="f14cf-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f14cf-139">OUTPUTS</span></span>

### <span data-ttu-id="f14cf-140">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="f14cf-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="f14cf-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="f14cf-141">NOTES</span></span>

<span data-ttu-id="f14cf-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="f14cf-142">ALIASES</span></span>

## <span data-ttu-id="f14cf-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f14cf-143">RELATED LINKS</span></span>

