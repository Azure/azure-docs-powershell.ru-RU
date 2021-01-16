---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418695"
---
# <span data-ttu-id="82121-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="82121-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="82121-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82121-102">SYNOPSIS</span></span>
<span data-ttu-id="82121-103">Возвращает гибридные группы сотрудников runbook.</span><span class="sxs-lookup"><span data-stu-id="82121-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="82121-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82121-104">SYNTAX</span></span>

### <span data-ttu-id="82121-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82121-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82121-106">ByName</span><span class="sxs-lookup"><span data-stu-id="82121-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82121-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82121-107">DESCRIPTION</span></span>
<span data-ttu-id="82121-108">Командлет **Get-AzAutomationHybridWorkerGroup** получает группы сотрудников гибридной книги автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="82121-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="82121-109">Чтобы получить конкретную группу, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="82121-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="82121-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82121-110">EXAMPLES</span></span>

### <span data-ttu-id="82121-111">Пример 1. Получить все гибридные группы сотрудников runbook</span><span class="sxs-lookup"><span data-stu-id="82121-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="82121-112">Эта команда возвращает все гибридные группы рабочих книг в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82121-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="82121-113">Пример 2. Получить одну группу рабочих в гибридной рабочей книге</span><span class="sxs-lookup"><span data-stu-id="82121-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="82121-114">Эта команда возвращает гибридную группу рабочих книг с именем HybridRunbookWorkerGroup01 в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82121-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="82121-115">Пример 3. Группу рабочих в гибридной рабочей книге</span><span class="sxs-lookup"><span data-stu-id="82121-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="82121-116">Эта команда возвращает сотрудников гибридной рабочей книги в группу рабочих гибридной книги с именем HybridRunbookWorkerGroup01 в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82121-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="82121-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82121-117">PARAMETERS</span></span>

### <span data-ttu-id="82121-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="82121-118">-AutomationAccountName</span></span>
<span data-ttu-id="82121-119">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="82121-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="82121-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82121-120">-DefaultProfile</span></span>
<span data-ttu-id="82121-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82121-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82121-122">-Name</span><span class="sxs-lookup"><span data-stu-id="82121-122">-Name</span></span>
<span data-ttu-id="82121-123">Имя группы рабочих в гибридной рабочей книге.</span><span class="sxs-lookup"><span data-stu-id="82121-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="82121-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82121-124">-ResourceGroupName</span></span>
<span data-ttu-id="82121-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82121-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="82121-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82121-126">CommonParameters</span></span>
<span data-ttu-id="82121-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82121-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82121-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82121-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82121-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82121-129">INPUTS</span></span>

### <span data-ttu-id="82121-130">System.String</span><span class="sxs-lookup"><span data-stu-id="82121-130">System.String</span></span>

## <span data-ttu-id="82121-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82121-131">OUTPUTS</span></span>

### <span data-ttu-id="82121-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="82121-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="82121-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82121-133">NOTES</span></span>

## <span data-ttu-id="82121-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82121-134">RELATED LINKS</span></span>
