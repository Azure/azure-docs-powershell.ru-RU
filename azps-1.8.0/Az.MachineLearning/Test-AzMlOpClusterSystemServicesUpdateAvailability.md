---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/test-azmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: d05f8b746dbd212c834e3554639340fa6075c216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899730"
---
# <span data-ttu-id="5b8ca-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="5b8ca-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="5b8ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b8ca-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8ca-103">Проверка наличия обновлений для системных служб, связанных с кластером работоспособности.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

## <span data-ttu-id="5b8ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b8ca-104">SYNTAX</span></span>

### <span data-ttu-id="5b8ca-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b8ca-105">TestByNameAndResourceGroup</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b8ca-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b8ca-106">TestByInputObject</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b8ca-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b8ca-107">TestByResourceId</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b8ca-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b8ca-108">DESCRIPTION</span></span>
<span data-ttu-id="5b8ca-109">Системные службы получают обновления независимо от кластера операций.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="5b8ca-110">С помощью этого командлета пользователь сможет узнать, если Invoke-AzMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-110">Using this cmdlet will let the user know if Invoke-AzMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="5b8ca-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b8ca-111">EXAMPLES</span></span>

### <span data-ttu-id="5b8ca-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b8ca-112">Example 1</span></span>
```
PS C:\> Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="5b8ca-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5b8ca-113">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="5b8ca-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5b8ca-114">Example 3</span></span>
```
PS C:\> Find-AzResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="5b8ca-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b8ca-115">PARAMETERS</span></span>

### <span data-ttu-id="5b8ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b8ca-116">-DefaultProfile</span></span>
<span data-ttu-id="5b8ca-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b8ca-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b8ca-118">-InputObject</span></span>
<span data-ttu-id="5b8ca-119">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-119">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="5b8ca-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b8ca-120">-Name</span></span>
<span data-ttu-id="5b8ca-121">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-121">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="5b8ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b8ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b8ca-123">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-123">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="5b8ca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b8ca-124">-ResourceId</span></span>
<span data-ttu-id="5b8ca-125">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="5b8ca-125">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="5b8ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8ca-126">CommonParameters</span></span>
<span data-ttu-id="5b8ca-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b8ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8ca-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b8ca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8ca-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b8ca-129">INPUTS</span></span>

### <span data-ttu-id="5b8ca-130">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="5b8ca-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="5b8ca-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5b8ca-131">System.String</span></span>

## <span data-ttu-id="5b8ca-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b8ca-132">OUTPUTS</span></span>

### <span data-ttu-id="5b8ca-133">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="5b8ca-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="5b8ca-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b8ca-134">NOTES</span></span>

## <span data-ttu-id="5b8ca-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b8ca-135">RELATED LINKS</span></span>
