---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 66740917-E8BB-44ED-9CBB-9825BD1840E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b049d770dbcee8b7cea56dbadbf7d4071c344cc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076362"
---
# <span data-ttu-id="df618-101">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="df618-101">Get-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="df618-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df618-102">SYNOPSIS</span></span>

<span data-ttu-id="df618-103">Получает определение Runbook.</span><span class="sxs-lookup"><span data-stu-id="df618-103">Gets a runbook definition.</span></span>

## <span data-ttu-id="df618-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df618-104">SYNTAX</span></span>

```
Get-AzureAutomationRunbookDefinition -Name <String> [-Slot <String>] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="df618-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df618-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="df618-106">Командлет **Get-AzureAutomationRunbookDefinition** получает определение черновика, опубликованное определение или оба определения Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="df618-106">The **Get-AzureAutomationRunbookDefinition** cmdlet gets the draft definition, the published definition, or both definitions of an Azure Automation runbook.</span></span>
<span data-ttu-id="df618-107">По умолчанию возвращается опубликованная версия.</span><span class="sxs-lookup"><span data-stu-id="df618-107">By default, the published version is returned.</span></span>

## <span data-ttu-id="df618-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df618-108">EXAMPLES</span></span>

### <span data-ttu-id="df618-109">Пример 1: получение определения Runbook</span><span class="sxs-lookup"><span data-stu-id="df618-109">Example 1: Get a runbook definition</span></span>
```
PS C:\> Get-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "RunbookDef01" -Slot "Published"
```

<span data-ttu-id="df618-110">Эта команда получает определение опубликованного Runbook модуля Runbook с именем RunbookDef01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="df618-110">This command gets the published runbook definition of the runbook named RunbookDef01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="df618-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df618-111">PARAMETERS</span></span>

### <span data-ttu-id="df618-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df618-112">-AutomationAccountName</span></span>
<span data-ttu-id="df618-113">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="df618-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="df618-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="df618-114">-Name</span></span>
<span data-ttu-id="df618-115">Указывает имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="df618-115">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df618-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="df618-116">-Profile</span></span>
<span data-ttu-id="df618-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="df618-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="df618-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="df618-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="df618-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="df618-119">-Slot</span></span>
<span data-ttu-id="df618-120">Задает ячейку.</span><span class="sxs-lookup"><span data-stu-id="df618-120">Specifies the slot.</span></span>
<span data-ttu-id="df618-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="df618-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="df618-122">Проверяем</span><span class="sxs-lookup"><span data-stu-id="df618-122">Draft</span></span>
- <span data-ttu-id="df618-123">Отменить</span><span class="sxs-lookup"><span data-stu-id="df618-123">Published</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df618-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df618-124">CommonParameters</span></span>
<span data-ttu-id="df618-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df618-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df618-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df618-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df618-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df618-127">INPUTS</span></span>

## <span data-ttu-id="df618-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df618-128">OUTPUTS</span></span>

## <span data-ttu-id="df618-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="df618-129">NOTES</span></span>

## <span data-ttu-id="df618-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df618-130">RELATED LINKS</span></span>

[<span data-ttu-id="df618-131">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="df618-131">Set-AzureAutomationRunbookDefinition</span></span>](./Set-AzureAutomationRunbookDefinition.md)


