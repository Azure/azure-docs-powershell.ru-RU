---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316207"
---
# <span data-ttu-id="165e5-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="165e5-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="165e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="165e5-102">SYNOPSIS</span></span>
<span data-ttu-id="165e5-103">Остановка задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="165e5-103">Stops an Automation job.</span></span>

## <span data-ttu-id="165e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="165e5-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="165e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="165e5-105">DESCRIPTION</span></span>
<span data-ttu-id="165e5-106">Командлет **Stop-AzAutomationJob** останавливает задание службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="165e5-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="165e5-107">Укажите выполнение задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="165e5-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="165e5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="165e5-108">EXAMPLES</span></span>

### <span data-ttu-id="165e5-109">Пример 1: Остановка задания</span><span class="sxs-lookup"><span data-stu-id="165e5-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="165e5-110">Эта команда останавливает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="165e5-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="165e5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="165e5-111">PARAMETERS</span></span>

### <span data-ttu-id="165e5-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="165e5-112">-AutomationAccountName</span></span>
<span data-ttu-id="165e5-113">Указывает имя учетной записи автоматизации, в которой этот командлет останавливает задание.</span><span class="sxs-lookup"><span data-stu-id="165e5-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="165e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="165e5-114">-DefaultProfile</span></span>
<span data-ttu-id="165e5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="165e5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165e5-116">-ID</span><span class="sxs-lookup"><span data-stu-id="165e5-116">-Id</span></span>
<span data-ttu-id="165e5-117">Указывает идентификатор задания, которое останавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="165e5-117">Specifies the ID of a job that this cmdlet stops.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="165e5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="165e5-118">-ResourceGroupName</span></span>
<span data-ttu-id="165e5-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="165e5-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="165e5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="165e5-120">CommonParameters</span></span>
<span data-ttu-id="165e5-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="165e5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="165e5-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="165e5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="165e5-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="165e5-123">INPUTS</span></span>

### <span data-ttu-id="165e5-124">System. GUID</span><span class="sxs-lookup"><span data-stu-id="165e5-124">System.Guid</span></span>

### <span data-ttu-id="165e5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="165e5-125">System.String</span></span>

## <span data-ttu-id="165e5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="165e5-126">OUTPUTS</span></span>

### <span data-ttu-id="165e5-127">System. void</span><span class="sxs-lookup"><span data-stu-id="165e5-127">System.Void</span></span>

## <span data-ttu-id="165e5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="165e5-128">NOTES</span></span>

## <span data-ttu-id="165e5-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="165e5-129">RELATED LINKS</span></span>

[<span data-ttu-id="165e5-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="165e5-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="165e5-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="165e5-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="165e5-132">Возобновить — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="165e5-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="165e5-133">Приостановить — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="165e5-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


