---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326748"
---
# <span data-ttu-id="8e791-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8e791-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="8e791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e791-102">SYNOPSIS</span></span>
<span data-ttu-id="8e791-103">Возвращает и перечисляет все кластеры Azure HDInsight, связанные с текущей подпиской или определенной группой ресурсов, либо извлекает определенный кластер.</span><span class="sxs-lookup"><span data-stu-id="8e791-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="8e791-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e791-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e791-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e791-105">DESCRIPTION</span></span>
<span data-ttu-id="8e791-106">Для текущей подписки на Azure HDInsight перечислены кластеры службы **Get-AzHDInsightCluster.**</span><span class="sxs-lookup"><span data-stu-id="8e791-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="8e791-107">Используйте параметр *ClusterName* для получения сведений о конкретном кластере.</span><span class="sxs-lookup"><span data-stu-id="8e791-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="8e791-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e791-108">EXAMPLES</span></span>

### <span data-ttu-id="8e791-109">Пример 1. Список всех кластеров Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="8e791-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="8e791-110">Эта команда содержит список всех кластеров Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8e791-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="8e791-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e791-111">PARAMETERS</span></span>

### <span data-ttu-id="8e791-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8e791-112">-ClusterName</span></span>
<span data-ttu-id="8e791-113">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="8e791-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e791-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e791-114">-DefaultProfile</span></span>
<span data-ttu-id="8e791-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8e791-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e791-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e791-116">-ResourceGroupName</span></span>
<span data-ttu-id="8e791-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e791-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e791-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e791-118">CommonParameters</span></span>
<span data-ttu-id="8e791-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e791-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e791-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e791-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e791-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e791-121">INPUTS</span></span>

### <span data-ttu-id="8e791-122">Нет</span><span class="sxs-lookup"><span data-stu-id="8e791-122">None</span></span>

## <span data-ttu-id="8e791-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e791-123">OUTPUTS</span></span>

### <span data-ttu-id="8e791-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8e791-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="8e791-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e791-125">NOTES</span></span>

## <span data-ttu-id="8e791-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e791-126">RELATED LINKS</span></span>

[<span data-ttu-id="8e791-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8e791-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="8e791-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8e791-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


