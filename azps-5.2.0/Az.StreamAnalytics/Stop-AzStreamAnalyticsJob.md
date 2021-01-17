---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414351"
---
# <span data-ttu-id="31b2c-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="31b2c-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="31b2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="31b2c-103">Остановка задания stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="31b2c-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="31b2c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31b2c-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b2c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="31b2c-106">Асинхронно при запуске cmdlet **Stop-AzStreamAnalyticsJob** в Azure задание Stream Analytics прекращает работу и поиск используемых ресурсов с последующим поиском.</span><span class="sxs-lookup"><span data-stu-id="31b2c-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="31b2c-107">Определение задания и метаданные остаются доступными в рамках подписки через портал Azure и API управления, что дает возможность редактировать и перезапускать задание.</span><span class="sxs-lookup"><span data-stu-id="31b2c-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="31b2c-108">Плата за задание в состоянии "Остановлено" взиматься не будет.</span><span class="sxs-lookup"><span data-stu-id="31b2c-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="31b2c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31b2c-109">EXAMPLES</span></span>

### <span data-ttu-id="31b2c-110">Пример 1. Остановка запуска задания</span><span class="sxs-lookup"><span data-stu-id="31b2c-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="31b2c-111">Эта команда останавливает задание StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="31b2c-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="31b2c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31b2c-112">PARAMETERS</span></span>

### <span data-ttu-id="31b2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b2c-113">-DefaultProfile</span></span>
<span data-ttu-id="31b2c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31b2c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b2c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="31b2c-115">-Name</span></span>
<span data-ttu-id="31b2c-116">Указывает имя задания аналитики Azure Stream Analytics, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="31b2c-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="31b2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="31b2c-118">Имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="31b2c-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="31b2c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b2c-119">CommonParameters</span></span>
<span data-ttu-id="31b2c-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b2c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b2c-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b2c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b2c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31b2c-122">INPUTS</span></span>

### <span data-ttu-id="31b2c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="31b2c-123">System.String</span></span>

## <span data-ttu-id="31b2c-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31b2c-124">OUTPUTS</span></span>

### <span data-ttu-id="31b2c-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31b2c-125">System.Boolean</span></span>

## <span data-ttu-id="31b2c-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31b2c-126">NOTES</span></span>

## <span data-ttu-id="31b2c-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31b2c-127">RELATED LINKS</span></span>

[<span data-ttu-id="31b2c-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="31b2c-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="31b2c-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="31b2c-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="31b2c-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="31b2c-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="31b2c-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="31b2c-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="31b2c-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="31b2c-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


