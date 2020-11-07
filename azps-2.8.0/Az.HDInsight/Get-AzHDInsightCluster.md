---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 8b15a93ee576af683cb2ebfffa621937a2ebba78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720840"
---
# <span data-ttu-id="83863-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="83863-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="83863-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83863-102">SYNOPSIS</span></span>
<span data-ttu-id="83863-103">Возвращает и перечисляет все кластеры HDInsight Azure, связанные с текущей подпиской или указанной группой ресурсов, или извлекает определенный кластер.</span><span class="sxs-lookup"><span data-stu-id="83863-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="83863-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83863-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83863-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83863-105">DESCRIPTION</span></span>
<span data-ttu-id="83863-106">Командлет **Get-AzHDInsightCluster** включает в себя кластеры служб Azure HDInsight для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="83863-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="83863-107">Используйте параметр *имя_кластера* для получения подробных сведений о конкретном кластере.</span><span class="sxs-lookup"><span data-stu-id="83863-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="83863-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83863-108">EXAMPLES</span></span>

### <span data-ttu-id="83863-109">Пример 1: список всех кластеров Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="83863-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="83863-110">Эта команда выводит список всех кластеров Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="83863-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="83863-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83863-111">PARAMETERS</span></span>

### <span data-ttu-id="83863-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="83863-112">-ClusterName</span></span>
<span data-ttu-id="83863-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="83863-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="83863-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83863-114">-DefaultProfile</span></span>
<span data-ttu-id="83863-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="83863-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83863-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83863-116">-ResourceGroupName</span></span>
<span data-ttu-id="83863-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83863-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="83863-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83863-118">CommonParameters</span></span>
<span data-ttu-id="83863-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83863-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83863-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83863-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83863-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83863-121">INPUTS</span></span>

### <span data-ttu-id="83863-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="83863-122">None</span></span>

## <span data-ttu-id="83863-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83863-123">OUTPUTS</span></span>

### <span data-ttu-id="83863-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="83863-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="83863-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="83863-125">NOTES</span></span>

## <span data-ttu-id="83863-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83863-126">RELATED LINKS</span></span>

[<span data-ttu-id="83863-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="83863-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="83863-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="83863-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


