---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 6b5797d67b709e9c44756dad018a47eb416ed174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564344"
---
# <span data-ttu-id="4697d-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="4697d-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="4697d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4697d-102">SYNOPSIS</span></span>
<span data-ttu-id="4697d-103">Получает клавиши доступа, связанные с кластером для выфункционирования.</span><span class="sxs-lookup"><span data-stu-id="4697d-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4697d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4697d-104">SYNTAX</span></span>

### <span data-ttu-id="4697d-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4697d-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4697d-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4697d-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4697d-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4697d-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4697d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4697d-108">DESCRIPTION</span></span>
<span data-ttu-id="4697d-109">Ключи для учетной записи хранения, реестра контейнера и других служб, связанных с кластером операций, не возвращаются при извлечении свойств кластера.</span><span class="sxs-lookup"><span data-stu-id="4697d-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="4697d-110">Конкретный вызов для получения ключей должен быть сделан, так как они являются конфиденциальной информацией.</span><span class="sxs-lookup"><span data-stu-id="4697d-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="4697d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4697d-111">EXAMPLES</span></span>

### <span data-ttu-id="4697d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4697d-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="4697d-113">Возвращает секретные ключи для служб, связанных с кластером операций.</span><span class="sxs-lookup"><span data-stu-id="4697d-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="4697d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4697d-114">PARAMETERS</span></span>

### <span data-ttu-id="4697d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4697d-115">-DefaultProfile</span></span>
<span data-ttu-id="4697d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4697d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4697d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4697d-117">-InputObject</span></span>
<span data-ttu-id="4697d-118">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="4697d-118">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4697d-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4697d-119">-Name</span></span>
<span data-ttu-id="4697d-120">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="4697d-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4697d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4697d-121">-ResourceGroupName</span></span>
<span data-ttu-id="4697d-122">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="4697d-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4697d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4697d-123">-ResourceId</span></span>
<span data-ttu-id="4697d-124">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="4697d-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4697d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4697d-125">CommonParameters</span></span>
<span data-ttu-id="4697d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4697d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4697d-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4697d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4697d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4697d-128">INPUTS</span></span>

### <span data-ttu-id="4697d-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="4697d-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="4697d-130">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4697d-130">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4697d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4697d-131">System.String</span></span>

## <span data-ttu-id="4697d-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4697d-132">OUTPUTS</span></span>

### <span data-ttu-id="4697d-133">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="4697d-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="4697d-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="4697d-134">NOTES</span></span>

## <span data-ttu-id="4697d-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4697d-135">RELATED LINKS</span></span>
