---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315641"
---
# <span data-ttu-id="65b69-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="65b69-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="65b69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65b69-102">SYNOPSIS</span></span>
<span data-ttu-id="65b69-103">Получение сведений о ресурсе типа управляемого узла.</span><span class="sxs-lookup"><span data-stu-id="65b69-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="65b69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65b69-104">SYNTAX</span></span>

### <span data-ttu-id="65b69-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65b69-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65b69-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="65b69-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65b69-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65b69-107">DESCRIPTION</span></span>
<span data-ttu-id="65b69-108">Получение сведений о ресурсе типа управляемого узла.</span><span class="sxs-lookup"><span data-stu-id="65b69-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="65b69-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65b69-109">EXAMPLES</span></span>

### <span data-ttu-id="65b69-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65b69-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="65b69-111">Получение сведений о типе узла.</span><span class="sxs-lookup"><span data-stu-id="65b69-111">Get node type details.</span></span>

### <span data-ttu-id="65b69-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="65b69-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="65b69-113">Получение списка типов узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="65b69-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="65b69-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65b69-114">PARAMETERS</span></span>

### <span data-ttu-id="65b69-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="65b69-115">-ClusterName</span></span>
<span data-ttu-id="65b69-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="65b69-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b69-117">-DefaultProfile</span></span>
<span data-ttu-id="65b69-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65b69-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b69-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="65b69-119">-Name</span></span>
<span data-ttu-id="65b69-120">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="65b69-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b69-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b69-121">-ResourceGroupName</span></span>
<span data-ttu-id="65b69-122">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65b69-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b69-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b69-123">CommonParameters</span></span>
<span data-ttu-id="65b69-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65b69-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b69-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65b69-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b69-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65b69-126">INPUTS</span></span>

### <span data-ttu-id="65b69-127">System. String</span><span class="sxs-lookup"><span data-stu-id="65b69-127">System.String</span></span>

## <span data-ttu-id="65b69-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65b69-128">OUTPUTS</span></span>

### <span data-ttu-id="65b69-129">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="65b69-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="65b69-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="65b69-130">NOTES</span></span>

## <span data-ttu-id="65b69-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65b69-131">RELATED LINKS</span></span>
