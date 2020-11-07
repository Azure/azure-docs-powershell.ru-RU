---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 337371f4ba42c80d8ebf3feed166a3804dd3f25e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907374"
---
# <span data-ttu-id="2fd97-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="2fd97-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="2fd97-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fd97-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd97-103">Создает или обновляет преобразование в задании.</span><span class="sxs-lookup"><span data-stu-id="2fd97-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="2fd97-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fd97-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fd97-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fd97-105">DESCRIPTION</span></span>
<span data-ttu-id="2fd97-106">Командлет **New-AzStreamAnalyticsTransformation** создает преобразование в рамках задания Stream Analytics или обновляет существующее преобразование.</span><span class="sxs-lookup"><span data-stu-id="2fd97-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="2fd97-107">Имя преобразования можно задать в поле. Файл JSON или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="2fd97-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="2fd97-108">Если заданы оба флажка, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="2fd97-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="2fd97-109">Если вы задаете уже существующее и не указали параметр Force, командлет запрашивает необходимость замены существующего преобразования.</span><span class="sxs-lookup"><span data-stu-id="2fd97-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="2fd97-110">Если указать параметр *Force* и задать существующее имя преобразования, преобразование будет заменено без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2fd97-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="2fd97-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fd97-111">EXAMPLES</span></span>

### <span data-ttu-id="2fd97-112">Пример 1: создание или замена преобразования в задании</span><span class="sxs-lookup"><span data-stu-id="2fd97-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="2fd97-113">Эта команда создает преобразование с именем StreamingJobTransform в задании, именуемом StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="2fd97-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="2fd97-114">Если существующее преобразование уже определено с этим именем, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="2fd97-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="2fd97-115">Пример 2: замена преобразования в задании</span><span class="sxs-lookup"><span data-stu-id="2fd97-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="2fd97-116">Эта команда заменяет определение StreamingJobTransform в задании StreamingJob без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2fd97-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="2fd97-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fd97-117">PARAMETERS</span></span>

### <span data-ttu-id="2fd97-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd97-118">-DefaultProfile</span></span>
<span data-ttu-id="2fd97-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fd97-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fd97-120">-Файл</span><span class="sxs-lookup"><span data-stu-id="2fd97-120">-File</span></span>
<span data-ttu-id="2fd97-121">Задает путь к файлу JSON, содержащему представление JSON преобразования Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="2fd97-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="2fd97-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2fd97-122">-Force</span></span>
<span data-ttu-id="2fd97-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2fd97-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fd97-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="2fd97-124">-JobName</span></span>
<span data-ttu-id="2fd97-125">Указывает имя задания Azure Stream Analytics, в котором нужно создать преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2fd97-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="2fd97-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fd97-126">-Name</span></span>
<span data-ttu-id="2fd97-127">Указывает имя создаваемого преобразования Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2fd97-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="2fd97-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fd97-128">-ResourceGroupName</span></span>
<span data-ttu-id="2fd97-129">Указывает имя группы ресурсов, в которой нужно создать преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2fd97-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="2fd97-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fd97-130">-Confirm</span></span>
<span data-ttu-id="2fd97-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fd97-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fd97-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fd97-132">-WhatIf</span></span>
<span data-ttu-id="2fd97-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fd97-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fd97-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fd97-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fd97-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd97-135">CommonParameters</span></span>
<span data-ttu-id="2fd97-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fd97-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd97-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fd97-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd97-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fd97-138">INPUTS</span></span>

### <span data-ttu-id="2fd97-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2fd97-139">System.String</span></span>

## <span data-ttu-id="2fd97-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fd97-140">OUTPUTS</span></span>

### <span data-ttu-id="2fd97-141">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="2fd97-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="2fd97-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fd97-142">NOTES</span></span>

## <span data-ttu-id="2fd97-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fd97-143">RELATED LINKS</span></span>

[<span data-ttu-id="2fd97-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="2fd97-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


