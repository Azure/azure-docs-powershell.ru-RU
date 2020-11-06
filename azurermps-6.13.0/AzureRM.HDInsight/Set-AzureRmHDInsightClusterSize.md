---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: 01dfcbbc9a8996ff351ecc9d88c688c96be345d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568548"
---
# <span data-ttu-id="836d5-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="836d5-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="836d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="836d5-102">SYNOPSIS</span></span>
<span data-ttu-id="836d5-103">Задает количество рабочих узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="836d5-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="836d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="836d5-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="836d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="836d5-105">DESCRIPTION</span></span>
<span data-ttu-id="836d5-106">Командлет **Set-AzureRmHDInsightClusterSize** задает количество узлов рабочих процессов в указанном кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="836d5-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="836d5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="836d5-107">EXAMPLES</span></span>

### <span data-ttu-id="836d5-108">Пример 1: Установка размера указанного кластера</span><span class="sxs-lookup"><span data-stu-id="836d5-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="836d5-109">Эта команда задает размер кластера с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="836d5-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="836d5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="836d5-110">PARAMETERS</span></span>

### <span data-ttu-id="836d5-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="836d5-111">-ClusterName</span></span>
<span data-ttu-id="836d5-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="836d5-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="836d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="836d5-113">-DefaultProfile</span></span>
<span data-ttu-id="836d5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="836d5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="836d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="836d5-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="836d5-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="836d5-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="836d5-117">-TargetInstanceCount</span></span>
<span data-ttu-id="836d5-118">Указывает нужное количество рабочих узлов в кластере.</span><span class="sxs-lookup"><span data-stu-id="836d5-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="836d5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836d5-119">CommonParameters</span></span>
<span data-ttu-id="836d5-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="836d5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836d5-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="836d5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836d5-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="836d5-122">INPUTS</span></span>

### <span data-ttu-id="836d5-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="836d5-123">None</span></span>

## <span data-ttu-id="836d5-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="836d5-124">OUTPUTS</span></span>

### <span data-ttu-id="836d5-125">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="836d5-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="836d5-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="836d5-126">NOTES</span></span>

## <span data-ttu-id="836d5-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="836d5-127">RELATED LINKS</span></span>
