---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: cdf8c04a3d3b3b9fc50e571642bc14352d976b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566976"
---
# <span data-ttu-id="c831c-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="c831c-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="c831c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c831c-102">SYNOPSIS</span></span>
<span data-ttu-id="c831c-103">Получает клавиши доступа, связанные с кластером для выфункционирования.</span><span class="sxs-lookup"><span data-stu-id="c831c-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c831c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c831c-104">SYNTAX</span></span>

### <span data-ttu-id="c831c-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c831c-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c831c-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c831c-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c831c-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c831c-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c831c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c831c-108">DESCRIPTION</span></span>
<span data-ttu-id="c831c-109">Ключи для учетной записи хранения, реестра контейнера и других служб, связанных с кластером операций, не возвращаются при извлечении свойств кластера.</span><span class="sxs-lookup"><span data-stu-id="c831c-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="c831c-110">Конкретный вызов для получения ключей должен быть сделан, так как они являются конфиденциальной информацией.</span><span class="sxs-lookup"><span data-stu-id="c831c-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="c831c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c831c-111">EXAMPLES</span></span>

### <span data-ttu-id="c831c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c831c-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="c831c-113">Возвращает секретные ключи для служб, связанных с кластером операций.</span><span class="sxs-lookup"><span data-stu-id="c831c-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="c831c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c831c-114">PARAMETERS</span></span>

### <span data-ttu-id="c831c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c831c-115">-DefaultProfile</span></span>
<span data-ttu-id="c831c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c831c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c831c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c831c-117">-InputObject</span></span>
<span data-ttu-id="c831c-118">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="c831c-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c831c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c831c-119">-Name</span></span>
<span data-ttu-id="c831c-120">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="c831c-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c831c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c831c-121">-ResourceGroupName</span></span>
<span data-ttu-id="c831c-122">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="c831c-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c831c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c831c-123">-ResourceId</span></span>
<span data-ttu-id="c831c-124">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="c831c-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c831c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c831c-125">CommonParameters</span></span>
<span data-ttu-id="c831c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c831c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c831c-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c831c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c831c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c831c-128">INPUTS</span></span>

### <span data-ttu-id="c831c-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="c831c-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="c831c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c831c-130">System.String</span></span>

## <span data-ttu-id="c831c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c831c-131">OUTPUTS</span></span>

### <span data-ttu-id="c831c-132">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="c831c-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="c831c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c831c-133">NOTES</span></span>

## <span data-ttu-id="c831c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c831c-134">RELATED LINKS</span></span>

