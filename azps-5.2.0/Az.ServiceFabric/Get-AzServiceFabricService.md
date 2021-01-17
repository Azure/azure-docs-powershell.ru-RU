---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323220"
---
# <span data-ttu-id="2cc87-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2cc87-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="2cc87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cc87-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc87-103">Получить сведения о службе "Ткань услуги" в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="2cc87-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="2cc87-104">Поддерживаются только ARM развернутые службы.</span><span class="sxs-lookup"><span data-stu-id="2cc87-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="2cc87-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2cc87-105">SYNTAX</span></span>

### <span data-ttu-id="2cc87-106">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2cc87-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc87-107">ByName</span><span class="sxs-lookup"><span data-stu-id="2cc87-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc87-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2cc87-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cc87-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cc87-109">DESCRIPTION</span></span>
<span data-ttu-id="2cc87-110">Этот cmdlet получит сведения о службе в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="2cc87-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="2cc87-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2cc87-111">EXAMPLES</span></span>

### <span data-ttu-id="2cc87-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2cc87-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="2cc87-113">В этом примере подробные сведения о ресурсе службы testApp~testService.</span><span class="sxs-lookup"><span data-stu-id="2cc87-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="2cc87-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2cc87-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="2cc87-115">В этом примере в приложении TestApp приводится список служб.</span><span class="sxs-lookup"><span data-stu-id="2cc87-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="2cc87-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cc87-116">PARAMETERS</span></span>

### <span data-ttu-id="2cc87-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="2cc87-117">-ApplicationName</span></span>
<span data-ttu-id="2cc87-118">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="2cc87-118">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc87-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2cc87-119">-ClusterName</span></span>
<span data-ttu-id="2cc87-120">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="2cc87-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2cc87-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc87-121">-DefaultProfile</span></span>
<span data-ttu-id="2cc87-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cc87-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cc87-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2cc87-123">-Name</span></span>
<span data-ttu-id="2cc87-124">Укажите имя службы.</span><span class="sxs-lookup"><span data-stu-id="2cc87-124">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc87-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc87-125">-ResourceGroupName</span></span>
<span data-ttu-id="2cc87-126">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cc87-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2cc87-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cc87-127">-ResourceId</span></span>
<span data-ttu-id="2cc87-128">Arm ResourceId службы.</span><span class="sxs-lookup"><span data-stu-id="2cc87-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="2cc87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc87-129">CommonParameters</span></span>
<span data-ttu-id="2cc87-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc87-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cc87-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc87-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cc87-132">INPUTS</span></span>

### <span data-ttu-id="2cc87-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2cc87-133">System.String</span></span>

## <span data-ttu-id="2cc87-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2cc87-134">OUTPUTS</span></span>

### <span data-ttu-id="2cc87-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="2cc87-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="2cc87-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2cc87-136">NOTES</span></span>

## <span data-ttu-id="2cc87-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cc87-137">RELATED LINKS</span></span>
