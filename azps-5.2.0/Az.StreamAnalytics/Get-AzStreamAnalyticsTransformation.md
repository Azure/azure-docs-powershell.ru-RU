---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414439"
---
# <span data-ttu-id="e0ae0-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="e0ae0-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="e0ae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ae0-103">Получает сведения о преобразовании задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="e0ae0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0ae0-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0ae0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0ae0-105">DESCRIPTION</span></span>
<span data-ttu-id="e0ae0-106">Для получения сведений о преобразовании, определенном в задание Stream Analytics, возвращается cmdlet **Get-AzStreamAnalyticsTransformation.**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="e0ae0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0ae0-107">EXAMPLES</span></span>

### <span data-ttu-id="e0ae0-108">ПРИМЕР 1. Просмотр сведений о преобразовании в Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="e0ae0-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="e0ae0-109">Эта команда возвращает сведения о преобразовании, называемом StreamingJob в задаче StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="e0ae0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0ae0-110">PARAMETERS</span></span>

### <span data-ttu-id="e0ae0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ae0-111">-DefaultProfile</span></span>
<span data-ttu-id="e0ae0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0ae0-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="e0ae0-113">-JobName</span></span>
<span data-ttu-id="e0ae0-114">Указывает имя задания Azure Stream Analytics, к которому принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="e0ae0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e0ae0-115">-Name</span></span>
<span data-ttu-id="e0ae0-116">Указывает имя преобразования службы Azure Stream Analytics, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="e0ae0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ae0-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0ae0-118">Имя группы ресурсов, к которой принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="e0ae0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ae0-119">CommonParameters</span></span>
<span data-ttu-id="e0ae0-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ae0-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ae0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ae0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0ae0-122">INPUTS</span></span>

### <span data-ttu-id="e0ae0-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e0ae0-123">System.String</span></span>

## <span data-ttu-id="e0ae0-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0ae0-124">OUTPUTS</span></span>

### <span data-ttu-id="e0ae0-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="e0ae0-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="e0ae0-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0ae0-126">NOTES</span></span>

## <span data-ttu-id="e0ae0-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0ae0-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0ae0-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="e0ae0-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


