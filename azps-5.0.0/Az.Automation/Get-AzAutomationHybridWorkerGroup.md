---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246434"
---
# <span data-ttu-id="8ae6f-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="8ae6f-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="8ae6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ae6f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae6f-103">Получает группы гибридных рабочих ролей Runbook.</span><span class="sxs-lookup"><span data-stu-id="8ae6f-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="8ae6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ae6f-104">SYNTAX</span></span>

### <span data-ttu-id="8ae6f-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ae6f-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ae6f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8ae6f-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ae6f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ae6f-107">DESCRIPTION</span></span>
<span data-ttu-id="8ae6f-108">Командлет **Get-AzAutomationHybridWorkerGroup** получает группы гибридных рабочих ролей Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="8ae6f-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="8ae6f-109">Чтобы получить определенную группу, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="8ae6f-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="8ae6f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ae6f-110">EXAMPLES</span></span>

### <span data-ttu-id="8ae6f-111">Пример 1: получение всех групп гибридных рабочих ролей Runbook</span><span class="sxs-lookup"><span data-stu-id="8ae6f-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8ae6f-112">Эта команда получает все группы гибридных рабочих ролей Runbook в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8ae6f-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8ae6f-113">Пример 2: получение единственной группы гибридной рабочей роли Runbook</span><span class="sxs-lookup"><span data-stu-id="8ae6f-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="8ae6f-114">Эта команда получает группу гибридной роли Runbook Worker с именем HybridRunbookWorkerGroup01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8ae6f-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8ae6f-115">Пример 3: получение сотрудников в гибридной группе Runbook Worker</span><span class="sxs-lookup"><span data-stu-id="8ae6f-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="8ae6f-116">Эта команда получает гибридные роли Runbook для гибридной группы Runbook Worker с именем HybridRunbookWorkerGroup01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8ae6f-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8ae6f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ae6f-117">PARAMETERS</span></span>

### <span data-ttu-id="8ae6f-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8ae6f-118">-AutomationAccountName</span></span>
<span data-ttu-id="8ae6f-119">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8ae6f-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="8ae6f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae6f-120">-DefaultProfile</span></span>
<span data-ttu-id="8ae6f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8ae6f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ae6f-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ae6f-122">-Name</span></span>
<span data-ttu-id="8ae6f-123">Указывает имя группы гибридной рабочей роли Runbook.</span><span class="sxs-lookup"><span data-stu-id="8ae6f-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="8ae6f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae6f-124">-ResourceGroupName</span></span>
<span data-ttu-id="8ae6f-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ae6f-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8ae6f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae6f-126">CommonParameters</span></span>
<span data-ttu-id="8ae6f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ae6f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae6f-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ae6f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae6f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ae6f-129">INPUTS</span></span>

### <span data-ttu-id="8ae6f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8ae6f-130">System.String</span></span>

## <span data-ttu-id="8ae6f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ae6f-131">OUTPUTS</span></span>

### <span data-ttu-id="8ae6f-132">Microsoft. Azure. Commands. Automation. Model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="8ae6f-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="8ae6f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ae6f-133">NOTES</span></span>

## <span data-ttu-id="8ae6f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ae6f-134">RELATED LINKS</span></span>
