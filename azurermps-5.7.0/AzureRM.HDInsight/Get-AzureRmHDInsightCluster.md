---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: 76cf830e79c2374d81c57a1341ae99636333e273
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566184"
---
# <span data-ttu-id="b9b8c-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b9b8c-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="b9b8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b8c-103">Возвращает и перечисляет все кластеры HDInsight Azure, связанные с текущей подпиской или указанной группой ресурсов, или извлекает определенный кластер.</span><span class="sxs-lookup"><span data-stu-id="b9b8c-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9b8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9b8c-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9b8c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9b8c-105">DESCRIPTION</span></span>
<span data-ttu-id="b9b8c-106">Командлет **Get-AzureRmHDInsightCluster** включает в себя кластеры служб Azure HDInsight для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="b9b8c-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="b9b8c-107">Используйте параметр *имя_кластера* для получения подробных сведений о конкретном кластере.</span><span class="sxs-lookup"><span data-stu-id="b9b8c-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="b9b8c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9b8c-108">EXAMPLES</span></span>

### <span data-ttu-id="b9b8c-109">Пример 1: список всех кластеров Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="b9b8c-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="b9b8c-110">Эта команда выводит список всех кластеров Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b9b8c-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="b9b8c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9b8c-111">PARAMETERS</span></span>

### <span data-ttu-id="b9b8c-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="b9b8c-112">-ClusterName</span></span>
<span data-ttu-id="b9b8c-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b9b8c-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b8c-114">-DefaultProfile</span></span>
<span data-ttu-id="b9b8c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b9b8c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9b8c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b8c-116">-ResourceGroupName</span></span>
<span data-ttu-id="b9b8c-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9b8c-117">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b8c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b8c-118">CommonParameters</span></span>
<span data-ttu-id="b9b8c-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9b8c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b8c-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9b8c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b8c-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9b8c-121">INPUTS</span></span>

### <span data-ttu-id="b9b8c-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="b9b8c-122">None</span></span>
<span data-ttu-id="b9b8c-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b9b8c-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9b8c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9b8c-124">OUTPUTS</span></span>

### <span data-ttu-id="b9b8c-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. AzureHDInsightCluster]</span><span class="sxs-lookup"><span data-stu-id="b9b8c-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster]</span></span>

## <span data-ttu-id="b9b8c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9b8c-126">NOTES</span></span>

## <span data-ttu-id="b9b8c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9b8c-127">RELATED LINKS</span></span>

[<span data-ttu-id="b9b8c-128">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b9b8c-128">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="b9b8c-129">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b9b8c-129">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


