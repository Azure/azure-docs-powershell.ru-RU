---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 9c9f1b3c88e49eca3be8a923324d195d3a773c1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974312"
---
# <span data-ttu-id="452d3-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="452d3-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="452d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="452d3-102">SYNOPSIS</span></span>
<span data-ttu-id="452d3-103">Получить сведения о типе версии приложения "Служивная ткань".</span><span class="sxs-lookup"><span data-stu-id="452d3-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="452d3-104">Поддерживаются только ARM развернутые версии приложений.</span><span class="sxs-lookup"><span data-stu-id="452d3-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="452d3-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="452d3-105">SYNTAX</span></span>

### <span data-ttu-id="452d3-106">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="452d3-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="452d3-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="452d3-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="452d3-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="452d3-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="452d3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="452d3-109">DESCRIPTION</span></span>
<span data-ttu-id="452d3-110">Используйте этот cmdlet, чтобы получить сведения о версии приложения в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="452d3-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="452d3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="452d3-111">EXAMPLES</span></span>

### <span data-ttu-id="452d3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="452d3-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="452d3-113">В этом примере тип приложения TestAppType с версией "v1" возвращается как "testAppType", если ресурс не будет обнаружиться, будет выбрасываться исключение.</span><span class="sxs-lookup"><span data-stu-id="452d3-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="452d3-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="452d3-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="452d3-115">В этом примере возвращается список версий типа приложения, определенных в указанном кластере и типе.</span><span class="sxs-lookup"><span data-stu-id="452d3-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="452d3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="452d3-116">PARAMETERS</span></span>

### <span data-ttu-id="452d3-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="452d3-117">-ClusterName</span></span>
<span data-ttu-id="452d3-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="452d3-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="452d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="452d3-119">-DefaultProfile</span></span>
<span data-ttu-id="452d3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="452d3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="452d3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="452d3-121">-Name</span></span>
<span data-ttu-id="452d3-122">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="452d3-122">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="452d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="452d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="452d3-124">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="452d3-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="452d3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="452d3-125">-ResourceId</span></span>
<span data-ttu-id="452d3-126">Arm ResourceId версии приложения.</span><span class="sxs-lookup"><span data-stu-id="452d3-126">Arm ResourceId of the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="452d3-127">-Version</span><span class="sxs-lookup"><span data-stu-id="452d3-127">-Version</span></span>
<span data-ttu-id="452d3-128">Укажите версию типа приложения.</span><span class="sxs-lookup"><span data-stu-id="452d3-128">Specify the version of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVersion
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="452d3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452d3-129">CommonParameters</span></span>
<span data-ttu-id="452d3-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="452d3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452d3-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="452d3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452d3-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="452d3-132">INPUTS</span></span>

### <span data-ttu-id="452d3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="452d3-133">System.String</span></span>

## <span data-ttu-id="452d3-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="452d3-134">OUTPUTS</span></span>

### <span data-ttu-id="452d3-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="452d3-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="452d3-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="452d3-136">NOTES</span></span>

## <span data-ttu-id="452d3-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="452d3-137">RELATED LINKS</span></span>
