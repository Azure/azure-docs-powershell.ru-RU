---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 0082f5625351b8bb8e832ad60eb76837f09ccd47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974323"
---
# <span data-ttu-id="1752e-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1752e-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="1752e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1752e-102">SYNOPSIS</span></span>
<span data-ttu-id="1752e-103">Получить сведения о типе приложения "Служивная ткань".</span><span class="sxs-lookup"><span data-stu-id="1752e-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="1752e-104">Поддерживаются только ARM развернутых типов приложений.</span><span class="sxs-lookup"><span data-stu-id="1752e-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="1752e-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1752e-105">SYNTAX</span></span>

### <span data-ttu-id="1752e-106">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1752e-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1752e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="1752e-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1752e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1752e-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1752e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1752e-109">DESCRIPTION</span></span>
<span data-ttu-id="1752e-110">Используйте этот cmdlet, чтобы получить сведения о типе приложения в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="1752e-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="1752e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1752e-111">EXAMPLES</span></span>

### <span data-ttu-id="1752e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1752e-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="1752e-113">В этом примере будут указаны сведения о типе приложения с заданными параметрами. Если ресурс не будет указан, будет выдано исключение.</span><span class="sxs-lookup"><span data-stu-id="1752e-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="1752e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1752e-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="1752e-115">В этом примере вы получите список типов приложений, определенных в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="1752e-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="1752e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1752e-116">PARAMETERS</span></span>

### <span data-ttu-id="1752e-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1752e-117">-ClusterName</span></span>
<span data-ttu-id="1752e-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="1752e-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1752e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1752e-119">-DefaultProfile</span></span>
<span data-ttu-id="1752e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1752e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1752e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1752e-121">-Name</span></span>
<span data-ttu-id="1752e-122">Указание имени типа приложения</span><span class="sxs-lookup"><span data-stu-id="1752e-122">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1752e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1752e-123">-ResourceGroupName</span></span>
<span data-ttu-id="1752e-124">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1752e-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1752e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1752e-125">-ResourceId</span></span>
<span data-ttu-id="1752e-126">Arm ResourceId типа приложения.</span><span class="sxs-lookup"><span data-stu-id="1752e-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="1752e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1752e-127">CommonParameters</span></span>
<span data-ttu-id="1752e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1752e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1752e-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1752e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1752e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1752e-130">INPUTS</span></span>

### <span data-ttu-id="1752e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1752e-131">System.String</span></span>

## <span data-ttu-id="1752e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1752e-132">OUTPUTS</span></span>

### <span data-ttu-id="1752e-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="1752e-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="1752e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1752e-134">NOTES</span></span>

## <span data-ttu-id="1752e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1752e-135">RELATED LINKS</span></span>
