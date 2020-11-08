---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: a0625a974da7d6544345419573fa4e96f0bbcae1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94088009"
---
# <span data-ttu-id="5da64-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5da64-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="5da64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5da64-102">SYNOPSIS</span></span>
<span data-ttu-id="5da64-103">Получение подробных сведений о типе приложения в структуре служб.</span><span class="sxs-lookup"><span data-stu-id="5da64-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="5da64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5da64-104">SYNTAX</span></span>

### <span data-ttu-id="5da64-105">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5da64-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5da64-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5da64-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5da64-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5da64-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5da64-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5da64-108">DESCRIPTION</span></span>
<span data-ttu-id="5da64-109">Используйте этот командлет, чтобы получить сведения о типе приложения в заданной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="5da64-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="5da64-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5da64-110">EXAMPLES</span></span>

### <span data-ttu-id="5da64-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5da64-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="5da64-112">В этом примере будут получены сведения о типе приложения с заданными параметрами, если он не находит ресурс, который вызывает исключение.</span><span class="sxs-lookup"><span data-stu-id="5da64-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="5da64-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5da64-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="5da64-114">В этом примере будет получен список типов приложений, определенных в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="5da64-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="5da64-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5da64-115">PARAMETERS</span></span>

### <span data-ttu-id="5da64-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="5da64-116">-ClusterName</span></span>
<span data-ttu-id="5da64-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="5da64-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5da64-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da64-118">-DefaultProfile</span></span>
<span data-ttu-id="5da64-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5da64-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5da64-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5da64-120">-Name</span></span>
<span data-ttu-id="5da64-121">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="5da64-121">Specify the name of the application type</span></span>

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

### <span data-ttu-id="5da64-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da64-122">-ResourceGroupName</span></span>
<span data-ttu-id="5da64-123">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5da64-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5da64-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5da64-124">-ResourceId</span></span>
<span data-ttu-id="5da64-125">Значение ResourceId для типа приложения.</span><span class="sxs-lookup"><span data-stu-id="5da64-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="5da64-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da64-126">CommonParameters</span></span>
<span data-ttu-id="5da64-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5da64-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da64-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5da64-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da64-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5da64-129">INPUTS</span></span>

### <span data-ttu-id="5da64-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5da64-130">System.String</span></span>

## <span data-ttu-id="5da64-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5da64-131">OUTPUTS</span></span>

### <span data-ttu-id="5da64-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="5da64-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="5da64-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5da64-133">NOTES</span></span>

## <span data-ttu-id="5da64-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5da64-134">RELATED LINKS</span></span>
