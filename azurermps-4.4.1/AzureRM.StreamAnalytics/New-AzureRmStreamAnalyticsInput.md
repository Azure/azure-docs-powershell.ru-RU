---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 84df5d0ed28b2d11b3e03e298242da4938a47eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569152"
---
# <span data-ttu-id="7a19f-101">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7a19f-101">New-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="7a19f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a19f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a19f-103">Создание или обновление входных данных задания.</span><span class="sxs-lookup"><span data-stu-id="7a19f-103">Creates or updates a job input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a19f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a19f-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a19f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a19f-105">DESCRIPTION</span></span>
<span data-ttu-id="7a19f-106">Командлет **New-AzureRmStreamAnalyticsInput** создает входные данные в задании Stream Analytics или обновляет существующие входные данные.</span><span class="sxs-lookup"><span data-stu-id="7a19f-106">The **New-AzureRmStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="7a19f-107">Имя входных данных можно задать в файле JSON или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="7a19f-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="7a19f-108">Если заданы оба флажка, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="7a19f-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="7a19f-109">Если вы задаете входные данные, которые уже существуют, и не указали параметр *Force* , командлет запрашивает, нужно ли заменять существующие входные данные.</span><span class="sxs-lookup"><span data-stu-id="7a19f-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>

<span data-ttu-id="7a19f-110">Если вы укажете параметр *Force* и укажите существующее имя ввода, ввод будет заменен без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7a19f-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="7a19f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a19f-111">EXAMPLES</span></span>

### <span data-ttu-id="7a19f-112">Пример 1: Создание входных данных задания с определением из файла</span><span class="sxs-lookup"><span data-stu-id="7a19f-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="7a19f-113">Эта команда создает входные данные из файла Input.json.</span><span class="sxs-lookup"><span data-stu-id="7a19f-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="7a19f-114">Если уже определено имя, указанное в файле определения входных данных, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="7a19f-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="7a19f-115">Пример 2: Создание входных данных задания</span><span class="sxs-lookup"><span data-stu-id="7a19f-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="7a19f-116">Эта команда создает новый ввод для задания с именем EntryStream.</span><span class="sxs-lookup"><span data-stu-id="7a19f-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="7a19f-117">Если уже определено имя с таким же именем, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="7a19f-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="7a19f-118">Пример 3: замена входных данных задания с определением из файла</span><span class="sxs-lookup"><span data-stu-id="7a19f-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="7a19f-119">Эта команда заменяет определение существующего источника входных данных с именем EntryStream с определением из файла без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7a19f-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="7a19f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a19f-120">PARAMETERS</span></span>

### <span data-ttu-id="7a19f-121">-Файл</span><span class="sxs-lookup"><span data-stu-id="7a19f-121">-File</span></span>
<span data-ttu-id="7a19f-122">Задает путь к файлу JSON, содержащему представление JSON ввода Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="7a19f-122">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="7a19f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7a19f-123">-Force</span></span>
<span data-ttu-id="7a19f-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7a19f-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a19f-125">-JobName</span><span class="sxs-lookup"><span data-stu-id="7a19f-125">-JobName</span></span>
<span data-ttu-id="7a19f-126">Указывает имя задания Azure Stream Analytics, в котором нужно создать вход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7a19f-126">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="7a19f-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a19f-127">-Name</span></span>
<span data-ttu-id="7a19f-128">Указывает имя создаваемого ввода Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7a19f-128">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="7a19f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a19f-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a19f-130">Указывает имя группы ресурсов, в которой нужно создать входные данные для потока Azure.</span><span class="sxs-lookup"><span data-stu-id="7a19f-130">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="7a19f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a19f-131">-Confirm</span></span>
<span data-ttu-id="7a19f-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a19f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a19f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a19f-133">-WhatIf</span></span>
<span data-ttu-id="7a19f-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a19f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a19f-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a19f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a19f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a19f-136">-DefaultProfile</span></span>
<span data-ttu-id="7a19f-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a19f-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a19f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a19f-138">CommonParameters</span></span>
<span data-ttu-id="7a19f-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a19f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a19f-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a19f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a19f-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a19f-141">INPUTS</span></span>

## <span data-ttu-id="7a19f-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a19f-142">OUTPUTS</span></span>

### <span data-ttu-id="7a19f-143">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="7a19f-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="7a19f-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a19f-144">NOTES</span></span>

## <span data-ttu-id="7a19f-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a19f-145">RELATED LINKS</span></span>

[<span data-ttu-id="7a19f-146">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7a19f-146">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="7a19f-147">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7a19f-147">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="7a19f-148">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7a19f-148">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


