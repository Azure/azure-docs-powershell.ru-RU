---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 5E5B8102-9E7E-4128-8160-3AA3803B118F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ff0831e6458a9d587b508acfa2e09948d81d87e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075462"
---
# <span data-ttu-id="3532d-101">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3532d-101">Resume-AzureAutomationJob</span></span>

## <span data-ttu-id="3532d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3532d-102">SYNOPSIS</span></span>

<span data-ttu-id="3532d-103">Возобновление приостановленного задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3532d-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="3532d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3532d-104">SYNTAX</span></span>

```
Resume-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3532d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3532d-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3532d-106">Командлет **Resume-AzureAutomationJob** возобновляет приостановленное задание службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3532d-106">The **Resume-AzureAutomationJob** cmdlet resumes a suspended Microsoft Azure Automation job.</span></span>
<span data-ttu-id="3532d-107">Используйте параметр *ID* , чтобы указать приостановленное задание.</span><span class="sxs-lookup"><span data-stu-id="3532d-107">Use the *Id* parameter to specify the suspended job.</span></span>

<span data-ttu-id="3532d-108">Чтобы приостановить задание, используйте командлет Suspend-AzureAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="3532d-108">To suspend a job, use the Suspend-AzureAutomationJob cmdlet.</span></span>

## <span data-ttu-id="3532d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3532d-109">EXAMPLES</span></span>

### <span data-ttu-id="3532d-110">Пример 1: возобновление приостановленного задания</span><span class="sxs-lookup"><span data-stu-id="3532d-110">Example 1: Resume a suspended job</span></span>
```
PS C:\> Resume-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="3532d-111">Эта команда возобновляет задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="3532d-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="3532d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3532d-112">PARAMETERS</span></span>

### <span data-ttu-id="3532d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3532d-113">-AutomationAccountName</span></span>
<span data-ttu-id="3532d-114">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3532d-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="3532d-115">-ID</span><span class="sxs-lookup"><span data-stu-id="3532d-115">-Id</span></span>
<span data-ttu-id="3532d-116">Указывает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="3532d-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="3532d-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="3532d-117">-Profile</span></span>
<span data-ttu-id="3532d-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3532d-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3532d-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3532d-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3532d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3532d-120">CommonParameters</span></span>
<span data-ttu-id="3532d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3532d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3532d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3532d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3532d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3532d-123">INPUTS</span></span>

## <span data-ttu-id="3532d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3532d-124">OUTPUTS</span></span>

## <span data-ttu-id="3532d-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="3532d-125">NOTES</span></span>

## <span data-ttu-id="3532d-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3532d-126">RELATED LINKS</span></span>

[<span data-ttu-id="3532d-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3532d-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="3532d-128">Остановить-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3532d-128">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="3532d-129">Приостановить — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3532d-129">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


