---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2E363D6B-7A05-4C54-B005-68FDBA49A105
online version: ''
schema: 2.0.0
ms.openlocfilehash: cda64b916635d3b46ffb7e8b4170330810a95b5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075942"
---
# <span data-ttu-id="160f8-101">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="160f8-101">Stop-AzureAutomationJob</span></span>

## <span data-ttu-id="160f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="160f8-102">SYNOPSIS</span></span>

<span data-ttu-id="160f8-103">Остановка задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="160f8-103">Stops an Automation job.</span></span>

## <span data-ttu-id="160f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="160f8-104">SYNTAX</span></span>

```
Stop-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="160f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="160f8-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="160f8-106">Командлет **Stop-AzureAutomationJob** останавливает задание службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="160f8-106">The **Stop-AzureAutomationJob** cmdlet stops a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="160f8-107">Укажите выполнение задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="160f8-107">Specify a running automation job.</span></span>

## <span data-ttu-id="160f8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="160f8-108">EXAMPLES</span></span>

### <span data-ttu-id="160f8-109">Пример 1: Остановка задания</span><span class="sxs-lookup"><span data-stu-id="160f8-109">Example 1: Stop a job</span></span>
```
PS C:\> Stop-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="160f8-110">Эта команда останавливает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="160f8-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="160f8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="160f8-111">PARAMETERS</span></span>

### <span data-ttu-id="160f8-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="160f8-112">-AutomationAccountName</span></span>
<span data-ttu-id="160f8-113">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="160f8-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="160f8-114">-ID</span><span class="sxs-lookup"><span data-stu-id="160f8-114">-Id</span></span>
<span data-ttu-id="160f8-115">Указывает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="160f8-115">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="160f8-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="160f8-116">-Profile</span></span>
<span data-ttu-id="160f8-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="160f8-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="160f8-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="160f8-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="160f8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160f8-119">CommonParameters</span></span>
<span data-ttu-id="160f8-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="160f8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160f8-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="160f8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160f8-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="160f8-122">INPUTS</span></span>

## <span data-ttu-id="160f8-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="160f8-123">OUTPUTS</span></span>

## <span data-ttu-id="160f8-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="160f8-124">NOTES</span></span>

## <span data-ttu-id="160f8-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="160f8-125">RELATED LINKS</span></span>

[<span data-ttu-id="160f8-126">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="160f8-126">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="160f8-127">Возобновить — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="160f8-127">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="160f8-128">Приостановить — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="160f8-128">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


