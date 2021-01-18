---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517262"
---
# <span data-ttu-id="ec78a-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ec78a-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="ec78a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec78a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec78a-103">Получите сведения о ресурсах типа "Управляемый узел".</span><span class="sxs-lookup"><span data-stu-id="ec78a-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="ec78a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec78a-104">SYNTAX</span></span>

### <span data-ttu-id="ec78a-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec78a-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec78a-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ec78a-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec78a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec78a-107">DESCRIPTION</span></span>
<span data-ttu-id="ec78a-108">Получите сведения о ресурсах типа "Управляемый узел".</span><span class="sxs-lookup"><span data-stu-id="ec78a-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="ec78a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec78a-109">EXAMPLES</span></span>

### <span data-ttu-id="ec78a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec78a-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="ec78a-111">Получите сведения о типе узла.</span><span class="sxs-lookup"><span data-stu-id="ec78a-111">Get node type details.</span></span>

### <span data-ttu-id="ec78a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ec78a-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="ec78a-113">Получить список типов узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="ec78a-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="ec78a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec78a-114">PARAMETERS</span></span>

### <span data-ttu-id="ec78a-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ec78a-115">-ClusterName</span></span>
<span data-ttu-id="ec78a-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ec78a-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ec78a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec78a-117">-DefaultProfile</span></span>
<span data-ttu-id="ec78a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec78a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec78a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ec78a-119">-Name</span></span>
<span data-ttu-id="ec78a-120">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="ec78a-120">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="ec78a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec78a-121">-ResourceGroupName</span></span>
<span data-ttu-id="ec78a-122">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec78a-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ec78a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec78a-123">CommonParameters</span></span>
<span data-ttu-id="ec78a-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec78a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec78a-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec78a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec78a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec78a-126">INPUTS</span></span>

### <span data-ttu-id="ec78a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ec78a-127">System.String</span></span>

## <span data-ttu-id="ec78a-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec78a-128">OUTPUTS</span></span>

### <span data-ttu-id="ec78a-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ec78a-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="ec78a-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec78a-130">NOTES</span></span>

## <span data-ttu-id="ec78a-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec78a-131">RELATED LINKS</span></span>
