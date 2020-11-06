---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: 81f25eeb8d0e6b704c4ee6ef71cd2aebcf3624ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566720"
---
# <span data-ttu-id="c1b03-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c1b03-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="c1b03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1b03-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b03-103">Возвращает и перечисляет все кластеры HDInsight Azure, связанные с текущей подпиской или указанной группой ресурсов, или извлекает определенный кластер.</span><span class="sxs-lookup"><span data-stu-id="c1b03-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1b03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1b03-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1b03-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b03-106">Командлет **Get-AzureRmHDInsightCluster** включает в себя кластеры служб Azure HDInsight для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="c1b03-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="c1b03-107">Используйте параметр *имя_кластера* для получения подробных сведений о конкретном кластере.</span><span class="sxs-lookup"><span data-stu-id="c1b03-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="c1b03-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1b03-108">EXAMPLES</span></span>

### <span data-ttu-id="c1b03-109">Пример 1: список всех кластеров Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1b03-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="c1b03-110">Эта команда выводит список всех кластеров Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c1b03-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="c1b03-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1b03-111">PARAMETERS</span></span>

### <span data-ttu-id="c1b03-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="c1b03-112">-ClusterName</span></span>
<span data-ttu-id="c1b03-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="c1b03-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c1b03-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b03-114">-ResourceGroupName</span></span>
<span data-ttu-id="c1b03-115">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c1b03-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c1b03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b03-116">-DefaultProfile</span></span>
<span data-ttu-id="c1b03-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b03-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1b03-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b03-118">CommonParameters</span></span>
<span data-ttu-id="c1b03-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1b03-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b03-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b03-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b03-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1b03-121">INPUTS</span></span>

## <span data-ttu-id="c1b03-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1b03-122">OUTPUTS</span></span>

### <span data-ttu-id="c1b03-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. AzureHDInsightCluster]</span><span class="sxs-lookup"><span data-stu-id="c1b03-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster]</span></span>

## <span data-ttu-id="c1b03-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1b03-124">NOTES</span></span>

## <span data-ttu-id="c1b03-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1b03-125">RELATED LINKS</span></span>

[<span data-ttu-id="c1b03-126">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c1b03-126">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="c1b03-127">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c1b03-127">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


