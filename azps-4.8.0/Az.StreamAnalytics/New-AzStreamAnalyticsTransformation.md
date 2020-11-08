---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080148"
---
# <span data-ttu-id="ad157-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="ad157-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="ad157-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad157-102">SYNOPSIS</span></span>
<span data-ttu-id="ad157-103">Создает или обновляет преобразование в задании.</span><span class="sxs-lookup"><span data-stu-id="ad157-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="ad157-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad157-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad157-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad157-105">DESCRIPTION</span></span>
<span data-ttu-id="ad157-106">Командлет **New-AzStreamAnalyticsTransformation** создает преобразование в рамках задания Stream Analytics или обновляет существующее преобразование.</span><span class="sxs-lookup"><span data-stu-id="ad157-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="ad157-107">Имя преобразования можно задать в поле. Файл JSON или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="ad157-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="ad157-108">Если заданы оба флажка, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="ad157-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="ad157-109">Если вы задаете уже существующее и не указали параметр Force, командлет запрашивает необходимость замены существующего преобразования.</span><span class="sxs-lookup"><span data-stu-id="ad157-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="ad157-110">Если указать параметр *Force* и задать существующее имя преобразования, преобразование будет заменено без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ad157-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="ad157-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad157-111">EXAMPLES</span></span>

### <span data-ttu-id="ad157-112">Пример 1: создание или замена преобразования в задании</span><span class="sxs-lookup"><span data-stu-id="ad157-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="ad157-113">Эта команда создает преобразование с именем StreamingJobTransform в задании, именуемом StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="ad157-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="ad157-114">Если существующее преобразование уже определено с этим именем, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="ad157-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="ad157-115">Пример 2: замена преобразования в задании</span><span class="sxs-lookup"><span data-stu-id="ad157-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="ad157-116">Эта команда заменяет определение StreamingJobTransform в задании StreamingJob без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ad157-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="ad157-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad157-117">PARAMETERS</span></span>

### <span data-ttu-id="ad157-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad157-118">-DefaultProfile</span></span>
<span data-ttu-id="ad157-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad157-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad157-120">-Файл</span><span class="sxs-lookup"><span data-stu-id="ad157-120">-File</span></span>
<span data-ttu-id="ad157-121">Задает путь к файлу JSON, содержащему представление JSON преобразования Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="ad157-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="ad157-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ad157-122">-Force</span></span>
<span data-ttu-id="ad157-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad157-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad157-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="ad157-124">-JobName</span></span>
<span data-ttu-id="ad157-125">Указывает имя задания Azure Stream Analytics, в котором нужно создать преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ad157-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="ad157-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad157-126">-Name</span></span>
<span data-ttu-id="ad157-127">Указывает имя создаваемого преобразования Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ad157-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="ad157-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad157-128">-ResourceGroupName</span></span>
<span data-ttu-id="ad157-129">Указывает имя группы ресурсов, в которой нужно создать преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ad157-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="ad157-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad157-130">-Confirm</span></span>
<span data-ttu-id="ad157-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad157-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad157-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad157-132">-WhatIf</span></span>
<span data-ttu-id="ad157-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad157-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad157-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad157-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad157-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad157-135">CommonParameters</span></span>
<span data-ttu-id="ad157-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad157-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad157-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad157-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad157-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad157-138">INPUTS</span></span>

### <span data-ttu-id="ad157-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ad157-139">System.String</span></span>

## <span data-ttu-id="ad157-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad157-140">OUTPUTS</span></span>

### <span data-ttu-id="ad157-141">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="ad157-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="ad157-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad157-142">NOTES</span></span>

## <span data-ttu-id="ad157-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad157-143">RELATED LINKS</span></span>

[<span data-ttu-id="ad157-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="ad157-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)

