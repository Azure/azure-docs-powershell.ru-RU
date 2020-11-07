---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 60bc6754fb63d118e2b74e60ab503600a128ba3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907381"
---
# <span data-ttu-id="6d7db-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6d7db-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="6d7db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d7db-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7db-103">Создание или обновление входных данных задания.</span><span class="sxs-lookup"><span data-stu-id="6d7db-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="6d7db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d7db-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d7db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d7db-105">DESCRIPTION</span></span>
<span data-ttu-id="6d7db-106">Командлет **New-AzStreamAnalyticsInput** создает входные данные в задании Stream Analytics или обновляет существующие входные данные.</span><span class="sxs-lookup"><span data-stu-id="6d7db-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="6d7db-107">Имя входных данных можно задать в файле JSON или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="6d7db-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="6d7db-108">Если заданы оба флажка, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="6d7db-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="6d7db-109">Если вы задаете входные данные, которые уже существуют, и не указали параметр *Force* , командлет запрашивает, нужно ли заменять существующие входные данные.</span><span class="sxs-lookup"><span data-stu-id="6d7db-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="6d7db-110">Если вы укажете параметр *Force* и укажите существующее имя ввода, ввод будет заменен без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6d7db-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="6d7db-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d7db-111">EXAMPLES</span></span>

### <span data-ttu-id="6d7db-112">Пример 1: Создание входных данных задания с определением из файла</span><span class="sxs-lookup"><span data-stu-id="6d7db-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="6d7db-113">Эта команда создает входные данные из файла Input.json.</span><span class="sxs-lookup"><span data-stu-id="6d7db-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="6d7db-114">Если уже определено имя, указанное в файле определения входных данных, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="6d7db-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="6d7db-115">Пример 2: Создание входных данных задания</span><span class="sxs-lookup"><span data-stu-id="6d7db-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="6d7db-116">Эта команда создает новый ввод для задания с именем EntryStream.</span><span class="sxs-lookup"><span data-stu-id="6d7db-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="6d7db-117">Если уже определено имя с таким же именем, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="6d7db-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="6d7db-118">Пример 3: замена входных данных задания с определением из файла</span><span class="sxs-lookup"><span data-stu-id="6d7db-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="6d7db-119">Эта команда заменяет определение существующего источника входных данных с именем EntryStream с определением из файла без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6d7db-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="6d7db-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d7db-120">PARAMETERS</span></span>

### <span data-ttu-id="6d7db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7db-121">-DefaultProfile</span></span>
<span data-ttu-id="6d7db-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7db-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d7db-123">-Файл</span><span class="sxs-lookup"><span data-stu-id="6d7db-123">-File</span></span>
<span data-ttu-id="6d7db-124">Задает путь к файлу JSON, содержащему представление JSON ввода Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="6d7db-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="6d7db-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6d7db-125">-Force</span></span>
<span data-ttu-id="6d7db-126">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6d7db-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d7db-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="6d7db-127">-JobName</span></span>
<span data-ttu-id="6d7db-128">Указывает имя задания Azure Stream Analytics, в котором нужно создать вход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d7db-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="6d7db-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d7db-129">-Name</span></span>
<span data-ttu-id="6d7db-130">Указывает имя создаваемого ввода Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d7db-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="6d7db-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d7db-131">-ResourceGroupName</span></span>
<span data-ttu-id="6d7db-132">Указывает имя группы ресурсов, в которой нужно создать входные данные для потока Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7db-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="6d7db-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d7db-133">-Confirm</span></span>
<span data-ttu-id="6d7db-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d7db-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d7db-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d7db-135">-WhatIf</span></span>
<span data-ttu-id="6d7db-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d7db-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d7db-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d7db-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d7db-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7db-138">CommonParameters</span></span>
<span data-ttu-id="6d7db-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d7db-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7db-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d7db-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7db-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d7db-141">INPUTS</span></span>

### <span data-ttu-id="6d7db-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6d7db-142">System.String</span></span>

## <span data-ttu-id="6d7db-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d7db-143">OUTPUTS</span></span>

### <span data-ttu-id="6d7db-144">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="6d7db-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="6d7db-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d7db-145">NOTES</span></span>

## <span data-ttu-id="6d7db-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d7db-146">RELATED LINKS</span></span>

[<span data-ttu-id="6d7db-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6d7db-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="6d7db-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6d7db-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="6d7db-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6d7db-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


