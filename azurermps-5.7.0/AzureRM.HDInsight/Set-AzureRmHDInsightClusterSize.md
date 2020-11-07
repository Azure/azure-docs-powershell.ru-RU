---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: eda9032cde317f418132e28917f7543d60ea0bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733279"
---
# <span data-ttu-id="8a448-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="8a448-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="8a448-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a448-102">SYNOPSIS</span></span>
<span data-ttu-id="8a448-103">Задает количество рабочих узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="8a448-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a448-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a448-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a448-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a448-105">DESCRIPTION</span></span>
<span data-ttu-id="8a448-106">Командлет **Set-AzureRmHDInsightClusterSize** задает количество узлов рабочих процессов в указанном кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8a448-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="8a448-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a448-107">EXAMPLES</span></span>

### <span data-ttu-id="8a448-108">Пример 1: Установка размера указанного кластера</span><span class="sxs-lookup"><span data-stu-id="8a448-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="8a448-109">Эта команда задает размер кластера с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="8a448-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="8a448-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a448-110">PARAMETERS</span></span>

### <span data-ttu-id="8a448-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="8a448-111">-ClusterName</span></span>
<span data-ttu-id="8a448-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="8a448-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a448-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a448-113">-DefaultProfile</span></span>
<span data-ttu-id="8a448-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8a448-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a448-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a448-115">-ResourceGroupName</span></span>
<span data-ttu-id="8a448-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a448-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8a448-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="8a448-117">-TargetInstanceCount</span></span>
<span data-ttu-id="8a448-118">Указывает нужное количество рабочих узлов в кластере.</span><span class="sxs-lookup"><span data-stu-id="8a448-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a448-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a448-119">CommonParameters</span></span>
<span data-ttu-id="8a448-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a448-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a448-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a448-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a448-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a448-122">INPUTS</span></span>

### <span data-ttu-id="8a448-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="8a448-123">None</span></span>
<span data-ttu-id="8a448-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8a448-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a448-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a448-125">OUTPUTS</span></span>

### <span data-ttu-id="8a448-126">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="8a448-126">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="8a448-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a448-127">NOTES</span></span>

## <span data-ttu-id="8a448-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a448-128">RELATED LINKS</span></span>

