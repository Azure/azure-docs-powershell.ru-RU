---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077489"
---
# <span data-ttu-id="f9561-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="f9561-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="f9561-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9561-102">SYNOPSIS</span></span>
<span data-ttu-id="f9561-103">Получает сведения о преобразовании задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="f9561-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="f9561-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9561-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9561-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9561-105">DESCRIPTION</span></span>
<span data-ttu-id="f9561-106">Командлет **Get-AzStreamAnalyticsTransformation** получает сведения о преобразовании, определенном в задании Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="f9561-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="f9561-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9561-107">EXAMPLES</span></span>

### <span data-ttu-id="f9561-108">Пример 1: получение сведений об преобразовании Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="f9561-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="f9561-109">Эта команда возвращает сведения о преобразовании с именем StreamingJob для задания с именем StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="f9561-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="f9561-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9561-110">PARAMETERS</span></span>

### <span data-ttu-id="f9561-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9561-111">-DefaultProfile</span></span>
<span data-ttu-id="f9561-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9561-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9561-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="f9561-113">-JobName</span></span>
<span data-ttu-id="f9561-114">Указывает имя задания Azure Stream Analytics, которому принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="f9561-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="f9561-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9561-115">-Name</span></span>
<span data-ttu-id="f9561-116">Указывает имя извлекаемого преобразования Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="f9561-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="f9561-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9561-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9561-118">Указывает имя группы ресурсов, которой принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="f9561-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="f9561-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9561-119">CommonParameters</span></span>
<span data-ttu-id="f9561-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9561-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9561-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9561-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9561-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9561-122">INPUTS</span></span>

### <span data-ttu-id="f9561-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f9561-123">System.String</span></span>

## <span data-ttu-id="f9561-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9561-124">OUTPUTS</span></span>

### <span data-ttu-id="f9561-125">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="f9561-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="f9561-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9561-126">NOTES</span></span>

## <span data-ttu-id="f9561-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9561-127">RELATED LINKS</span></span>

[<span data-ttu-id="f9561-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="f9561-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)

