---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 24313884b92a9a4c738425d64463c695ff689c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560423"
---
# <span data-ttu-id="e21e0-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="e21e0-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="e21e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e21e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e21e0-103">Получает сведения о преобразовании задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e21e0-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e21e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e21e0-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e21e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e21e0-105">DESCRIPTION</span></span>
<span data-ttu-id="e21e0-106">Командлет **Get-AzureRmStreamAnalyticsTransformation** получает сведения о преобразовании, определенном в задании Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e21e0-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="e21e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e21e0-107">EXAMPLES</span></span>

### <span data-ttu-id="e21e0-108">Пример 1: получение сведений об преобразовании Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="e21e0-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="e21e0-109">Эта команда возвращает сведения о преобразовании с именем StreamingJob для задания с именем StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="e21e0-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="e21e0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e21e0-110">PARAMETERS</span></span>

### <span data-ttu-id="e21e0-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="e21e0-111">-JobName</span></span>
<span data-ttu-id="e21e0-112">Указывает имя задания Azure Stream Analytics, которому принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e21e0-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="e21e0-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e21e0-113">-Name</span></span>
<span data-ttu-id="e21e0-114">Указывает имя извлекаемого преобразования Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e21e0-114">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="e21e0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21e0-115">-ResourceGroupName</span></span>
<span data-ttu-id="e21e0-116">Указывает имя группы ресурсов, которой принадлежит преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="e21e0-116">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="e21e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21e0-117">-DefaultProfile</span></span>
<span data-ttu-id="e21e0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e21e0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e21e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21e0-119">CommonParameters</span></span>
<span data-ttu-id="e21e0-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e21e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21e0-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e21e0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21e0-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e21e0-122">INPUTS</span></span>

## <span data-ttu-id="e21e0-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e21e0-123">OUTPUTS</span></span>

### <span data-ttu-id="e21e0-124">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="e21e0-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="e21e0-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e21e0-125">NOTES</span></span>

## <span data-ttu-id="e21e0-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e21e0-126">RELATED LINKS</span></span>

[<span data-ttu-id="e21e0-127">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="e21e0-127">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


