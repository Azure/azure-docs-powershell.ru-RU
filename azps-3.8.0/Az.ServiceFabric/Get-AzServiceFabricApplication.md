---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: e78580f98ae0569a2104a4d39123070e7383fa6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074291"
---
# <span data-ttu-id="c42b1-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c42b1-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="c42b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c42b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c42b1-103">Получение сведений о приложении "структура служб".</span><span class="sxs-lookup"><span data-stu-id="c42b1-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="c42b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c42b1-104">SYNTAX</span></span>

### <span data-ttu-id="c42b1-105">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c42b1-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c42b1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c42b1-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c42b1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c42b1-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c42b1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c42b1-108">DESCRIPTION</span></span>
<span data-ttu-id="c42b1-109">Этот командлет получает сведения о приложении в заданной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="c42b1-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="c42b1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c42b1-110">EXAMPLES</span></span>

### <span data-ttu-id="c42b1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c42b1-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="c42b1-112">В этом примере показано получение сведений о ресурсах приложения для приложения "testApp".</span><span class="sxs-lookup"><span data-stu-id="c42b1-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="c42b1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c42b1-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="c42b1-114">В этом примере показано получение списка приложений в кластере "testCluster".</span><span class="sxs-lookup"><span data-stu-id="c42b1-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="c42b1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c42b1-115">PARAMETERS</span></span>

### <span data-ttu-id="c42b1-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="c42b1-116">-ClusterName</span></span>
<span data-ttu-id="c42b1-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="c42b1-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c42b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42b1-118">-DefaultProfile</span></span>
<span data-ttu-id="c42b1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c42b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c42b1-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c42b1-120">-Name</span></span>
<span data-ttu-id="c42b1-121">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="c42b1-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="c42b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c42b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="c42b1-123">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c42b1-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c42b1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c42b1-124">-ResourceId</span></span>
<span data-ttu-id="c42b1-125">ИД ресурса ARM приложения.</span><span class="sxs-lookup"><span data-stu-id="c42b1-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="c42b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42b1-126">CommonParameters</span></span>
<span data-ttu-id="c42b1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c42b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42b1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c42b1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42b1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c42b1-129">INPUTS</span></span>

### <span data-ttu-id="c42b1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c42b1-130">System.String</span></span>

## <span data-ttu-id="c42b1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c42b1-131">OUTPUTS</span></span>

### <span data-ttu-id="c42b1-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="c42b1-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="c42b1-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c42b1-133">NOTES</span></span>

## <span data-ttu-id="c42b1-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c42b1-134">RELATED LINKS</span></span>
