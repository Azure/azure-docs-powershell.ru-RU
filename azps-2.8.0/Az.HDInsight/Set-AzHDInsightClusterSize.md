---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 1616714879a260dea3611809b5f7028b4a203d34
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720798"
---
# <span data-ttu-id="334c1-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="334c1-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="334c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="334c1-102">SYNOPSIS</span></span>
<span data-ttu-id="334c1-103">Задает количество рабочих узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="334c1-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="334c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="334c1-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="334c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="334c1-105">DESCRIPTION</span></span>
<span data-ttu-id="334c1-106">Командлет **Set-AzHDInsightClusterSize** задает количество узлов рабочих процессов в указанном кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="334c1-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="334c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="334c1-107">EXAMPLES</span></span>

### <span data-ttu-id="334c1-108">Пример 1: Установка размера указанного кластера</span><span class="sxs-lookup"><span data-stu-id="334c1-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="334c1-109">Эта команда задает размер кластера с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="334c1-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="334c1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="334c1-110">PARAMETERS</span></span>

### <span data-ttu-id="334c1-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="334c1-111">-ClusterName</span></span>
<span data-ttu-id="334c1-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="334c1-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="334c1-113">-DefaultProfile</span></span>
<span data-ttu-id="334c1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="334c1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="334c1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="334c1-115">-ResourceGroupName</span></span>
<span data-ttu-id="334c1-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="334c1-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334c1-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="334c1-117">-TargetInstanceCount</span></span>
<span data-ttu-id="334c1-118">Указывает нужное количество рабочих узлов в кластере.</span><span class="sxs-lookup"><span data-stu-id="334c1-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334c1-119">CommonParameters</span></span>
<span data-ttu-id="334c1-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="334c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334c1-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="334c1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334c1-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="334c1-122">INPUTS</span></span>

### <span data-ttu-id="334c1-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="334c1-123">None</span></span>

## <span data-ttu-id="334c1-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="334c1-124">OUTPUTS</span></span>

### <span data-ttu-id="334c1-125">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="334c1-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="334c1-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="334c1-126">NOTES</span></span>

## <span data-ttu-id="334c1-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="334c1-127">RELATED LINKS</span></span>
