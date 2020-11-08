---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CE04DEE6-28AE-43A3-A8DE-98AC0A57E575
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1c2d9a3aa53cb8efd2924f24aa80db2c7fd07fea
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075759"
---
# <span data-ttu-id="25944-101">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="25944-101">Suspend-AzureAutomationJob</span></span>

## <span data-ttu-id="25944-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25944-102">SYNOPSIS</span></span>

<span data-ttu-id="25944-103">Приостанавливает задание автоматизации.</span><span class="sxs-lookup"><span data-stu-id="25944-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="25944-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25944-104">SYNTAX</span></span>

```
Suspend-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="25944-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25944-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="25944-106">Командлет **Suspend-AzureAutomationJob** приостанавливает задание службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25944-106">The **Suspend-AzureAutomationJob** cmdlet suspends a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="25944-107">Укажите выполнение задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="25944-107">Specify a running Automation job.</span></span>

<span data-ttu-id="25944-108">Чтобы возобновить приостановленное задание, используйте командлет **Resume-AzureAutomationJob** .</span><span class="sxs-lookup"><span data-stu-id="25944-108">To resume a suspended job, use the **Resume-AzureAutomationJob** cmdlet.</span></span>

## <span data-ttu-id="25944-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25944-109">EXAMPLES</span></span>

### <span data-ttu-id="25944-110">Пример 1: Приостановка задания</span><span class="sxs-lookup"><span data-stu-id="25944-110">Example 1: Suspend a job</span></span>
```
PS C:\> Suspend-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="25944-111">Эта команда приостанавливает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="25944-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="25944-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25944-112">PARAMETERS</span></span>

### <span data-ttu-id="25944-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="25944-113">-AutomationAccountName</span></span>
<span data-ttu-id="25944-114">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="25944-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="25944-115">-ID</span><span class="sxs-lookup"><span data-stu-id="25944-115">-Id</span></span>
<span data-ttu-id="25944-116">Указывает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="25944-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="25944-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="25944-117">-Profile</span></span>
<span data-ttu-id="25944-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="25944-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25944-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25944-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25944-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25944-120">CommonParameters</span></span>
<span data-ttu-id="25944-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25944-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25944-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25944-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25944-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25944-123">INPUTS</span></span>

## <span data-ttu-id="25944-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25944-124">OUTPUTS</span></span>

## <span data-ttu-id="25944-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="25944-125">NOTES</span></span>

## <span data-ttu-id="25944-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25944-126">RELATED LINKS</span></span>

[<span data-ttu-id="25944-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="25944-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="25944-128">Возобновить — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="25944-128">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="25944-129">Остановить-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="25944-129">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)


