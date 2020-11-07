---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: 1029871a2125668c732f7ff541582f06dbd790c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733055"
---
# <span data-ttu-id="35a7a-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="35a7a-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="35a7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="35a7a-103">Удаляет указанный кластер HDInsight из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="35a7a-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35a7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35a7a-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35a7a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35a7a-105">DESCRIPTION</span></span>
<span data-ttu-id="35a7a-106">Командлет **Remove-AzureRmHDInsightCluster** удаляет указанный кластер служб HDInsight из подписки.</span><span class="sxs-lookup"><span data-stu-id="35a7a-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="35a7a-107">Эта операция также удаляет все данные, хранящиеся в распределенной файловой системе Hadoop (HDFS) в кластере.</span><span class="sxs-lookup"><span data-stu-id="35a7a-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="35a7a-108">Данные, хранящиеся в связанной учетной записи хранилища Azure, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="35a7a-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="35a7a-109">Данные, хранящиеся в внешних metastores, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="35a7a-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="35a7a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35a7a-110">EXAMPLES</span></span>

### <span data-ttu-id="35a7a-111">Пример 1: Удаление кластера Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="35a7a-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="35a7a-112">Эта команда удаляет кластер с именем "-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="35a7a-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="35a7a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35a7a-113">PARAMETERS</span></span>

### <span data-ttu-id="35a7a-114">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="35a7a-114">-ClusterName</span></span>
<span data-ttu-id="35a7a-115">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="35a7a-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="35a7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a7a-116">-DefaultProfile</span></span>
<span data-ttu-id="35a7a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="35a7a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35a7a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a7a-118">-ResourceGroupName</span></span>
<span data-ttu-id="35a7a-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35a7a-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="35a7a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a7a-120">CommonParameters</span></span>
<span data-ttu-id="35a7a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35a7a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a7a-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a7a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a7a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35a7a-123">INPUTS</span></span>

### <span data-ttu-id="35a7a-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="35a7a-124">None</span></span>
<span data-ttu-id="35a7a-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="35a7a-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35a7a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35a7a-126">OUTPUTS</span></span>

### <span data-ttu-id="35a7a-127">Microsoft. Azure. Management. HDInsight. Models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="35a7a-127">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="35a7a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="35a7a-128">NOTES</span></span>

## <span data-ttu-id="35a7a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35a7a-129">RELATED LINKS</span></span>

[<span data-ttu-id="35a7a-130">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="35a7a-130">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="35a7a-131">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="35a7a-131">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


