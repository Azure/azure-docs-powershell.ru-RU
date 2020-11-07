---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
ms.openlocfilehash: d8b8a333b4d009ee1b40a8b4ddc6ed49850f1a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720449"
---
# <span data-ttu-id="a6ac9-101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="a6ac9-101">Get-AzMlOpClusterKey</span></span>

## <span data-ttu-id="a6ac9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ac9-103">Получает клавиши доступа, связанные с кластером для выфункционирования.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-103">Gets the access keys associated with an operationalization cluster.</span></span>

## <span data-ttu-id="a6ac9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6ac9-104">SYNTAX</span></span>

### <span data-ttu-id="a6ac9-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a6ac9-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6ac9-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a6ac9-106">GetByInputObject</span></span>
```
Get-AzMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6ac9-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a6ac9-107">GetByResourceId</span></span>
```
Get-AzMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6ac9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6ac9-108">DESCRIPTION</span></span>
<span data-ttu-id="a6ac9-109">Ключи для учетной записи хранения, реестра контейнера и других служб, связанных с кластером операций, не возвращаются при извлечении свойств кластера.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="a6ac9-110">Конкретный вызов для получения ключей должен быть сделан, так как они являются конфиденциальной информацией.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="a6ac9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6ac9-111">EXAMPLES</span></span>

### <span data-ttu-id="a6ac9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6ac9-112">Example 1</span></span>
```
PS C:\> Get-AzMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="a6ac9-113">Возвращает секретные ключи для служб, связанных с кластером операций.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="a6ac9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6ac9-114">PARAMETERS</span></span>

### <span data-ttu-id="a6ac9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ac9-115">-DefaultProfile</span></span>
<span data-ttu-id="a6ac9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6ac9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6ac9-117">-InputObject</span></span>
<span data-ttu-id="a6ac9-118">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-118">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="a6ac9-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6ac9-119">-Name</span></span>
<span data-ttu-id="a6ac9-120">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="a6ac9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ac9-121">-ResourceGroupName</span></span>
<span data-ttu-id="a6ac9-122">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="a6ac9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6ac9-123">-ResourceId</span></span>
<span data-ttu-id="a6ac9-124">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="a6ac9-124">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="a6ac9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ac9-125">CommonParameters</span></span>
<span data-ttu-id="a6ac9-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ac9-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6ac9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ac9-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6ac9-128">INPUTS</span></span>

### <span data-ttu-id="a6ac9-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="a6ac9-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="a6ac9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a6ac9-130">System.String</span></span>

## <span data-ttu-id="a6ac9-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6ac9-131">OUTPUTS</span></span>

### <span data-ttu-id="a6ac9-132">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="a6ac9-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="a6ac9-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6ac9-133">NOTES</span></span>

## <span data-ttu-id="a6ac9-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6ac9-134">RELATED LINKS</span></span>
