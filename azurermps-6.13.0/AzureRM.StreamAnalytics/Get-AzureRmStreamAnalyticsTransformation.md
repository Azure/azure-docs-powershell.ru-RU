---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: d83038d521e562ec835324dd50740ec929fb5893
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556471"
---
# <span data-ttu-id="8e023-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="8e023-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="8e023-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e023-102">SYNOPSIS</span></span>
<span data-ttu-id="8e023-103">Получает сведения о преобразовании задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="8e023-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e023-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e023-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e023-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e023-105">DESCRIPTION</span></span>
<span data-ttu-id="8e023-106">Командлет **Get-AzureRmStreamAnalyticsTransformation** получает сведения о преобразовании, определенном в задании Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="8e023-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="8e023-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e023-107">EXAMPLES</span></span>

### <span data-ttu-id="8e023-108">Пример 1: получение сведений об преобразовании Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="8e023-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="8e023-109">Эта команда возвращает сведения о преобразовании с именем StreamingJob для задания с именем StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="8e023-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="8e023-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e023-110">PARAMETERS</span></span>

### <span data-ttu-id="8e023-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e023-111">-DefaultProfile</span></span>
<span data-ttu-id="8e023-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e023-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e023-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="8e023-113">-JobName</span></span>
<span data-ttu-id="8e023-114">Указывает имя задания Azure Stream Analytics, которому принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="8e023-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e023-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e023-115">-Name</span></span>
<span data-ttu-id="8e023-116">Указывает имя извлекаемого преобразования Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="8e023-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e023-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e023-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e023-118">Указывает имя группы ресурсов, которой принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="8e023-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e023-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e023-119">CommonParameters</span></span>
<span data-ttu-id="8e023-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e023-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e023-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e023-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e023-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e023-122">INPUTS</span></span>

### <span data-ttu-id="8e023-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8e023-123">System.String</span></span>

## <span data-ttu-id="8e023-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e023-124">OUTPUTS</span></span>

### <span data-ttu-id="8e023-125">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="8e023-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="8e023-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e023-126">NOTES</span></span>

## <span data-ttu-id="8e023-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e023-127">RELATED LINKS</span></span>

[<span data-ttu-id="8e023-128">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="8e023-128">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


