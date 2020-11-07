---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 9c92156f3fe739cd4f4285d536bd8a4c79cd3ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732826"
---
# <span data-ttu-id="ed6e9-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="ed6e9-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="ed6e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6e9-103">Получает сведения о преобразовании задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed6e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed6e9-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed6e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed6e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed6e9-106">Командлет **Get-AzureRmStreamAnalyticsTransformation** получает сведения о преобразовании, определенном в задании Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="ed6e9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed6e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ed6e9-108">Пример 1: получение сведений об преобразовании Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="ed6e9-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="ed6e9-109">Эта команда возвращает сведения о преобразовании с именем StreamingJob для задания с именем StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="ed6e9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed6e9-110">PARAMETERS</span></span>

### <span data-ttu-id="ed6e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6e9-111">-DefaultProfile</span></span>
<span data-ttu-id="ed6e9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed6e9-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="ed6e9-113">-JobName</span></span>
<span data-ttu-id="ed6e9-114">Указывает имя задания Azure Stream Analytics, которому принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6e9-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed6e9-115">-Name</span></span>
<span data-ttu-id="ed6e9-116">Указывает имя извлекаемого преобразования Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6e9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed6e9-117">-ResourceGroupName</span></span>
<span data-ttu-id="ed6e9-118">Указывает имя группы ресурсов, которой принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6e9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6e9-119">CommonParameters</span></span>
<span data-ttu-id="ed6e9-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6e9-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed6e9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6e9-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed6e9-122">INPUTS</span></span>

### <span data-ttu-id="ed6e9-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="ed6e9-123">None</span></span>
<span data-ttu-id="ed6e9-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed6e9-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed6e9-125">OUTPUTS</span></span>

### <span data-ttu-id="ed6e9-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="ed6e9-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="ed6e9-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed6e9-127">NOTES</span></span>

## <span data-ttu-id="ed6e9-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed6e9-128">RELATED LINKS</span></span>

[<span data-ttu-id="ed6e9-129">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="ed6e9-129">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


