---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9832faaaaf1097f53aff841f8a455680b2a40a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564336"
---
# <span data-ttu-id="df647-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="df647-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="df647-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df647-102">SYNOPSIS</span></span>
<span data-ttu-id="df647-103">Проверка наличия обновлений для системных служб, связанных с кластером работоспособности.</span><span class="sxs-lookup"><span data-stu-id="df647-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df647-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df647-104">SYNTAX</span></span>

### <span data-ttu-id="df647-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="df647-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df647-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="df647-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df647-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="df647-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df647-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df647-108">DESCRIPTION</span></span>
<span data-ttu-id="df647-109">Системные службы получают обновления независимо от кластера операций.</span><span class="sxs-lookup"><span data-stu-id="df647-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="df647-110">С помощью этого командлета пользователь сможет узнать, если Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="df647-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="df647-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df647-111">EXAMPLES</span></span>

### <span data-ttu-id="df647-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df647-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="df647-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="df647-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="df647-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="df647-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="df647-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df647-115">PARAMETERS</span></span>

### <span data-ttu-id="df647-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df647-116">-DefaultProfile</span></span>
<span data-ttu-id="df647-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df647-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df647-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df647-118">-InputObject</span></span>
<span data-ttu-id="df647-119">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="df647-119">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df647-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="df647-120">-Name</span></span>
<span data-ttu-id="df647-121">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="df647-121">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df647-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df647-122">-ResourceGroupName</span></span>
<span data-ttu-id="df647-123">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="df647-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df647-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df647-124">-ResourceId</span></span>
<span data-ttu-id="df647-125">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="df647-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df647-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df647-126">CommonParameters</span></span>
<span data-ttu-id="df647-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df647-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df647-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df647-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df647-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df647-129">INPUTS</span></span>

### <span data-ttu-id="df647-130">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="df647-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="df647-131">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="df647-131">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="df647-132">System. String</span><span class="sxs-lookup"><span data-stu-id="df647-132">System.String</span></span>

## <span data-ttu-id="df647-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df647-133">OUTPUTS</span></span>

### <span data-ttu-id="df647-134">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="df647-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="df647-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="df647-135">NOTES</span></span>

## <span data-ttu-id="df647-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df647-136">RELATED LINKS</span></span>
