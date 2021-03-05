---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 6dfb659987178b4bfe65855552e1018d085de360
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973827"
---
# <span data-ttu-id="1730b-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1730b-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="1730b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1730b-102">SYNOPSIS</span></span>
<span data-ttu-id="1730b-103">Создает или обновляет ввод задания.</span><span class="sxs-lookup"><span data-stu-id="1730b-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="1730b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1730b-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1730b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1730b-105">DESCRIPTION</span></span>
<span data-ttu-id="1730b-106">**Cmdlet New-AzStreamAnalyticsInput** создает входные данные в заданиях Stream Analytics или обновляет существующие входные данные.</span><span class="sxs-lookup"><span data-stu-id="1730b-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="1730b-107">Имя входных данных может быть указано в файле JSON или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="1730b-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="1730b-108">Если они заданы, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="1730b-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="1730b-109">Если вы указали входные данные, которые уже существуют и не указали параметр *Force,* будет указано, следует ли заменять существующие входные данные.</span><span class="sxs-lookup"><span data-stu-id="1730b-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="1730b-110">Если задать параметр *Force* и указать существующее входное имя, входные данные будут заменены без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1730b-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="1730b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1730b-111">EXAMPLES</span></span>

### <span data-ttu-id="1730b-112">Пример 1. Создание задания ввода с определением из файла</span><span class="sxs-lookup"><span data-stu-id="1730b-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="1730b-113">Эта команда создает входные данные из Input.jsфайла.</span><span class="sxs-lookup"><span data-stu-id="1730b-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="1730b-114">Если уже определен существующий входной код с именем, указанным в файле определения входных данных, будет указано, следует ли заменить его.</span><span class="sxs-lookup"><span data-stu-id="1730b-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="1730b-115">Пример 2. Создание задания</span><span class="sxs-lookup"><span data-stu-id="1730b-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="1730b-116">Эта команда создает новый вход для задания EntryStream.</span><span class="sxs-lookup"><span data-stu-id="1730b-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="1730b-117">Если существующее имя уже определено, будет выводить запрос на его замену.</span><span class="sxs-lookup"><span data-stu-id="1730b-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="1730b-118">Пример 3. Замена ввода задания определением из файла</span><span class="sxs-lookup"><span data-stu-id="1730b-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="1730b-119">Эта команда заменяет определение существующего источника ввода EntryStream определением из файла без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1730b-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="1730b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1730b-120">PARAMETERS</span></span>

### <span data-ttu-id="1730b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1730b-121">-DefaultProfile</span></span>
<span data-ttu-id="1730b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1730b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1730b-123">-File</span><span class="sxs-lookup"><span data-stu-id="1730b-123">-File</span></span>
<span data-ttu-id="1730b-124">Путь к файлу JSON, который содержит представление JSON входной информации Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="1730b-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="1730b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1730b-125">-Force</span></span>
<span data-ttu-id="1730b-126">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1730b-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1730b-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="1730b-127">-JobName</span></span>
<span data-ttu-id="1730b-128">Указывает имя задания Azure Stream Analytics, для которого нужно создать входные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="1730b-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="1730b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="1730b-129">-Name</span></span>
<span data-ttu-id="1730b-130">Указывает имя входных данных службы Azure Stream Analytics, которые нужно создать.</span><span class="sxs-lookup"><span data-stu-id="1730b-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="1730b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1730b-131">-ResourceGroupName</span></span>
<span data-ttu-id="1730b-132">Имя группы ресурсов, для которой нужно создать потоковую передачу Azure.</span><span class="sxs-lookup"><span data-stu-id="1730b-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="1730b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1730b-133">-Confirm</span></span>
<span data-ttu-id="1730b-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1730b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1730b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1730b-135">-WhatIf</span></span>
<span data-ttu-id="1730b-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1730b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1730b-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1730b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1730b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1730b-138">CommonParameters</span></span>
<span data-ttu-id="1730b-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1730b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1730b-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1730b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1730b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1730b-141">INPUTS</span></span>

### <span data-ttu-id="1730b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1730b-142">System.String</span></span>

## <span data-ttu-id="1730b-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1730b-143">OUTPUTS</span></span>

### <span data-ttu-id="1730b-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="1730b-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="1730b-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1730b-145">NOTES</span></span>

## <span data-ttu-id="1730b-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1730b-146">RELATED LINKS</span></span>

[<span data-ttu-id="1730b-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1730b-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="1730b-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1730b-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="1730b-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1730b-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


