---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: ab97162fb2651bce8e242ca0cef7b497ffcf1bef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234276"
---
# <span data-ttu-id="0e766-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0e766-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="0e766-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e766-102">SYNOPSIS</span></span>
<span data-ttu-id="0e766-103">Удаляет указанный кластер HDInsight из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="0e766-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="0e766-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0e766-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e766-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e766-105">DESCRIPTION</span></span>
<span data-ttu-id="0e766-106">При этом из **подписки** удаляется указанный кластер служб HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0e766-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="0e766-107">В ходе этой операции также удаляются все данные, хранимые в распределенной файловой системе Hadoop (HDFS) на кластере.</span><span class="sxs-lookup"><span data-stu-id="0e766-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="0e766-108">Данные, хранимые в связанной учетной записи хранилища Azure, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="0e766-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="0e766-109">Данные, хранимые во внешних метамагагах, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="0e766-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="0e766-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0e766-110">EXAMPLES</span></span>

### <span data-ttu-id="0e766-111">Пример 1. Удаление кластера Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="0e766-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="0e766-112">Эта команда удаляет кластер под названием "ваш-hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="0e766-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0e766-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e766-113">PARAMETERS</span></span>

### <span data-ttu-id="0e766-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0e766-114">-ClusterName</span></span>
<span data-ttu-id="0e766-115">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="0e766-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0e766-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e766-116">-DefaultProfile</span></span>
<span data-ttu-id="0e766-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0e766-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e766-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e766-118">-PassThru</span></span>
<span data-ttu-id="0e766-119">Если в данный момент имеется passThru, выведет результат</span><span class="sxs-lookup"><span data-stu-id="0e766-119">If PassThru is present, output the result</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e766-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e766-120">-ResourceGroupName</span></span>
<span data-ttu-id="0e766-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e766-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0e766-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e766-122">CommonParameters</span></span>
<span data-ttu-id="0e766-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e766-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e766-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e766-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e766-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e766-125">INPUTS</span></span>

### <span data-ttu-id="0e766-126">Нет</span><span class="sxs-lookup"><span data-stu-id="0e766-126">None</span></span>
## <span data-ttu-id="0e766-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e766-127">OUTPUTS</span></span>

### <span data-ttu-id="0e766-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e766-128">System.Boolean</span></span>
## <span data-ttu-id="0e766-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0e766-129">NOTES</span></span>

## <span data-ttu-id="0e766-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e766-130">RELATED LINKS</span></span>

[<span data-ttu-id="0e766-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0e766-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="0e766-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0e766-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


