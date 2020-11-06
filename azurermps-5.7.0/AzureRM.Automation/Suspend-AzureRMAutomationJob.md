---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/suspend-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: 05747721219610524e0a245df5b5a67e8e69b483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567473"
---
# <span data-ttu-id="744f7-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="744f7-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="744f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="744f7-102">SYNOPSIS</span></span>
<span data-ttu-id="744f7-103">Приостанавливает задание автоматизации.</span><span class="sxs-lookup"><span data-stu-id="744f7-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="744f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="744f7-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="744f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="744f7-105">DESCRIPTION</span></span>
<span data-ttu-id="744f7-106">Командлет **Suspend-AzureRmAutomationJob** приостанавливает задание службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="744f7-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="744f7-107">Укажите выполнение задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="744f7-107">Specify a running Automation job.</span></span>

<span data-ttu-id="744f7-108">Чтобы возобновить приостановленное задание, используйте командлет Resume-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="744f7-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="744f7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="744f7-109">EXAMPLES</span></span>

### <span data-ttu-id="744f7-110">Пример 1: Приостановка задания</span><span class="sxs-lookup"><span data-stu-id="744f7-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="744f7-111">Эта команда приостанавливает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="744f7-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="744f7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="744f7-112">PARAMETERS</span></span>

### <span data-ttu-id="744f7-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="744f7-113">-AutomationAccountName</span></span>
<span data-ttu-id="744f7-114">Указывает имя учетной записи автоматизации, в которой этот командлет приостанавливает задание.</span><span class="sxs-lookup"><span data-stu-id="744f7-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744f7-115">-DefaultProfile</span></span>
<span data-ttu-id="744f7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="744f7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744f7-117">-ID</span><span class="sxs-lookup"><span data-stu-id="744f7-117">-Id</span></span>
<span data-ttu-id="744f7-118">Указывает идентификатор задания, приостановки которого является этот командлет.</span><span class="sxs-lookup"><span data-stu-id="744f7-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744f7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744f7-119">-ResourceGroupName</span></span>
<span data-ttu-id="744f7-120">Указывает идентификатор задания, приостановки которого является этот командлет.</span><span class="sxs-lookup"><span data-stu-id="744f7-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744f7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744f7-121">CommonParameters</span></span>
<span data-ttu-id="744f7-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="744f7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744f7-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="744f7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744f7-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="744f7-124">INPUTS</span></span>

### <span data-ttu-id="744f7-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="744f7-125">None</span></span>
<span data-ttu-id="744f7-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="744f7-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="744f7-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="744f7-127">OUTPUTS</span></span>

## <span data-ttu-id="744f7-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="744f7-128">NOTES</span></span>

## <span data-ttu-id="744f7-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="744f7-129">RELATED LINKS</span></span>

[<span data-ttu-id="744f7-130">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="744f7-130">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="744f7-131">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="744f7-131">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="744f7-132">Возобновить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="744f7-132">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="744f7-133">Остановить-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="744f7-133">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


