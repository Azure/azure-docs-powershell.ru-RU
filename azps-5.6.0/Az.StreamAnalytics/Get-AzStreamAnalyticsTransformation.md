---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 0c009ed05b475e466ab0b2c0dd7c6f18e70c2f9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973843"
---
# <span data-ttu-id="8a7ed-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="8a7ed-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="8a7ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a7ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8a7ed-103">Получает сведения о преобразовании задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="8a7ed-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="8a7ed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8a7ed-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a7ed-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a7ed-105">DESCRIPTION</span></span>
<span data-ttu-id="8a7ed-106">Для получения сведений о преобразовании, определенном в задание Stream Analytics, возвращается cmdlet **Get-AzStreamAnalyticsTransformation.**</span><span class="sxs-lookup"><span data-stu-id="8a7ed-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="8a7ed-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8a7ed-107">EXAMPLES</span></span>

### <span data-ttu-id="8a7ed-108">ПРИМЕР 1. Просмотр сведений о преобразовании средства аналитики Stream</span><span class="sxs-lookup"><span data-stu-id="8a7ed-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="8a7ed-109">Эта команда возвращает сведения о преобразовании, называемом StreamingJob в задание StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="8a7ed-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="8a7ed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a7ed-110">PARAMETERS</span></span>

### <span data-ttu-id="8a7ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a7ed-111">-DefaultProfile</span></span>
<span data-ttu-id="8a7ed-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7ed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a7ed-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="8a7ed-113">-JobName</span></span>
<span data-ttu-id="8a7ed-114">Указывает имя задания Azure Stream Analytics, к которому принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="8a7ed-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="8a7ed-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8a7ed-115">-Name</span></span>
<span data-ttu-id="8a7ed-116">Указывает имя преобразования службы Azure Stream Analytics, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="8a7ed-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="8a7ed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a7ed-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a7ed-118">Имя группы ресурсов, к которой относится преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="8a7ed-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="8a7ed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a7ed-119">CommonParameters</span></span>
<span data-ttu-id="8a7ed-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a7ed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a7ed-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a7ed-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a7ed-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a7ed-122">INPUTS</span></span>

### <span data-ttu-id="8a7ed-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8a7ed-123">System.String</span></span>

## <span data-ttu-id="8a7ed-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a7ed-124">OUTPUTS</span></span>

### <span data-ttu-id="8a7ed-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="8a7ed-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="8a7ed-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8a7ed-126">NOTES</span></span>

## <span data-ttu-id="8a7ed-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a7ed-127">RELATED LINKS</span></span>

[<span data-ttu-id="8a7ed-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="8a7ed-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


