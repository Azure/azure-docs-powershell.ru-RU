---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 5946be075e2b97283546614543d5a0d4544bfa0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242136"
---
# <span data-ttu-id="e7f42-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e7f42-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="e7f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f42-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f42-103">Получить сведения о приложении "Служивная ткань".</span><span class="sxs-lookup"><span data-stu-id="e7f42-103">Get Service Fabric application details.</span></span> <span data-ttu-id="e7f42-104">Поддерживаются ARM только развернутые приложения.</span><span class="sxs-lookup"><span data-stu-id="e7f42-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="e7f42-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e7f42-105">SYNTAX</span></span>

### <span data-ttu-id="e7f42-106">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7f42-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7f42-107">ByName</span><span class="sxs-lookup"><span data-stu-id="e7f42-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7f42-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f42-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7f42-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7f42-109">DESCRIPTION</span></span>
<span data-ttu-id="e7f42-110">Этот cmdlet получает сведения о приложении в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="e7f42-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="e7f42-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e7f42-111">EXAMPLES</span></span>

### <span data-ttu-id="e7f42-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7f42-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="e7f42-113">В этом примере подробные сведения о ресурсах приложения testApp.</span><span class="sxs-lookup"><span data-stu-id="e7f42-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="e7f42-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e7f42-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="e7f42-115">В этом примере возвращается список приложений из кластера TestCluster.</span><span class="sxs-lookup"><span data-stu-id="e7f42-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="e7f42-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7f42-116">PARAMETERS</span></span>

### <span data-ttu-id="e7f42-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e7f42-117">-ClusterName</span></span>
<span data-ttu-id="e7f42-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="e7f42-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e7f42-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f42-119">-DefaultProfile</span></span>
<span data-ttu-id="e7f42-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7f42-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7f42-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e7f42-121">-Name</span></span>
<span data-ttu-id="e7f42-122">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="e7f42-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f42-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f42-123">-ResourceGroupName</span></span>
<span data-ttu-id="e7f42-124">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7f42-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e7f42-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f42-125">-ResourceId</span></span>
<span data-ttu-id="e7f42-126">Arm ResourceId приложения.</span><span class="sxs-lookup"><span data-stu-id="e7f42-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="e7f42-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f42-127">CommonParameters</span></span>
<span data-ttu-id="e7f42-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f42-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f42-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7f42-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f42-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7f42-130">INPUTS</span></span>

### <span data-ttu-id="e7f42-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e7f42-131">System.String</span></span>

## <span data-ttu-id="e7f42-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7f42-132">OUTPUTS</span></span>

### <span data-ttu-id="e7f42-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="e7f42-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="e7f42-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e7f42-134">NOTES</span></span>

## <span data-ttu-id="e7f42-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7f42-135">RELATED LINKS</span></span>
