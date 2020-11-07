---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733360"
---
# <span data-ttu-id="99f44-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="99f44-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="99f44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99f44-102">SYNOPSIS</span></span>
<span data-ttu-id="99f44-103">Проверка наличия обновлений для системных служб, связанных с кластером работоспособности.</span><span class="sxs-lookup"><span data-stu-id="99f44-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99f44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99f44-104">SYNTAX</span></span>

### <span data-ttu-id="99f44-105">Проверка доступности обновления на основании входных параметров командлета.</span><span class="sxs-lookup"><span data-stu-id="99f44-105">Test for update availability from cmdlet input parameters.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="99f44-106">Проверка доступности обновления из определения экземпляра OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="99f44-106">Test for update availability from an OperationalizationCluster instance definition.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### <span data-ttu-id="99f44-107">Проверка доступности обновления из идентификатора Azure ресурс.</span><span class="sxs-lookup"><span data-stu-id="99f44-107">Test for update availability from an Azure resouce id.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## <span data-ttu-id="99f44-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99f44-108">DESCRIPTION</span></span>
<span data-ttu-id="99f44-109">Системные службы получают обновления независимо от кластера операций.</span><span class="sxs-lookup"><span data-stu-id="99f44-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="99f44-110">С помощью этого командлета пользователь сможет узнать, если Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="99f44-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="99f44-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99f44-111">EXAMPLES</span></span>

### <span data-ttu-id="99f44-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="99f44-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="99f44-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="99f44-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="99f44-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="99f44-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="99f44-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99f44-115">PARAMETERS</span></span>

### <span data-ttu-id="99f44-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99f44-116">-InputObject</span></span>
<span data-ttu-id="99f44-117">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="99f44-117">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99f44-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99f44-118">-Name</span></span>
<span data-ttu-id="99f44-119">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="99f44-119">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f44-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f44-120">-ResourceGroupName</span></span>
<span data-ttu-id="99f44-121">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="99f44-121">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f44-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99f44-122">-ResourceId</span></span>
<span data-ttu-id="99f44-123">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="99f44-123">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="99f44-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99f44-124">INPUTS</span></span>

### <span data-ttu-id="99f44-125">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="99f44-125">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="99f44-126">System. String</span><span class="sxs-lookup"><span data-stu-id="99f44-126">System.String</span></span>


## <span data-ttu-id="99f44-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99f44-127">OUTPUTS</span></span>

### <span data-ttu-id="99f44-128">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="99f44-128">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>


## <span data-ttu-id="99f44-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="99f44-129">NOTES</span></span>

## <span data-ttu-id="99f44-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99f44-130">RELATED LINKS</span></span>

