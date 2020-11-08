---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076070"
---
# <span data-ttu-id="02505-101">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="02505-101">Set-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="02505-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02505-102">SYNOPSIS</span></span>

<span data-ttu-id="02505-103">Обновляет определение черновика Runbook.</span><span class="sxs-lookup"><span data-stu-id="02505-103">Updates the draft definition of a runbook.</span></span>

## <span data-ttu-id="02505-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02505-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="02505-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02505-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="02505-106">Командлет **Set-AzureAutomationRunbookDefinition** обновляет определение черновика Runbook Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="02505-106">The **Set-AzureAutomationRunbookDefinition** cmdlet updates the draft definition of a Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="02505-107">Укажите файл сценария Windows PowerShell (PS1), содержащий Runbook, который станет черновиком Runbook.</span><span class="sxs-lookup"><span data-stu-id="02505-107">Specify a Windows PowerShell script (.ps1) file that contains a runbook that becomes the draft runbook.</span></span>

<span data-ttu-id="02505-108">Если определение черновика уже существует, используйте параметр *overwrite* , чтобы принудительно перезаписать существующий черновик в командлете.</span><span class="sxs-lookup"><span data-stu-id="02505-108">If a draft definition already exists, use the *Overwrite* parameter to force the cmdlet to overwrite the existing draft.</span></span>

## <span data-ttu-id="02505-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02505-109">EXAMPLES</span></span>

### <span data-ttu-id="02505-110">Пример 1: переопределение существующего определения черновика Runbook</span><span class="sxs-lookup"><span data-stu-id="02505-110">Example 1: Overwrite an existing draft definition of a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

<span data-ttu-id="02505-111">Эта команда перезапишет существующее определение черновика Runbook.</span><span class="sxs-lookup"><span data-stu-id="02505-111">This command overwrites the existing draft definition of a runbook.</span></span>

## <span data-ttu-id="02505-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02505-112">PARAMETERS</span></span>

### <span data-ttu-id="02505-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="02505-113">-AutomationAccountName</span></span>
<span data-ttu-id="02505-114">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="02505-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="02505-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02505-115">-Name</span></span>
<span data-ttu-id="02505-116">Задает имя.</span><span class="sxs-lookup"><span data-stu-id="02505-116">Specifies a name.</span></span>

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

### <span data-ttu-id="02505-117">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="02505-117">-Overwrite</span></span>
<span data-ttu-id="02505-118">Указывает, нужно ли перезаписывать существующее определение черновика.</span><span class="sxs-lookup"><span data-stu-id="02505-118">Indicates whether to overwrite an existing draft definition.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02505-119">-Path</span><span class="sxs-lookup"><span data-stu-id="02505-119">-Path</span></span>
<span data-ttu-id="02505-120">Указывает путь к Runbook.</span><span class="sxs-lookup"><span data-stu-id="02505-120">Specifies the path to a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02505-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="02505-121">-Profile</span></span>
<span data-ttu-id="02505-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="02505-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02505-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="02505-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02505-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02505-124">CommonParameters</span></span>
<span data-ttu-id="02505-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02505-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02505-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02505-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02505-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02505-127">INPUTS</span></span>

## <span data-ttu-id="02505-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02505-128">OUTPUTS</span></span>

### <span data-ttu-id="02505-129">Microsoft. Azure. Commands. Automation. Model. RunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="02505-129">Microsoft.Azure.Commands.Automation.Model.RunbookDefinition</span></span>

## <span data-ttu-id="02505-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="02505-130">NOTES</span></span>

## <span data-ttu-id="02505-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02505-131">RELATED LINKS</span></span>

[<span data-ttu-id="02505-132">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="02505-132">Get-AzureAutomationRunbookDefinition</span></span>](./Get-AzureAutomationRunbookDefinition.md)


