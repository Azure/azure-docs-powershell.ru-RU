---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 346664d4714836b9965088d946262257e76747e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963619"
---
# <span data-ttu-id="4071a-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4071a-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="4071a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4071a-102">SYNOPSIS</span></span>
<span data-ttu-id="4071a-103">Получить сведения о приложении "Служивная ткань".</span><span class="sxs-lookup"><span data-stu-id="4071a-103">Get Service Fabric application details.</span></span> <span data-ttu-id="4071a-104">Поддерживаются ARM только развернутые приложения.</span><span class="sxs-lookup"><span data-stu-id="4071a-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="4071a-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4071a-105">SYNTAX</span></span>

### <span data-ttu-id="4071a-106">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4071a-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4071a-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4071a-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4071a-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4071a-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4071a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4071a-109">DESCRIPTION</span></span>
<span data-ttu-id="4071a-110">Этот cmdlet получает сведения о приложении в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="4071a-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="4071a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4071a-111">EXAMPLES</span></span>

### <span data-ttu-id="4071a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4071a-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="4071a-113">В этом примере подробные сведения о ресурсах приложения testApp.</span><span class="sxs-lookup"><span data-stu-id="4071a-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="4071a-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4071a-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="4071a-115">В этом примере возвращается список приложений из кластера TestCluster.</span><span class="sxs-lookup"><span data-stu-id="4071a-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="4071a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4071a-116">PARAMETERS</span></span>

### <span data-ttu-id="4071a-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4071a-117">-ClusterName</span></span>
<span data-ttu-id="4071a-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="4071a-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4071a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4071a-119">-DefaultProfile</span></span>
<span data-ttu-id="4071a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4071a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4071a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4071a-121">-Name</span></span>
<span data-ttu-id="4071a-122">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="4071a-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="4071a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4071a-123">-ResourceGroupName</span></span>
<span data-ttu-id="4071a-124">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4071a-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4071a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4071a-125">-ResourceId</span></span>
<span data-ttu-id="4071a-126">Arm ResourceId приложения.</span><span class="sxs-lookup"><span data-stu-id="4071a-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="4071a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4071a-127">CommonParameters</span></span>
<span data-ttu-id="4071a-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4071a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4071a-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4071a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4071a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4071a-130">INPUTS</span></span>

### <span data-ttu-id="4071a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4071a-131">System.String</span></span>

## <span data-ttu-id="4071a-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4071a-132">OUTPUTS</span></span>

### <span data-ttu-id="4071a-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="4071a-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="4071a-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4071a-134">NOTES</span></span>

## <span data-ttu-id="4071a-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4071a-135">RELATED LINKS</span></span>
