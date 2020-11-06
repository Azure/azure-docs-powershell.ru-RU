---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 746dde8dd3460add5eb6a20e4a9b771873dac0e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564347"
---
# <span data-ttu-id="a52e5-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a52e5-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="a52e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a52e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a52e5-103">Возвращает объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="a52e5-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a52e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a52e5-104">SYNTAX</span></span>

### <span data-ttu-id="a52e5-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="a52e5-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a52e5-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a52e5-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a52e5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a52e5-107">DESCRIPTION</span></span>
<span data-ttu-id="a52e5-108">Получает объект кластера для оборганизации по имени или по группе ресурсов или по подписке.</span><span class="sxs-lookup"><span data-stu-id="a52e5-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="a52e5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a52e5-109">EXAMPLES</span></span>

### <span data-ttu-id="a52e5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a52e5-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="a52e5-111">Получает определенный кластер выопераций по имени.</span><span class="sxs-lookup"><span data-stu-id="a52e5-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="a52e5-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a52e5-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="a52e5-113">Получает все кластеры выопераций в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a52e5-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="a52e5-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a52e5-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="a52e5-115">Получает все кластеры выопераций в подписке.</span><span class="sxs-lookup"><span data-stu-id="a52e5-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="a52e5-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a52e5-116">PARAMETERS</span></span>

### <span data-ttu-id="a52e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52e5-117">-DefaultProfile</span></span>
<span data-ttu-id="a52e5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a52e5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a52e5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a52e5-119">-Name</span></span>
<span data-ttu-id="a52e5-120">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="a52e5-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="a52e5-122">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="a52e5-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52e5-123">CommonParameters</span></span>
<span data-ttu-id="a52e5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a52e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52e5-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52e5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52e5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a52e5-126">INPUTS</span></span>

### <span data-ttu-id="a52e5-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="a52e5-127">None</span></span>

## <span data-ttu-id="a52e5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a52e5-128">OUTPUTS</span></span>

### <span data-ttu-id="a52e5-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="a52e5-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="a52e5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a52e5-130">NOTES</span></span>

## <span data-ttu-id="a52e5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a52e5-131">RELATED LINKS</span></span>
