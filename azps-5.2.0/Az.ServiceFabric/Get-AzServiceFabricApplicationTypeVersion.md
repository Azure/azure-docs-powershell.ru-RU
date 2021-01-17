---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7dc8ca2302b00b5eb200c30aed104f5fe5ff8642
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403007"
---
# <span data-ttu-id="49be4-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="49be4-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="49be4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49be4-102">SYNOPSIS</span></span>
<span data-ttu-id="49be4-103">Сведения о типе версии приложения "Служивная ткань".</span><span class="sxs-lookup"><span data-stu-id="49be4-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="49be4-104">Поддерживаются только ARM развернутые версии приложений.</span><span class="sxs-lookup"><span data-stu-id="49be4-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="49be4-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49be4-105">SYNTAX</span></span>

### <span data-ttu-id="49be4-106">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49be4-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49be4-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="49be4-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49be4-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="49be4-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49be4-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49be4-109">DESCRIPTION</span></span>
<span data-ttu-id="49be4-110">Используйте этот cmdlet, чтобы получить сведения о версии приложения в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="49be4-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="49be4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49be4-111">EXAMPLES</span></span>

### <span data-ttu-id="49be4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49be4-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="49be4-113">В этом примере тип приложения TestAppType с версией "v1" возвращается как "testAppType", если ресурс не будет обнаружиться, будет выбрасываться исключение.</span><span class="sxs-lookup"><span data-stu-id="49be4-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="49be4-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="49be4-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="49be4-115">В этом примере возвращается список версий типа приложения, определенных в указанном кластере и типе.</span><span class="sxs-lookup"><span data-stu-id="49be4-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="49be4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49be4-116">PARAMETERS</span></span>

### <span data-ttu-id="49be4-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="49be4-117">-ClusterName</span></span>
<span data-ttu-id="49be4-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="49be4-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="49be4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49be4-119">-DefaultProfile</span></span>
<span data-ttu-id="49be4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49be4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49be4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="49be4-121">-Name</span></span>
<span data-ttu-id="49be4-122">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="49be4-122">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="49be4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49be4-123">-ResourceGroupName</span></span>
<span data-ttu-id="49be4-124">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49be4-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="49be4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49be4-125">-ResourceId</span></span>
<span data-ttu-id="49be4-126">Arm ResourceId версии приложения.</span><span class="sxs-lookup"><span data-stu-id="49be4-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="49be4-127">-Version</span><span class="sxs-lookup"><span data-stu-id="49be4-127">-Version</span></span>
<span data-ttu-id="49be4-128">Укажите версию типа приложения.</span><span class="sxs-lookup"><span data-stu-id="49be4-128">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="49be4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49be4-129">CommonParameters</span></span>
<span data-ttu-id="49be4-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49be4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49be4-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49be4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49be4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49be4-132">INPUTS</span></span>

### <span data-ttu-id="49be4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="49be4-133">System.String</span></span>

## <span data-ttu-id="49be4-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49be4-134">OUTPUTS</span></span>

### <span data-ttu-id="49be4-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="49be4-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="49be4-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49be4-136">NOTES</span></span>

## <span data-ttu-id="49be4-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49be4-137">RELATED LINKS</span></span>
