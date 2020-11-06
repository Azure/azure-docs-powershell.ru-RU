---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567592"
---
# <span data-ttu-id="7802e-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="7802e-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="7802e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7802e-102">SYNOPSIS</span></span>
<span data-ttu-id="7802e-103">Получает клавиши доступа, связанные с кластером для выфункционирования.</span><span class="sxs-lookup"><span data-stu-id="7802e-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7802e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7802e-104">SYNTAX</span></span>

### <span data-ttu-id="7802e-105">Получите ключи кластера операций в ходе работы входных параметров командлета.</span><span class="sxs-lookup"><span data-stu-id="7802e-105">Get operationalization cluster's keys from cmdlet input parameters.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="7802e-106">Получите ключи кластера операций для работы с помощью определения экземпляра OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="7802e-106">Get operationalization cluster's keys from an OperationalizationCluster instance definition.</span></span>
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### <span data-ttu-id="7802e-107">Получите ключи кластера для операции оборганизации из идентификатора ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="7802e-107">Get operationalization cluster's keys from an Azure resource id.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## <span data-ttu-id="7802e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7802e-108">DESCRIPTION</span></span>
<span data-ttu-id="7802e-109">Ключи для учетной записи хранения, реестра контейнера и других служб, связанных с кластером операций, не возвращаются при извлечении свойств кластера.</span><span class="sxs-lookup"><span data-stu-id="7802e-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="7802e-110">Конкретный вызов для получения ключей должен быть сделан, так как они являются конфиденциальной информацией.</span><span class="sxs-lookup"><span data-stu-id="7802e-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="7802e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7802e-111">EXAMPLES</span></span>

### <span data-ttu-id="7802e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7802e-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="7802e-113">Возвращает секретные ключи для служб, связанных с кластером операций.</span><span class="sxs-lookup"><span data-stu-id="7802e-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="7802e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7802e-114">PARAMETERS</span></span>

### <span data-ttu-id="7802e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7802e-115">-InputObject</span></span>
<span data-ttu-id="7802e-116">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="7802e-116">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7802e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7802e-117">-Name</span></span>
<span data-ttu-id="7802e-118">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="7802e-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7802e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7802e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7802e-120">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="7802e-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7802e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7802e-121">-ResourceId</span></span>
<span data-ttu-id="7802e-122">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="7802e-122">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="7802e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7802e-123">INPUTS</span></span>

### <span data-ttu-id="7802e-124">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="7802e-124">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="7802e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7802e-125">System.String</span></span>


## <span data-ttu-id="7802e-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7802e-126">OUTPUTS</span></span>

### <span data-ttu-id="7802e-127">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="7802e-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>


## <span data-ttu-id="7802e-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="7802e-128">NOTES</span></span>

## <span data-ttu-id="7802e-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7802e-129">RELATED LINKS</span></span>

