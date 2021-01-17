---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395847"
---
# <span data-ttu-id="b143b-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="b143b-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="b143b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b143b-102">SYNOPSIS</span></span>
<span data-ttu-id="b143b-103">API для регистрации нового кластера K8s и создания отслеживаемго ресурса в ARM</span><span class="sxs-lookup"><span data-stu-id="b143b-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="b143b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b143b-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b143b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b143b-105">DESCRIPTION</span></span>
<span data-ttu-id="b143b-106">API для регистрации нового кластера K8s и создания отслеживаемго ресурса в ARM</span><span class="sxs-lookup"><span data-stu-id="b143b-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="b143b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b143b-107">EXAMPLES</span></span>

### <span data-ttu-id="b143b-108">Пример 1. Создание подключенных куберсетей</span><span class="sxs-lookup"><span data-stu-id="b143b-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="b143b-109">Эта команда создает подключенные куберсети.</span><span class="sxs-lookup"><span data-stu-id="b143b-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="b143b-110">Пример 1. Создание подключенных куберсетей с параметрами kubeConfig и kubeContext</span><span class="sxs-lookup"><span data-stu-id="b143b-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="b143b-111">Эта команда создает подключенные куберсети с параметрами kubeConfig и kubeContext.</span><span class="sxs-lookup"><span data-stu-id="b143b-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="b143b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b143b-112">PARAMETERS</span></span>

### <span data-ttu-id="b143b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b143b-113">-ClusterName</span></span>
<span data-ttu-id="b143b-114">Название кластера "Кубберсети", на котором он называется.</span><span class="sxs-lookup"><span data-stu-id="b143b-114">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="b143b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b143b-115">-DefaultProfile</span></span>
<span data-ttu-id="b143b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b143b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b143b-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="b143b-117">-KubeConfig</span></span>
<span data-ttu-id="b143b-118">Путь к файлу config kube</span><span class="sxs-lookup"><span data-stu-id="b143b-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="b143b-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="b143b-119">-KubeContext</span></span>
<span data-ttu-id="b143b-120">Контекст Kubconfig с текущего компьютера</span><span class="sxs-lookup"><span data-stu-id="b143b-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="b143b-121">-Location</span><span class="sxs-lookup"><span data-stu-id="b143b-121">-Location</span></span>
<span data-ttu-id="b143b-122">Расположение кластера</span><span class="sxs-lookup"><span data-stu-id="b143b-122">Location of the cluster</span></span>

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

### <span data-ttu-id="b143b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b143b-123">-ResourceGroupName</span></span>
<span data-ttu-id="b143b-124">Имя группы ресурсов, в которой зарегистрирован кластер куберсетей.</span><span class="sxs-lookup"><span data-stu-id="b143b-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="b143b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b143b-125">-SubscriptionId</span></span>
<span data-ttu-id="b143b-126">ИД подписки, в которой зарегистрирован кластер куберсетей.</span><span class="sxs-lookup"><span data-stu-id="b143b-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="b143b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b143b-127">-Confirm</span></span>
<span data-ttu-id="b143b-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b143b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b143b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b143b-129">-WhatIf</span></span>
<span data-ttu-id="b143b-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b143b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b143b-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b143b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b143b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b143b-132">CommonParameters</span></span>
<span data-ttu-id="b143b-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b143b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b143b-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b143b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b143b-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b143b-135">INPUTS</span></span>

## <span data-ttu-id="b143b-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b143b-136">OUTPUTS</span></span>

### <span data-ttu-id="b143b-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="b143b-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="b143b-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b143b-138">NOTES</span></span>

<span data-ttu-id="b143b-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b143b-139">ALIASES</span></span>

## <span data-ttu-id="b143b-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b143b-140">RELATED LINKS</span></span>

