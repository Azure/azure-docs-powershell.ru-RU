---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 78cec82383c257e325c35d0987de73f37aff253d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903770"
---
# <span data-ttu-id="29cde-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="29cde-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="29cde-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29cde-102">SYNOPSIS</span></span>
<span data-ttu-id="29cde-103">Получение подробных сведений о типе приложения в структуре служб.</span><span class="sxs-lookup"><span data-stu-id="29cde-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="29cde-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29cde-104">SYNTAX</span></span>

### <span data-ttu-id="29cde-105">ByResourceGroupAndCluster (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29cde-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29cde-106">ByName</span><span class="sxs-lookup"><span data-stu-id="29cde-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29cde-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="29cde-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29cde-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29cde-108">DESCRIPTION</span></span>
<span data-ttu-id="29cde-109">Используйте этот командлет, чтобы получить сведения о типе приложения в заданной группе ресурсов и кластере.</span><span class="sxs-lookup"><span data-stu-id="29cde-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="29cde-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29cde-110">EXAMPLES</span></span>

### <span data-ttu-id="29cde-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="29cde-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="29cde-112">В этом примере будут получены сведения о типе приложения с заданными параметрами, если он не находит ресурс, который вызывает исключение.</span><span class="sxs-lookup"><span data-stu-id="29cde-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="29cde-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="29cde-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="29cde-114">В этом примере будет получен список типов приложений, определенных в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="29cde-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="29cde-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29cde-115">PARAMETERS</span></span>

### <span data-ttu-id="29cde-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="29cde-116">-ClusterName</span></span>
<span data-ttu-id="29cde-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="29cde-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="29cde-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29cde-118">-DefaultProfile</span></span>
<span data-ttu-id="29cde-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29cde-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29cde-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="29cde-120">-Name</span></span>
<span data-ttu-id="29cde-121">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="29cde-121">Specify the name of the application type</span></span>

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

### <span data-ttu-id="29cde-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29cde-122">-ResourceGroupName</span></span>
<span data-ttu-id="29cde-123">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29cde-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="29cde-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29cde-124">-ResourceId</span></span>
<span data-ttu-id="29cde-125">Значение ResourceId для типа приложения.</span><span class="sxs-lookup"><span data-stu-id="29cde-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="29cde-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29cde-126">CommonParameters</span></span>
<span data-ttu-id="29cde-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29cde-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29cde-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29cde-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29cde-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29cde-129">INPUTS</span></span>

### <span data-ttu-id="29cde-130">System. String</span><span class="sxs-lookup"><span data-stu-id="29cde-130">System.String</span></span>

## <span data-ttu-id="29cde-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29cde-131">OUTPUTS</span></span>

### <span data-ttu-id="29cde-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="29cde-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="29cde-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="29cde-133">NOTES</span></span>

## <span data-ttu-id="29cde-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29cde-134">RELATED LINKS</span></span>
