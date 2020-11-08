---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078254"
---
# <span data-ttu-id="f1e7c-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="f1e7c-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="f1e7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e7c-103">Получение свойств службы HDInsight, например доступных местоположений и емкости.</span><span class="sxs-lookup"><span data-stu-id="f1e7c-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="f1e7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1e7c-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1e7c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e7c-106">Командлет **Get-AzHDInsightProperty** получает свойства, специфические для Azure HDInsight, например список доступных местоположений, версий кластера HDInsight и доступной вычислительной мощности.</span><span class="sxs-lookup"><span data-stu-id="f1e7c-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="f1e7c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1e7c-107">EXAMPLES</span></span>

### <span data-ttu-id="f1e7c-108">Пример 1: получение свойств кластера HDInsight для Azure</span><span class="sxs-lookup"><span data-stu-id="f1e7c-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="f1e7c-109">Эта команда получает свойства из службы HDInsight из расположения "Восток США 2.</span><span class="sxs-lookup"><span data-stu-id="f1e7c-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="f1e7c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1e7c-110">PARAMETERS</span></span>

### <span data-ttu-id="f1e7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e7c-111">-DefaultProfile</span></span>
<span data-ttu-id="f1e7c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f1e7c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1e7c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f1e7c-113">-Location</span></span>
<span data-ttu-id="f1e7c-114">Указывает расположение, для которого требуется получить свойства HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f1e7c-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="f1e7c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e7c-115">CommonParameters</span></span>
<span data-ttu-id="f1e7c-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1e7c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e7c-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1e7c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e7c-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1e7c-118">INPUTS</span></span>

### <span data-ttu-id="f1e7c-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="f1e7c-119">None</span></span>
## <span data-ttu-id="f1e7c-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1e7c-120">OUTPUTS</span></span>

### <span data-ttu-id="f1e7c-121">Microsoft. Azure. Management. HDInsight. Models. AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="f1e7c-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="f1e7c-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1e7c-122">NOTES</span></span>

## <span data-ttu-id="f1e7c-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1e7c-123">RELATED LINKS</span></span>