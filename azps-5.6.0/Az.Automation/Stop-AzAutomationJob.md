---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: c0169a799db59a66f0d44191e58dae3760ec4128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990534"
---
# <span data-ttu-id="5910a-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5910a-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="5910a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5910a-102">SYNOPSIS</span></span>
<span data-ttu-id="5910a-103">Остановка задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5910a-103">Stops an Automation job.</span></span>

## <span data-ttu-id="5910a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5910a-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5910a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5910a-105">DESCRIPTION</span></span>
<span data-ttu-id="5910a-106">При **настройке Stop-AzAutomationJob** задание автоматизации Azure прекращается.</span><span class="sxs-lookup"><span data-stu-id="5910a-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="5910a-107">Задание запускаемой автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5910a-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="5910a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5910a-108">EXAMPLES</span></span>

### <span data-ttu-id="5910a-109">Пример 1. Остановка задания</span><span class="sxs-lookup"><span data-stu-id="5910a-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5910a-110">Эта команда останавливает задание с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="5910a-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="5910a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5910a-111">PARAMETERS</span></span>

### <span data-ttu-id="5910a-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5910a-112">-AutomationAccountName</span></span>
<span data-ttu-id="5910a-113">Указывает имя учетной записи автоматизации, в которой этот cmdlet останавливает задание.</span><span class="sxs-lookup"><span data-stu-id="5910a-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="5910a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5910a-114">-DefaultProfile</span></span>
<span data-ttu-id="5910a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5910a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5910a-116">-Id</span><span class="sxs-lookup"><span data-stu-id="5910a-116">-Id</span></span>
<span data-ttu-id="5910a-117">Определяет код задания, которое останавливает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5910a-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="5910a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5910a-118">-ResourceGroupName</span></span>
<span data-ttu-id="5910a-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5910a-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5910a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5910a-120">CommonParameters</span></span>
<span data-ttu-id="5910a-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5910a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5910a-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5910a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5910a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5910a-123">INPUTS</span></span>

### <span data-ttu-id="5910a-124">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5910a-124">System.Guid</span></span>

### <span data-ttu-id="5910a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="5910a-125">System.String</span></span>

## <span data-ttu-id="5910a-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5910a-126">OUTPUTS</span></span>

### <span data-ttu-id="5910a-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="5910a-127">System.Void</span></span>

## <span data-ttu-id="5910a-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5910a-128">NOTES</span></span>

## <span data-ttu-id="5910a-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5910a-129">RELATED LINKS</span></span>

[<span data-ttu-id="5910a-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5910a-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="5910a-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="5910a-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="5910a-132">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5910a-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="5910a-133">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5910a-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


