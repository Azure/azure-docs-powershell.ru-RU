---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 49fe9e11bb11131f8270c53afc0fc9fb6ab6dae9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728426"
---
# <span data-ttu-id="dd928-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dd928-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="dd928-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd928-102">SYNOPSIS</span></span>
<span data-ttu-id="dd928-103">Проверяет состояние подключения для вывода.</span><span class="sxs-lookup"><span data-stu-id="dd928-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="dd928-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd928-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd928-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd928-105">DESCRIPTION</span></span>
<span data-ttu-id="dd928-106">Командлет **Test-AzStreamAnalyticsOutput** проверяет способность Stream Analytics подключаться к выходным данным.</span><span class="sxs-lookup"><span data-stu-id="dd928-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="dd928-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd928-107">EXAMPLES</span></span>

### <span data-ttu-id="dd928-108">Пример 1: Проверка состояния подключения вывода</span><span class="sxs-lookup"><span data-stu-id="dd928-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="dd928-109">Это проверяет состояние подключения выходного выхода в StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="dd928-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="dd928-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd928-110">PARAMETERS</span></span>

### <span data-ttu-id="dd928-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd928-111">-DefaultProfile</span></span>
<span data-ttu-id="dd928-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd928-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd928-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="dd928-113">-JobName</span></span>
<span data-ttu-id="dd928-114">Указывает имя задания Azure Stream Analytics, которому принадлежит требуемый выходной файл Azure Streaming Analytics.</span><span class="sxs-lookup"><span data-stu-id="dd928-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="dd928-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd928-115">-Name</span></span>
<span data-ttu-id="dd928-116">Указывает имя выходных данных Azure Stream Analytics для проверки.</span><span class="sxs-lookup"><span data-stu-id="dd928-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="dd928-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd928-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd928-118">Указывает имя группы ресурсов, к которой относятся выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="dd928-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="dd928-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd928-119">CommonParameters</span></span>
<span data-ttu-id="dd928-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd928-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd928-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd928-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd928-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd928-122">INPUTS</span></span>

### <span data-ttu-id="dd928-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dd928-123">System.String</span></span>

## <span data-ttu-id="dd928-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd928-124">OUTPUTS</span></span>

### <span data-ttu-id="dd928-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd928-125">System.Boolean</span></span>

## <span data-ttu-id="dd928-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd928-126">NOTES</span></span>

## <span data-ttu-id="dd928-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd928-127">RELATED LINKS</span></span>

[<span data-ttu-id="dd928-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dd928-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="dd928-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dd928-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="dd928-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dd928-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


