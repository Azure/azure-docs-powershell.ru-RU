---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: ea86fb4a110d355a848b9fe58969d30ccb96e2da
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078738"
---
# <span data-ttu-id="106e1-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="106e1-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="106e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="106e1-102">SYNOPSIS</span></span>
<span data-ttu-id="106e1-103">Получение сведений о версии для типа приложения "структура обслуживания".</span><span class="sxs-lookup"><span data-stu-id="106e1-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="106e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="106e1-104">SYNTAX</span></span>

### <span data-ttu-id="106e1-105">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="106e1-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="106e1-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="106e1-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="106e1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="106e1-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="106e1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="106e1-108">DESCRIPTION</span></span>
<span data-ttu-id="106e1-109">Используйте этот командлет, чтобы получить сведения о версии типа приложения в указанной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="106e1-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="106e1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="106e1-110">EXAMPLES</span></span>

### <span data-ttu-id="106e1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="106e1-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="106e1-112">В этом примере получается тип приложения "testAppType" с версией v1, если он не находит ресурс, который вызывает исключение.</span><span class="sxs-lookup"><span data-stu-id="106e1-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="106e1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="106e1-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="106e1-114">В этом примере показано получение списка версий типа приложения, определенных в указанном кластере и типе.</span><span class="sxs-lookup"><span data-stu-id="106e1-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="106e1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="106e1-115">PARAMETERS</span></span>

### <span data-ttu-id="106e1-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="106e1-116">-ClusterName</span></span>
<span data-ttu-id="106e1-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="106e1-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="106e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106e1-118">-DefaultProfile</span></span>
<span data-ttu-id="106e1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="106e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="106e1-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="106e1-120">-Name</span></span>
<span data-ttu-id="106e1-121">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="106e1-121">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="106e1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="106e1-122">-ResourceGroupName</span></span>
<span data-ttu-id="106e1-123">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="106e1-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="106e1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="106e1-124">-ResourceId</span></span>
<span data-ttu-id="106e1-125">Значение ResourceId для версии типа приложения.</span><span class="sxs-lookup"><span data-stu-id="106e1-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="106e1-126">-Version</span><span class="sxs-lookup"><span data-stu-id="106e1-126">-Version</span></span>
<span data-ttu-id="106e1-127">Укажите версию типа приложения.</span><span class="sxs-lookup"><span data-stu-id="106e1-127">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="106e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106e1-128">CommonParameters</span></span>
<span data-ttu-id="106e1-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="106e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106e1-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="106e1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106e1-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="106e1-131">INPUTS</span></span>

### <span data-ttu-id="106e1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="106e1-132">System.String</span></span>

## <span data-ttu-id="106e1-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="106e1-133">OUTPUTS</span></span>

### <span data-ttu-id="106e1-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="106e1-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="106e1-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="106e1-135">NOTES</span></span>

## <span data-ttu-id="106e1-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="106e1-136">RELATED LINKS</span></span>