---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414391"
---
# <span data-ttu-id="c6e32-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="c6e32-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="c6e32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6e32-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e32-103">Создает или обновляет преобразование в рамках задания.</span><span class="sxs-lookup"><span data-stu-id="c6e32-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="c6e32-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c6e32-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6e32-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6e32-105">DESCRIPTION</span></span>
<span data-ttu-id="c6e32-106">Для преобразования в рамках задания Анализа Stream или обновляется существующее преобразование с его функцией **New-AzStreamAnalyticsTransformation.**</span><span class="sxs-lookup"><span data-stu-id="c6e32-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="c6e32-107">Имя преобразования может быть указано в .. JSON-файл или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="c6e32-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="c6e32-108">Если они заданы, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="c6e32-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="c6e32-109">Если указать существующее преобразование и не задать параметр Force, будет указано, следует ли заменить существующее преобразование.</span><span class="sxs-lookup"><span data-stu-id="c6e32-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="c6e32-110">Если задать параметр *Force* и указать существующее имя преобразования, преобразование будет заменено без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c6e32-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="c6e32-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c6e32-111">EXAMPLES</span></span>

### <span data-ttu-id="c6e32-112">Пример 1. Создание или замена преобразования в задаче</span><span class="sxs-lookup"><span data-stu-id="c6e32-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="c6e32-113">Эта команда создает преобразование под названием StreamingJobTransform в задаче StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="c6e32-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="c6e32-114">Если существующее преобразование уже определено с этим именем, будет высображено, следует ли заменить его.</span><span class="sxs-lookup"><span data-stu-id="c6e32-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="c6e32-115">Пример 2. Замена преобразования в задаче</span><span class="sxs-lookup"><span data-stu-id="c6e32-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="c6e32-116">Эта команда заменяет определение StreamingJobTransform в командной ленте StreamingJob без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c6e32-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="c6e32-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6e32-117">PARAMETERS</span></span>

### <span data-ttu-id="c6e32-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e32-118">-DefaultProfile</span></span>
<span data-ttu-id="c6e32-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e32-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6e32-120">-File</span><span class="sxs-lookup"><span data-stu-id="c6e32-120">-File</span></span>
<span data-ttu-id="c6e32-121">Путь к файлу JSON, который содержит представление JSON преобразования Azure Stream Analytics, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="c6e32-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e32-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c6e32-122">-Force</span></span>
<span data-ttu-id="c6e32-123">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c6e32-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e32-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="c6e32-124">-JobName</span></span>
<span data-ttu-id="c6e32-125">Указывает имя задания Azure Stream Analytics, для которого нужно создать преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="c6e32-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="c6e32-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c6e32-126">-Name</span></span>
<span data-ttu-id="c6e32-127">Указывает имя преобразования службы Azure Stream Analytics, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="c6e32-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e32-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e32-128">-ResourceGroupName</span></span>
<span data-ttu-id="c6e32-129">Указывает имя группы ресурсов, для которой нужно создать преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="c6e32-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="c6e32-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6e32-130">-Confirm</span></span>
<span data-ttu-id="c6e32-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c6e32-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e32-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6e32-132">-WhatIf</span></span>
<span data-ttu-id="c6e32-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6e32-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6e32-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c6e32-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e32-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e32-135">CommonParameters</span></span>
<span data-ttu-id="c6e32-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e32-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e32-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e32-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e32-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6e32-138">INPUTS</span></span>

### <span data-ttu-id="c6e32-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c6e32-139">System.String</span></span>

## <span data-ttu-id="c6e32-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6e32-140">OUTPUTS</span></span>

### <span data-ttu-id="c6e32-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="c6e32-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="c6e32-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c6e32-142">NOTES</span></span>

## <span data-ttu-id="c6e32-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6e32-143">RELATED LINKS</span></span>

[<span data-ttu-id="c6e32-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="c6e32-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


