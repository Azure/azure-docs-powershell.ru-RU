---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: f232d1df7bef3800fc54b2469a51f3f69c8d4fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564496"
---
# <span data-ttu-id="3061a-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3061a-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="3061a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3061a-102">SYNOPSIS</span></span>
<span data-ttu-id="3061a-103">Возвращает и перечисляет все кластеры HDInsight Azure, связанные с текущей подпиской или указанной группой ресурсов, или извлекает определенный кластер.</span><span class="sxs-lookup"><span data-stu-id="3061a-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3061a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3061a-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3061a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3061a-105">DESCRIPTION</span></span>
<span data-ttu-id="3061a-106">Командлет **Get-AzureRmHDInsightCluster** включает в себя кластеры служб Azure HDInsight для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="3061a-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="3061a-107">Используйте параметр *имя_кластера* для получения подробных сведений о конкретном кластере.</span><span class="sxs-lookup"><span data-stu-id="3061a-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="3061a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3061a-108">EXAMPLES</span></span>

### <span data-ttu-id="3061a-109">Пример 1: список всех кластеров Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="3061a-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="3061a-110">Эта команда выводит список всех кластеров Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3061a-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="3061a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3061a-111">PARAMETERS</span></span>

### <span data-ttu-id="3061a-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="3061a-112">-ClusterName</span></span>
<span data-ttu-id="3061a-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="3061a-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3061a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3061a-114">-DefaultProfile</span></span>
<span data-ttu-id="3061a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3061a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3061a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3061a-116">-ResourceGroupName</span></span>
<span data-ttu-id="3061a-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3061a-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3061a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3061a-118">CommonParameters</span></span>
<span data-ttu-id="3061a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3061a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3061a-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3061a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3061a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3061a-121">INPUTS</span></span>

### <span data-ttu-id="3061a-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="3061a-122">None</span></span>

## <span data-ttu-id="3061a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3061a-123">OUTPUTS</span></span>

### <span data-ttu-id="3061a-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3061a-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="3061a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="3061a-125">NOTES</span></span>

## <span data-ttu-id="3061a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3061a-126">RELATED LINKS</span></span>

[<span data-ttu-id="3061a-127">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3061a-127">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="3061a-128">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3061a-128">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


