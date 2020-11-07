---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912990"
---
# <span data-ttu-id="209e1-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="209e1-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="209e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="209e1-102">SYNOPSIS</span></span>
<span data-ttu-id="209e1-103">Удаляет указанный кластер HDInsight из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="209e1-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="209e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="209e1-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="209e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="209e1-105">DESCRIPTION</span></span>
<span data-ttu-id="209e1-106">Командлет **Remove-AzHDInsightCluster** удаляет указанный кластер служб HDInsight из подписки.</span><span class="sxs-lookup"><span data-stu-id="209e1-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="209e1-107">Эта операция также удаляет все данные, хранящиеся в распределенной файловой системе Hadoop (HDFS) в кластере.</span><span class="sxs-lookup"><span data-stu-id="209e1-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="209e1-108">Данные, хранящиеся в связанной учетной записи хранилища Azure, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="209e1-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="209e1-109">Данные, хранящиеся в внешних metastores, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="209e1-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="209e1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="209e1-110">EXAMPLES</span></span>

### <span data-ttu-id="209e1-111">Пример 1: Удаление кластера Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="209e1-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="209e1-112">Эта команда удаляет кластер с именем "-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="209e1-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="209e1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="209e1-113">PARAMETERS</span></span>

### <span data-ttu-id="209e1-114">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="209e1-114">-ClusterName</span></span>
<span data-ttu-id="209e1-115">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="209e1-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="209e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="209e1-116">-DefaultProfile</span></span>
<span data-ttu-id="209e1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="209e1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209e1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="209e1-118">-ResourceGroupName</span></span>
<span data-ttu-id="209e1-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="209e1-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="209e1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="209e1-120">-PassThru</span></span>
<span data-ttu-id="209e1-121">Если указана пропускания, выводится результат.</span><span class="sxs-lookup"><span data-stu-id="209e1-121">If PassThru is present, output the result</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="209e1-122">CommonParameters</span></span>
<span data-ttu-id="209e1-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="209e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="209e1-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="209e1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="209e1-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="209e1-125">INPUTS</span></span>

### <span data-ttu-id="209e1-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="209e1-126">None</span></span>
## <span data-ttu-id="209e1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="209e1-127">OUTPUTS</span></span>

### <span data-ttu-id="209e1-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="209e1-128">System.Boolean</span></span>
## <span data-ttu-id="209e1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="209e1-129">NOTES</span></span>

## <span data-ttu-id="209e1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="209e1-130">RELATED LINKS</span></span>

[<span data-ttu-id="209e1-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="209e1-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="209e1-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="209e1-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


