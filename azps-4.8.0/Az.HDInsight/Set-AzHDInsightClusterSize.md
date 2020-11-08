---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078252"
---
# <span data-ttu-id="106b4-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="106b4-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="106b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="106b4-102">SYNOPSIS</span></span>
<span data-ttu-id="106b4-103">Задает количество рабочих узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="106b4-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="106b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="106b4-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="106b4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="106b4-105">DESCRIPTION</span></span>
<span data-ttu-id="106b4-106">Командлет **Set-AzHDInsightClusterSize** задает количество узлов рабочих процессов в указанном кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="106b4-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="106b4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="106b4-107">EXAMPLES</span></span>

### <span data-ttu-id="106b4-108">Пример 1: Установка размера указанного кластера</span><span class="sxs-lookup"><span data-stu-id="106b4-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="106b4-109">Эта команда задает размер кластера с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="106b4-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="106b4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="106b4-110">PARAMETERS</span></span>

### <span data-ttu-id="106b4-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="106b4-111">-ClusterName</span></span>
<span data-ttu-id="106b4-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="106b4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="106b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106b4-113">-DefaultProfile</span></span>
<span data-ttu-id="106b4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="106b4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="106b4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="106b4-115">-ResourceGroupName</span></span>
<span data-ttu-id="106b4-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="106b4-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="106b4-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="106b4-117">-TargetInstanceCount</span></span>
<span data-ttu-id="106b4-118">Указывает нужное количество рабочих узлов в кластере.</span><span class="sxs-lookup"><span data-stu-id="106b4-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="106b4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106b4-119">CommonParameters</span></span>
<span data-ttu-id="106b4-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="106b4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106b4-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="106b4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106b4-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="106b4-122">INPUTS</span></span>

### <span data-ttu-id="106b4-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="106b4-123">None</span></span>

## <span data-ttu-id="106b4-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="106b4-124">OUTPUTS</span></span>

### <span data-ttu-id="106b4-125">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="106b4-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="106b4-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="106b4-126">NOTES</span></span>

## <span data-ttu-id="106b4-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="106b4-127">RELATED LINKS</span></span>
