---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079777"
---
# <span data-ttu-id="ee299-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="ee299-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="ee299-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee299-102">SYNOPSIS</span></span>
<span data-ttu-id="ee299-103">API для регистрации нового кластера K8s и, следовательно, создания отслеживаемого ресурса на ARM</span><span class="sxs-lookup"><span data-stu-id="ee299-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="ee299-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee299-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee299-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee299-105">DESCRIPTION</span></span>
<span data-ttu-id="ee299-106">API для регистрации нового кластера K8s и, следовательно, создания отслеживаемого ресурса на ARM</span><span class="sxs-lookup"><span data-stu-id="ee299-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="ee299-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee299-107">EXAMPLES</span></span>

### <span data-ttu-id="ee299-108">Пример 1: Создание подключенного kubernetes</span><span class="sxs-lookup"><span data-stu-id="ee299-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="ee299-109">Эта команда создает подключенный kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ee299-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="ee299-110">Пример 1: Создание подключенного kubernetes с параметрами kubeConfig и kubeContext</span><span class="sxs-lookup"><span data-stu-id="ee299-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="ee299-111">Эта команда создает подключенный kubernetes с параметрами kubeConfig и kubeContext.</span><span class="sxs-lookup"><span data-stu-id="ee299-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="ee299-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee299-112">PARAMETERS</span></span>

### <span data-ttu-id="ee299-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ee299-113">-ClusterName</span></span>
<span data-ttu-id="ee299-114">Имя кластера Kubernetes, в котором вызывается Get.</span><span class="sxs-lookup"><span data-stu-id="ee299-114">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee299-115">-DefaultProfile</span></span>
<span data-ttu-id="ee299-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee299-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee299-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="ee299-117">-KubeConfig</span></span>
<span data-ttu-id="ee299-118">Путь к файлу конфигурации KUBE</span><span class="sxs-lookup"><span data-stu-id="ee299-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="ee299-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="ee299-119">-KubeContext</span></span>
<span data-ttu-id="ee299-120">Контекст Kubconfig с текущего компьютера</span><span class="sxs-lookup"><span data-stu-id="ee299-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="ee299-121">-Location</span><span class="sxs-lookup"><span data-stu-id="ee299-121">-Location</span></span>
<span data-ttu-id="ee299-122">Расположение кластера</span><span class="sxs-lookup"><span data-stu-id="ee299-122">Location of the cluster</span></span>

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

### <span data-ttu-id="ee299-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee299-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee299-124">Имя группы ресурсов, на которую зарегистрирован кластер kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ee299-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="ee299-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee299-125">-SubscriptionId</span></span>
<span data-ttu-id="ee299-126">Идентификатор подписки, на которую зарегистрирован kubernetes кластер.</span><span class="sxs-lookup"><span data-stu-id="ee299-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="ee299-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee299-127">-Confirm</span></span>
<span data-ttu-id="ee299-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee299-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee299-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee299-129">-WhatIf</span></span>
<span data-ttu-id="ee299-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ee299-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee299-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ee299-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee299-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee299-132">CommonParameters</span></span>
<span data-ttu-id="ee299-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee299-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee299-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee299-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee299-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee299-135">INPUTS</span></span>

## <span data-ttu-id="ee299-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee299-136">OUTPUTS</span></span>

### <span data-ttu-id="ee299-137">Microsoft. Azure. PowerShell. командлеты. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="ee299-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="ee299-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee299-138">NOTES</span></span>

<span data-ttu-id="ee299-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ee299-139">ALIASES</span></span>

## <span data-ttu-id="ee299-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee299-140">RELATED LINKS</span></span>

