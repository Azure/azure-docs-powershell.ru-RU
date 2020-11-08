---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 436A6D6E-2280-475C-A1F5-6A6D72DAD9E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4895c9aa12ad56b8e3ddffb88a19439777d5b54a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075655"
---
# <span data-ttu-id="6375e-101">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6375e-101">Get-AzureAutomationSchedule</span></span>

## <span data-ttu-id="6375e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6375e-102">SYNOPSIS</span></span>

<span data-ttu-id="6375e-103">Получает расписание автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6375e-103">Gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="6375e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6375e-104">SYNTAX</span></span>

### <span data-ttu-id="6375e-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6375e-105">ByAll (Default)</span></span>
```
Get-AzureAutomationSchedule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6375e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6375e-106">ByName</span></span>
```
Get-AzureAutomationSchedule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6375e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6375e-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6375e-108">Командлет **Get-AzureAutomationSchedule** получает расписание Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6375e-108">The **Get-AzureAutomationSchedule** cmdlet gets a Microsoft Azure Automation schedule.</span></span>

## <span data-ttu-id="6375e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6375e-109">EXAMPLES</span></span>

### <span data-ttu-id="6375e-110">Пример 1: получение расписания</span><span class="sxs-lookup"><span data-stu-id="6375e-110">Example 1: Get a schedule</span></span>
```
PS C:\> Get-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08"
```

<span data-ttu-id="6375e-111">Эта команда получает расписание с именем DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="6375e-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="6375e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6375e-112">PARAMETERS</span></span>

### <span data-ttu-id="6375e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6375e-113">-AutomationAccountName</span></span>
<span data-ttu-id="6375e-114">Указывает имя учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6375e-114">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="6375e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6375e-115">-Name</span></span>
<span data-ttu-id="6375e-116">Указывает имя расписания.</span><span class="sxs-lookup"><span data-stu-id="6375e-116">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6375e-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="6375e-117">-Profile</span></span>
<span data-ttu-id="6375e-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6375e-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6375e-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6375e-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6375e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6375e-120">CommonParameters</span></span>
<span data-ttu-id="6375e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6375e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6375e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6375e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6375e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6375e-123">INPUTS</span></span>

## <span data-ttu-id="6375e-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6375e-124">OUTPUTS</span></span>

### <span data-ttu-id="6375e-125">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="6375e-125">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="6375e-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="6375e-126">NOTES</span></span>

## <span data-ttu-id="6375e-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6375e-127">RELATED LINKS</span></span>

[<span data-ttu-id="6375e-128">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6375e-128">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="6375e-129">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6375e-129">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="6375e-130">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6375e-130">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


