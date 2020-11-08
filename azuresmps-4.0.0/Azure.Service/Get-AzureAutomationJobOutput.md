---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075658"
---
# <span data-ttu-id="11f84-101">Get-AzureAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="11f84-101">Get-AzureAutomationJobOutput</span></span>

## <span data-ttu-id="11f84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11f84-102">SYNOPSIS</span></span>

<span data-ttu-id="11f84-103">Получает выходные данные задания службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="11f84-103">Gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="11f84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11f84-104">SYNTAX</span></span>

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="11f84-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11f84-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="11f84-106">Командлет **Get-AzureAutomationJobOutput** получает выходные данные задания Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="11f84-106">The **Get-AzureAutomationJobOutput** cmdlet gets the output of a Microsoft Azure Automation job.</span></span>

## <span data-ttu-id="11f84-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11f84-107">EXAMPLES</span></span>

### <span data-ttu-id="11f84-108">Пример 1: получение выходных данных задания службы автоматизации Azure</span><span class="sxs-lookup"><span data-stu-id="11f84-108">Example 1: Get the output of an Azure Automation job</span></span>
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

<span data-ttu-id="11f84-109">Эта команда получает все выходные данные задания с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="11f84-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="11f84-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11f84-110">PARAMETERS</span></span>

### <span data-ttu-id="11f84-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11f84-111">-AutomationAccountName</span></span>
<span data-ttu-id="11f84-112">Указывает имя учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="11f84-112">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f84-113">-ID</span><span class="sxs-lookup"><span data-stu-id="11f84-113">-Id</span></span>
<span data-ttu-id="11f84-114">Указывает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="11f84-114">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f84-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="11f84-115">-Profile</span></span>
<span data-ttu-id="11f84-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="11f84-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11f84-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="11f84-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f84-118">-StartTime</span><span class="sxs-lookup"><span data-stu-id="11f84-118">-StartTime</span></span>
<span data-ttu-id="11f84-119">Указывает время начала.</span><span class="sxs-lookup"><span data-stu-id="11f84-119">Specifies a start time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f84-120">-Stream</span><span class="sxs-lookup"><span data-stu-id="11f84-120">-Stream</span></span>
<span data-ttu-id="11f84-121">Указывает тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="11f84-121">Specifies the type of output.</span></span>
<span data-ttu-id="11f84-122">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="11f84-122">Valid values are:</span></span> 

- <span data-ttu-id="11f84-123">Необходимые</span><span class="sxs-lookup"><span data-stu-id="11f84-123">Any</span></span>
- <span data-ttu-id="11f84-124">Приглашен</span><span class="sxs-lookup"><span data-stu-id="11f84-124">Debug</span></span>
- <span data-ttu-id="11f84-125">Ошибки</span><span class="sxs-lookup"><span data-stu-id="11f84-125">Error</span></span>
- <span data-ttu-id="11f84-126">Результата</span><span class="sxs-lookup"><span data-stu-id="11f84-126">Output</span></span>
- <span data-ttu-id="11f84-127">Последовательно</span><span class="sxs-lookup"><span data-stu-id="11f84-127">Progress</span></span>
- <span data-ttu-id="11f84-128">Подробный</span><span class="sxs-lookup"><span data-stu-id="11f84-128">Verbose</span></span>
- <span data-ttu-id="11f84-129">Об</span><span class="sxs-lookup"><span data-stu-id="11f84-129">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f84-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f84-130">CommonParameters</span></span>
<span data-ttu-id="11f84-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11f84-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f84-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f84-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f84-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11f84-133">INPUTS</span></span>

## <span data-ttu-id="11f84-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11f84-134">OUTPUTS</span></span>

## <span data-ttu-id="11f84-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="11f84-135">NOTES</span></span>

## <span data-ttu-id="11f84-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11f84-136">RELATED LINKS</span></span>

[<span data-ttu-id="11f84-137">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="11f84-137">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="11f84-138">Возобновить — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="11f84-138">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="11f84-139">Остановить-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="11f84-139">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="11f84-140">Приостановить — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="11f84-140">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


