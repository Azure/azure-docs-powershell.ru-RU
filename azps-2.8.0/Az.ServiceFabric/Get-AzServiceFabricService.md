---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 3076a405c47f165d2ace1e5251644cf4e4484a03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903762"
---
# <span data-ttu-id="00dcf-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="00dcf-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="00dcf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="00dcf-103">Получение сведений о службе фабрики служб в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="00dcf-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="00dcf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00dcf-104">SYNTAX</span></span>

### <span data-ttu-id="00dcf-105">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00dcf-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00dcf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="00dcf-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00dcf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00dcf-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00dcf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00dcf-108">DESCRIPTION</span></span>
<span data-ttu-id="00dcf-109">Этот командлет получит сведения о службе в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="00dcf-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="00dcf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00dcf-110">EXAMPLES</span></span>

### <span data-ttu-id="00dcf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00dcf-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="00dcf-112">В этом примере получает сведения о ресурсе службы для службы "testApp ~ testService".</span><span class="sxs-lookup"><span data-stu-id="00dcf-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="00dcf-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="00dcf-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="00dcf-114">В этом примере возвращается список служб в Aplication "testApp".</span><span class="sxs-lookup"><span data-stu-id="00dcf-114">This example gets a list of the services under the aplication "testApp".</span></span>

## <span data-ttu-id="00dcf-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00dcf-115">PARAMETERS</span></span>

### <span data-ttu-id="00dcf-116">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="00dcf-116">-ApplicationName</span></span>
<span data-ttu-id="00dcf-117">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="00dcf-117">Specify the name of the application.</span></span>

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

### <span data-ttu-id="00dcf-118">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="00dcf-118">-ClusterName</span></span>
<span data-ttu-id="00dcf-119">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="00dcf-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="00dcf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00dcf-120">-DefaultProfile</span></span>
<span data-ttu-id="00dcf-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00dcf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00dcf-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00dcf-122">-Name</span></span>
<span data-ttu-id="00dcf-123">Укажите имя службы.</span><span class="sxs-lookup"><span data-stu-id="00dcf-123">Specify the name of the service.</span></span>

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

### <span data-ttu-id="00dcf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00dcf-124">-ResourceGroupName</span></span>
<span data-ttu-id="00dcf-125">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="00dcf-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="00dcf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00dcf-126">-ResourceId</span></span>
<span data-ttu-id="00dcf-127">ResourceId (ИД) для службы.</span><span class="sxs-lookup"><span data-stu-id="00dcf-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="00dcf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00dcf-128">CommonParameters</span></span>
<span data-ttu-id="00dcf-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00dcf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00dcf-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00dcf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00dcf-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00dcf-131">INPUTS</span></span>

### <span data-ttu-id="00dcf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="00dcf-132">System.String</span></span>

## <span data-ttu-id="00dcf-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00dcf-133">OUTPUTS</span></span>

### <span data-ttu-id="00dcf-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="00dcf-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="00dcf-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="00dcf-135">NOTES</span></span>

## <span data-ttu-id="00dcf-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00dcf-136">RELATED LINKS</span></span>
