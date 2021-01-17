---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328359"
---
# <span data-ttu-id="76406-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="76406-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="76406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76406-102">SYNOPSIS</span></span>
<span data-ttu-id="76406-103">Удаляет указанный кластер HDInsight из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="76406-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="76406-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76406-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76406-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76406-105">DESCRIPTION</span></span>
<span data-ttu-id="76406-106">Для удаления указанного кластера службы HDInsight из подписки удаляется cmdlet **Remove-AzHDInsightCluster.**</span><span class="sxs-lookup"><span data-stu-id="76406-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="76406-107">В ходе этой операции также удаляются все данные, хранимые в распределенной файловой системе Hadoop (HDFS) на кластере.</span><span class="sxs-lookup"><span data-stu-id="76406-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="76406-108">Данные, хранимые в связанной учетной записи хранилища Azure, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="76406-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="76406-109">Данные, хранимые во внешних метамагагах, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="76406-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="76406-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76406-110">EXAMPLES</span></span>

### <span data-ttu-id="76406-111">Пример 1. Удаление кластера Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="76406-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="76406-112">Эта команда удаляет кластер под названием "ваш-hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="76406-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="76406-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76406-113">PARAMETERS</span></span>

### <span data-ttu-id="76406-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="76406-114">-ClusterName</span></span>
<span data-ttu-id="76406-115">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="76406-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="76406-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76406-116">-DefaultProfile</span></span>
<span data-ttu-id="76406-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="76406-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76406-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76406-118">-ResourceGroupName</span></span>
<span data-ttu-id="76406-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76406-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="76406-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76406-120">-PassThru</span></span>
<span data-ttu-id="76406-121">Если в данный момент имеется passThru, выведет результат</span><span class="sxs-lookup"><span data-stu-id="76406-121">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="76406-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76406-122">CommonParameters</span></span>
<span data-ttu-id="76406-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76406-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76406-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76406-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76406-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76406-125">INPUTS</span></span>

### <span data-ttu-id="76406-126">Нет</span><span class="sxs-lookup"><span data-stu-id="76406-126">None</span></span>
## <span data-ttu-id="76406-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76406-127">OUTPUTS</span></span>

### <span data-ttu-id="76406-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76406-128">System.Boolean</span></span>
## <span data-ttu-id="76406-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76406-129">NOTES</span></span>

## <span data-ttu-id="76406-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76406-130">RELATED LINKS</span></span>

[<span data-ttu-id="76406-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="76406-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="76406-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="76406-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


