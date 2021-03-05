---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 89c1b96744ce67765bed53f850e21a457ead4b6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996974"
---
# <span data-ttu-id="cc25f-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="cc25f-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="cc25f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc25f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc25f-103">Возвращает гибридные группы сотрудников runbook.</span><span class="sxs-lookup"><span data-stu-id="cc25f-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="cc25f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc25f-104">SYNTAX</span></span>

### <span data-ttu-id="cc25f-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc25f-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc25f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cc25f-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc25f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc25f-107">DESCRIPTION</span></span>
<span data-ttu-id="cc25f-108">Командлет **Get-AzAutomationHybridWorkerGroup** получает группы сотрудников гибридной книги автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="cc25f-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="cc25f-109">Чтобы получить конкретную группу, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="cc25f-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="cc25f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc25f-110">EXAMPLES</span></span>

### <span data-ttu-id="cc25f-111">Пример 1. Все гибридные группы сотрудников runbook</span><span class="sxs-lookup"><span data-stu-id="cc25f-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="cc25f-112">Эта команда возвращает все гибридные группы рабочих книг в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cc25f-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cc25f-113">Пример 2. Получить одну группу сотрудников гибридной рабочей книги</span><span class="sxs-lookup"><span data-stu-id="cc25f-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="cc25f-114">Эта команда возвращает гибридную группу рабочих книг с именем HybridRunbookWorkerGroup01 в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cc25f-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cc25f-115">Пример 3. Группу рабочих в гибридной рабочей книге</span><span class="sxs-lookup"><span data-stu-id="cc25f-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="cc25f-116">Эта команда возвращает сотрудников гибридной рабочей книги в группу рабочих гибридной книги с именем HybridRunbookWorkerGroup01 в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cc25f-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cc25f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc25f-117">PARAMETERS</span></span>

### <span data-ttu-id="cc25f-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cc25f-118">-AutomationAccountName</span></span>
<span data-ttu-id="cc25f-119">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="cc25f-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="cc25f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc25f-120">-DefaultProfile</span></span>
<span data-ttu-id="cc25f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cc25f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc25f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cc25f-122">-Name</span></span>
<span data-ttu-id="cc25f-123">Имя группы рабочих в гибридной рабочей книге.</span><span class="sxs-lookup"><span data-stu-id="cc25f-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc25f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc25f-124">-ResourceGroupName</span></span>
<span data-ttu-id="cc25f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc25f-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cc25f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc25f-126">CommonParameters</span></span>
<span data-ttu-id="cc25f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc25f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc25f-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc25f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc25f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc25f-129">INPUTS</span></span>

### <span data-ttu-id="cc25f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cc25f-130">System.String</span></span>

## <span data-ttu-id="cc25f-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc25f-131">OUTPUTS</span></span>

### <span data-ttu-id="cc25f-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="cc25f-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="cc25f-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc25f-133">NOTES</span></span>

## <span data-ttu-id="cc25f-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc25f-134">RELATED LINKS</span></span>
