---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E1141271-BA00-455C-AE80-DF5CD00348E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: c0dff4cb86ca46826a1fc7355a9f2c241d8de405
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076071"
---
# <span data-ttu-id="7755c-101">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7755c-101">Set-AzureAutomationSchedule</span></span>

## <span data-ttu-id="7755c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7755c-102">SYNOPSIS</span></span>

<span data-ttu-id="7755c-103">Изменение расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7755c-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="7755c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7755c-104">SYNTAX</span></span>

```
Set-AzureAutomationSchedule -Name <String> [-IsEnabled <Boolean>] [-Description <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7755c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7755c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7755c-106">Командлет **Set-AzureAutomationSchedule** изменяет расписание в Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7755c-106">The **Set-AzureAutomationSchedule** cmdlet modifies a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="7755c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7755c-107">EXAMPLES</span></span>

### <span data-ttu-id="7755c-108">Пример 1: изменение расписания</span><span class="sxs-lookup"><span data-stu-id="7755c-108">Example 1: Modify a schedule</span></span>
```
PS C:\> Set-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule"
```

<span data-ttu-id="7755c-109">Эта команда изменяет описание расписания с именем Schedule01.</span><span class="sxs-lookup"><span data-stu-id="7755c-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="7755c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7755c-110">PARAMETERS</span></span>

### <span data-ttu-id="7755c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7755c-111">-AutomationAccountName</span></span>
<span data-ttu-id="7755c-112">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7755c-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="7755c-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="7755c-113">-Description</span></span>
<span data-ttu-id="7755c-114">Задает описание расписания.</span><span class="sxs-lookup"><span data-stu-id="7755c-114">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7755c-115">-Включено</span><span class="sxs-lookup"><span data-stu-id="7755c-115">-IsEnabled</span></span>
<span data-ttu-id="7755c-116">Указывает, включено ли расписание.</span><span class="sxs-lookup"><span data-stu-id="7755c-116">Indicates whether the schedule is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7755c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7755c-117">-Name</span></span>
<span data-ttu-id="7755c-118">Задает имя расписания.</span><span class="sxs-lookup"><span data-stu-id="7755c-118">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="7755c-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="7755c-119">-Profile</span></span>
<span data-ttu-id="7755c-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7755c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7755c-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7755c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7755c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7755c-122">CommonParameters</span></span>
<span data-ttu-id="7755c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7755c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7755c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7755c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7755c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7755c-125">INPUTS</span></span>

## <span data-ttu-id="7755c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7755c-126">OUTPUTS</span></span>

### <span data-ttu-id="7755c-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="7755c-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="7755c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="7755c-128">NOTES</span></span>

## <span data-ttu-id="7755c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7755c-129">RELATED LINKS</span></span>

[<span data-ttu-id="7755c-130">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7755c-130">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="7755c-131">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7755c-131">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="7755c-132">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7755c-132">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)


