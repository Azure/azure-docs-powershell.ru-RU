---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396607"
---
# <span data-ttu-id="94443-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="94443-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="94443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94443-102">SYNOPSIS</span></span>
<span data-ttu-id="94443-103">Свойства службы HDInsight, например доступные расположения и емкость.</span><span class="sxs-lookup"><span data-stu-id="94443-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="94443-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94443-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94443-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94443-105">DESCRIPTION</span></span>
<span data-ttu-id="94443-106">Для **этого** можно получить свойства для Azure HDInsight, такие как список доступных мест, версии кластера HDInsight и доступные вычислительные мощности.</span><span class="sxs-lookup"><span data-stu-id="94443-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="94443-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94443-107">EXAMPLES</span></span>

### <span data-ttu-id="94443-108">Пример 1. Свойства кластера Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="94443-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="94443-109">Эта команда получает свойства из службы HDInsight из расположения восточной части США 2.</span><span class="sxs-lookup"><span data-stu-id="94443-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="94443-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94443-110">PARAMETERS</span></span>

### <span data-ttu-id="94443-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94443-111">-DefaultProfile</span></span>
<span data-ttu-id="94443-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94443-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94443-113">-Location</span><span class="sxs-lookup"><span data-stu-id="94443-113">-Location</span></span>
<span data-ttu-id="94443-114">Определяет место, для которого извлекаются свойства HDInsight.</span><span class="sxs-lookup"><span data-stu-id="94443-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="94443-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94443-115">CommonParameters</span></span>
<span data-ttu-id="94443-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94443-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94443-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94443-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94443-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94443-118">INPUTS</span></span>

### <span data-ttu-id="94443-119">Нет</span><span class="sxs-lookup"><span data-stu-id="94443-119">None</span></span>
## <span data-ttu-id="94443-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94443-120">OUTPUTS</span></span>

### <span data-ttu-id="94443-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="94443-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="94443-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94443-122">NOTES</span></span>

## <span data-ttu-id="94443-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94443-123">RELATED LINKS</span></span>
