---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078727"
---
# <span data-ttu-id="e8f70-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="e8f70-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="e8f70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8f70-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f70-103">Получение сведений об управляемом ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="e8f70-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="e8f70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8f70-104">SYNTAX</span></span>

### <span data-ttu-id="e8f70-105">BySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8f70-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8f70-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8f70-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8f70-107">ByName</span><span class="sxs-lookup"><span data-stu-id="e8f70-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8f70-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8f70-108">DESCRIPTION</span></span>
<span data-ttu-id="e8f70-109">Получение сведений об управляемом ресурсе кластера.</span><span class="sxs-lookup"><span data-stu-id="e8f70-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="e8f70-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8f70-110">EXAMPLES</span></span>

### <span data-ttu-id="e8f70-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8f70-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="e8f70-112">Получение сведений о кластере.</span><span class="sxs-lookup"><span data-stu-id="e8f70-112">Get cluster details.</span></span>

### <span data-ttu-id="e8f70-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e8f70-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="e8f70-114">Получение списка кластеров в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8f70-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="e8f70-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e8f70-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="e8f70-116">Получение списка кластеров в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="e8f70-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="e8f70-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8f70-117">PARAMETERS</span></span>

### <span data-ttu-id="e8f70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f70-118">-DefaultProfile</span></span>
<span data-ttu-id="e8f70-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f70-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f70-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8f70-120">-Name</span></span>
<span data-ttu-id="e8f70-121">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="e8f70-121">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e8f70-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f70-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8f70-123">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8f70-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e8f70-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f70-124">CommonParameters</span></span>
<span data-ttu-id="e8f70-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8f70-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f70-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8f70-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f70-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8f70-127">INPUTS</span></span>

### <span data-ttu-id="e8f70-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e8f70-128">System.String</span></span>

## <span data-ttu-id="e8f70-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8f70-129">OUTPUTS</span></span>

### <span data-ttu-id="e8f70-130">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="e8f70-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="e8f70-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8f70-131">NOTES</span></span>

## <span data-ttu-id="e8f70-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8f70-132">RELATED LINKS</span></span>
