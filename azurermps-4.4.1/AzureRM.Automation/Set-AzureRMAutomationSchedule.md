---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: 03763ad7c2212eb89650749eb6d407d9ce973693
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560559"
---
# <span data-ttu-id="a218c-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a218c-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="a218c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a218c-102">SYNOPSIS</span></span>
<span data-ttu-id="a218c-103">Изменение расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a218c-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a218c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a218c-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a218c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a218c-105">DESCRIPTION</span></span>
<span data-ttu-id="a218c-106">Командлет **Set-AzureRmAutomationSchedule** изменяет расписание в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a218c-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="a218c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a218c-107">EXAMPLES</span></span>

### <span data-ttu-id="a218c-108">Пример 1: изменение расписания</span><span class="sxs-lookup"><span data-stu-id="a218c-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a218c-109">Эта команда изменяет описание расписания с именем Schedule01.</span><span class="sxs-lookup"><span data-stu-id="a218c-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="a218c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a218c-110">PARAMETERS</span></span>

### <span data-ttu-id="a218c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a218c-111">-AutomationAccountName</span></span>
<span data-ttu-id="a218c-112">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет расписание.</span><span class="sxs-lookup"><span data-stu-id="a218c-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="a218c-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="a218c-113">-Description</span></span>
<span data-ttu-id="a218c-114">Задает описание расписания.</span><span class="sxs-lookup"><span data-stu-id="a218c-114">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a218c-115">-Включено</span><span class="sxs-lookup"><span data-stu-id="a218c-115">-IsEnabled</span></span>
<span data-ttu-id="a218c-116">Указывает, включает ли этот командлет расписание.</span><span class="sxs-lookup"><span data-stu-id="a218c-116">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a218c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a218c-117">-Name</span></span>
<span data-ttu-id="a218c-118">Указывает имя расписания, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a218c-118">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a218c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a218c-119">-ResourceGroupName</span></span>
<span data-ttu-id="a218c-120">Указывает имя группы ресурсов, для которой этот командлет изменяет расписание.</span><span class="sxs-lookup"><span data-stu-id="a218c-120">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="a218c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a218c-121">-DefaultProfile</span></span>
<span data-ttu-id="a218c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a218c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a218c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a218c-123">CommonParameters</span></span>
<span data-ttu-id="a218c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a218c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a218c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a218c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a218c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a218c-126">INPUTS</span></span>

## <span data-ttu-id="a218c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a218c-127">OUTPUTS</span></span>

### <span data-ttu-id="a218c-128">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="a218c-128">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="a218c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a218c-129">NOTES</span></span>

## <span data-ttu-id="a218c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a218c-130">RELATED LINKS</span></span>

[<span data-ttu-id="a218c-131">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a218c-131">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="a218c-132">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a218c-132">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="a218c-133">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a218c-133">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


