---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242112"
---
# <span data-ttu-id="2fd4d-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2fd4d-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="2fd4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fd4d-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd4d-103">Получите сведения о ресурсах с управляемым кластером.</span><span class="sxs-lookup"><span data-stu-id="2fd4d-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="2fd4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2fd4d-104">SYNTAX</span></span>

### <span data-ttu-id="2fd4d-105">BySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2fd4d-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fd4d-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2fd4d-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fd4d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="2fd4d-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fd4d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fd4d-108">DESCRIPTION</span></span>
<span data-ttu-id="2fd4d-109">Получите сведения о ресурсах с управляемым кластером.</span><span class="sxs-lookup"><span data-stu-id="2fd4d-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="2fd4d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2fd4d-110">EXAMPLES</span></span>

### <span data-ttu-id="2fd4d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2fd4d-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="2fd4d-112">Получите подробные сведения о кластере.</span><span class="sxs-lookup"><span data-stu-id="2fd4d-112">Get cluster details.</span></span>

### <span data-ttu-id="2fd4d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2fd4d-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="2fd4d-114">Получить список кластеров в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fd4d-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="2fd4d-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2fd4d-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="2fd4d-116">Получить список кластеров для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="2fd4d-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="2fd4d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fd4d-117">PARAMETERS</span></span>

### <span data-ttu-id="2fd4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd4d-118">-DefaultProfile</span></span>
<span data-ttu-id="2fd4d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fd4d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fd4d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2fd4d-120">-Name</span></span>
<span data-ttu-id="2fd4d-121">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="2fd4d-121">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2fd4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fd4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="2fd4d-123">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fd4d-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fd4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd4d-124">CommonParameters</span></span>
<span data-ttu-id="2fd4d-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fd4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd4d-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fd4d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd4d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2fd4d-127">INPUTS</span></span>

### <span data-ttu-id="2fd4d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2fd4d-128">System.String</span></span>

## <span data-ttu-id="2fd4d-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2fd4d-129">OUTPUTS</span></span>

### <span data-ttu-id="2fd4d-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2fd4d-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="2fd4d-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2fd4d-131">NOTES</span></span>

## <span data-ttu-id="2fd4d-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fd4d-132">RELATED LINKS</span></span>
