---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567119"
---
# <span data-ttu-id="31367-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="31367-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="31367-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31367-102">SYNOPSIS</span></span>
<span data-ttu-id="31367-103">Возвращает объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="31367-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31367-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31367-104">SYNTAX</span></span>

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31367-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31367-105">DESCRIPTION</span></span>
<span data-ttu-id="31367-106">Получает объект кластера для оборганизации по имени или по группе ресурсов или по подписке.</span><span class="sxs-lookup"><span data-stu-id="31367-106">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="31367-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31367-107">EXAMPLES</span></span>

### <span data-ttu-id="31367-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31367-108">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="31367-109">Получает определенный кластер выопераций по имени.</span><span class="sxs-lookup"><span data-stu-id="31367-109">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="31367-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="31367-110">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="31367-111">Получает все кластеры выопераций в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31367-111">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="31367-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="31367-112">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="31367-113">Получает все кластеры выопераций в подписке.</span><span class="sxs-lookup"><span data-stu-id="31367-113">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="31367-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31367-114">PARAMETERS</span></span>

### <span data-ttu-id="31367-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31367-115">-DefaultProfile</span></span>
<span data-ttu-id="31367-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31367-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31367-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31367-117">-Name</span></span>
<span data-ttu-id="31367-118">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="31367-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31367-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31367-119">-ResourceGroupName</span></span>
<span data-ttu-id="31367-120">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="31367-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31367-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31367-121">CommonParameters</span></span>
<span data-ttu-id="31367-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31367-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31367-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31367-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31367-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31367-124">INPUTS</span></span>

### <span data-ttu-id="31367-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="31367-125">None</span></span>

## <span data-ttu-id="31367-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31367-126">OUTPUTS</span></span>

### <span data-ttu-id="31367-127">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="31367-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="31367-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="31367-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="31367-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="31367-129">NOTES</span></span>

## <span data-ttu-id="31367-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31367-130">RELATED LINKS</span></span>

