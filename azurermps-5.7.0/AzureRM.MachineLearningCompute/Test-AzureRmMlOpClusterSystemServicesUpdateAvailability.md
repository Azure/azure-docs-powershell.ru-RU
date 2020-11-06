---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9f531b67d2dc3cc6010a7677c96dc4ecf10fb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564847"
---
# <span data-ttu-id="779a9-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="779a9-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="779a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="779a9-102">SYNOPSIS</span></span>
<span data-ttu-id="779a9-103">Проверка наличия обновлений для системных служб, связанных с кластером работоспособности.</span><span class="sxs-lookup"><span data-stu-id="779a9-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="779a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="779a9-104">SYNTAX</span></span>

### <span data-ttu-id="779a9-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="779a9-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="779a9-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="779a9-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="779a9-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="779a9-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="779a9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="779a9-108">DESCRIPTION</span></span>
<span data-ttu-id="779a9-109">Системные службы получают обновления независимо от кластера операций.</span><span class="sxs-lookup"><span data-stu-id="779a9-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="779a9-110">С помощью этого командлета пользователь сможет узнать, если Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="779a9-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="779a9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="779a9-111">EXAMPLES</span></span>

### <span data-ttu-id="779a9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="779a9-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="779a9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="779a9-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="779a9-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="779a9-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="779a9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="779a9-115">PARAMETERS</span></span>

### <span data-ttu-id="779a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="779a9-116">-DefaultProfile</span></span>
<span data-ttu-id="779a9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="779a9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="779a9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="779a9-118">-InputObject</span></span>
<span data-ttu-id="779a9-119">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="779a9-119">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="779a9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="779a9-120">-Name</span></span>
<span data-ttu-id="779a9-121">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="779a9-121">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="779a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="779a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="779a9-123">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="779a9-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="779a9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="779a9-124">-ResourceId</span></span>
<span data-ttu-id="779a9-125">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="779a9-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="779a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="779a9-126">CommonParameters</span></span>
<span data-ttu-id="779a9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="779a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="779a9-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="779a9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="779a9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="779a9-129">INPUTS</span></span>

### <span data-ttu-id="779a9-130">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="779a9-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="779a9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="779a9-131">System.String</span></span>

## <span data-ttu-id="779a9-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="779a9-132">OUTPUTS</span></span>

### <span data-ttu-id="779a9-133">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="779a9-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="779a9-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="779a9-134">NOTES</span></span>

## <span data-ttu-id="779a9-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="779a9-135">RELATED LINKS</span></span>

