---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
ms.openlocfilehash: 24400b7a2c882cef81d818c5f5b94fca4235ec83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899781"
---
# <span data-ttu-id="189cb-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="189cb-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="189cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="189cb-102">SYNOPSIS</span></span>
<span data-ttu-id="189cb-103">Возвращает объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="189cb-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="189cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="189cb-104">SYNTAX</span></span>

### <span data-ttu-id="189cb-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="189cb-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="189cb-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="189cb-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="189cb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="189cb-107">DESCRIPTION</span></span>
<span data-ttu-id="189cb-108">Получает объект кластера для оборганизации по имени или по группе ресурсов или по подписке.</span><span class="sxs-lookup"><span data-stu-id="189cb-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="189cb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="189cb-109">EXAMPLES</span></span>

### <span data-ttu-id="189cb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="189cb-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="189cb-111">Получает определенный кластер выопераций по имени.</span><span class="sxs-lookup"><span data-stu-id="189cb-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="189cb-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="189cb-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="189cb-113">Получает все кластеры выопераций в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="189cb-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="189cb-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="189cb-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="189cb-115">Получает все кластеры выопераций в подписке.</span><span class="sxs-lookup"><span data-stu-id="189cb-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="189cb-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="189cb-116">PARAMETERS</span></span>

### <span data-ttu-id="189cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189cb-117">-DefaultProfile</span></span>
<span data-ttu-id="189cb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="189cb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="189cb-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="189cb-119">-Name</span></span>
<span data-ttu-id="189cb-120">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="189cb-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="189cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="189cb-122">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="189cb-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="189cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189cb-123">CommonParameters</span></span>
<span data-ttu-id="189cb-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="189cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189cb-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="189cb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189cb-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="189cb-126">INPUTS</span></span>

### <span data-ttu-id="189cb-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="189cb-127">None</span></span>

## <span data-ttu-id="189cb-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="189cb-128">OUTPUTS</span></span>

### <span data-ttu-id="189cb-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="189cb-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="189cb-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="189cb-130">NOTES</span></span>

## <span data-ttu-id="189cb-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="189cb-131">RELATED LINKS</span></span>
