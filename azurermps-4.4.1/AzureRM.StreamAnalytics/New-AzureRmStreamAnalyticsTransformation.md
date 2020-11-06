---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: eb9f8b82e8ff8a0f60931953f2a3b4349e7b4a4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561984"
---
# <span data-ttu-id="9b2cf-101">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="9b2cf-101">New-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="9b2cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b2cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2cf-103">Создает или обновляет преобразование в задании.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-103">Creates or updates a transformation within a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b2cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b2cf-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b2cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b2cf-105">DESCRIPTION</span></span>
<span data-ttu-id="9b2cf-106">Командлет **New-AzureRmStreamAnalyticsTransformation** создает преобразование в рамках задания Stream Analytics или обновляет существующее преобразование.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-106">The **New-AzureRmStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="9b2cf-107">Имя преобразования можно задать в поле. Файл JSON или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="9b2cf-108">Если заданы оба флажка, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="9b2cf-109">Если вы задаете уже существующее и не указали параметр Force, командлет запрашивает необходимость замены существующего преобразования.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>

<span data-ttu-id="9b2cf-110">Если указать параметр *Force* и задать существующее имя преобразования, преобразование будет заменено без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="9b2cf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b2cf-111">EXAMPLES</span></span>

### <span data-ttu-id="9b2cf-112">Пример 1: создание или замена преобразования в задании</span><span class="sxs-lookup"><span data-stu-id="9b2cf-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="9b2cf-113">Эта команда создает преобразование с именем StreamingJobTransform в задании, именуемом StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="9b2cf-114">Если существующее преобразование уже определено с этим именем, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="9b2cf-115">Пример 2: замена преобразования в задании</span><span class="sxs-lookup"><span data-stu-id="9b2cf-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="9b2cf-116">Эта команда заменяет определение StreamingJobTransform в задании StreamingJob без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="9b2cf-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b2cf-117">PARAMETERS</span></span>

### <span data-ttu-id="9b2cf-118">-Файл</span><span class="sxs-lookup"><span data-stu-id="9b2cf-118">-File</span></span>
<span data-ttu-id="9b2cf-119">Задает путь к файлу JSON, содержащему представление JSON преобразования Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="9b2cf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9b2cf-120">-Force</span></span>
<span data-ttu-id="9b2cf-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9b2cf-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="9b2cf-122">-JobName</span></span>
<span data-ttu-id="9b2cf-123">Указывает имя задания Azure Stream Analytics, в котором нужно создать преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-123">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="9b2cf-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b2cf-124">-Name</span></span>
<span data-ttu-id="9b2cf-125">Указывает имя создаваемого преобразования Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-125">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="9b2cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b2cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b2cf-127">Указывает имя группы ресурсов, в которой нужно создать преобразование Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-127">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="9b2cf-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b2cf-128">-Confirm</span></span>
<span data-ttu-id="9b2cf-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b2cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b2cf-130">-WhatIf</span></span>
<span data-ttu-id="9b2cf-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b2cf-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b2cf-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2cf-133">-DefaultProfile</span></span>
<span data-ttu-id="9b2cf-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b2cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2cf-135">CommonParameters</span></span>
<span data-ttu-id="9b2cf-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b2cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2cf-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b2cf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2cf-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b2cf-138">INPUTS</span></span>

## <span data-ttu-id="9b2cf-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b2cf-139">OUTPUTS</span></span>

### <span data-ttu-id="9b2cf-140">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="9b2cf-140">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="9b2cf-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b2cf-141">NOTES</span></span>

## <span data-ttu-id="9b2cf-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b2cf-142">RELATED LINKS</span></span>

[<span data-ttu-id="9b2cf-143">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="9b2cf-143">Get-AzureRmStreamAnalyticsTransformation</span></span>](./Get-AzureRmStreamAnalyticsTransformation.md)


