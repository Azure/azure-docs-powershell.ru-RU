---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: 198f0db3cab8b2e0f6e8f9b466ac3e0027e4638c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564487"
---
# <span data-ttu-id="bac4f-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="bac4f-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="bac4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bac4f-102">SYNOPSIS</span></span>
<span data-ttu-id="bac4f-103">Получение свойств службы HDInsight, например доступных местоположений и емкости.</span><span class="sxs-lookup"><span data-stu-id="bac4f-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bac4f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bac4f-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bac4f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bac4f-105">DESCRIPTION</span></span>
<span data-ttu-id="bac4f-106">Командлет **Get-AzureRmHDInsightProperties** получает свойства, специфические для Azure HDInsight, например список доступных местоположений, версий кластера HDInsight и доступной вычислительной мощности.</span><span class="sxs-lookup"><span data-stu-id="bac4f-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="bac4f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bac4f-107">EXAMPLES</span></span>

### <span data-ttu-id="bac4f-108">Пример 1: получение свойств кластера HDInsight для Azure</span><span class="sxs-lookup"><span data-stu-id="bac4f-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="bac4f-109">Эта команда получает свойства из службы HDInsight из расположения "Восток США 2.</span><span class="sxs-lookup"><span data-stu-id="bac4f-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="bac4f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bac4f-110">PARAMETERS</span></span>

### <span data-ttu-id="bac4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac4f-111">-DefaultProfile</span></span>
<span data-ttu-id="bac4f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bac4f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bac4f-113">-Location</span><span class="sxs-lookup"><span data-stu-id="bac4f-113">-Location</span></span>
<span data-ttu-id="bac4f-114">Указывает расположение, для которого требуется получить свойства HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bac4f-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="bac4f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac4f-115">CommonParameters</span></span>
<span data-ttu-id="bac4f-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bac4f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac4f-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac4f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac4f-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bac4f-118">INPUTS</span></span>

### <span data-ttu-id="bac4f-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="bac4f-119">None</span></span>

## <span data-ttu-id="bac4f-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bac4f-120">OUTPUTS</span></span>

### <span data-ttu-id="bac4f-121">Microsoft. Azure. Management. HDInsight. Models. CapabilitiesResponse</span><span class="sxs-lookup"><span data-stu-id="bac4f-121">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="bac4f-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="bac4f-122">NOTES</span></span>

## <span data-ttu-id="bac4f-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bac4f-123">RELATED LINKS</span></span>
