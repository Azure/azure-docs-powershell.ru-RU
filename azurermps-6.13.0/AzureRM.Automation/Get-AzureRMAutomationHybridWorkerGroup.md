---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 8fe4c554fd781d198af6bea784a433c141c2d41d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733919"
---
# <span data-ttu-id="1a96b-101">Get-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="1a96b-101">Get-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="1a96b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a96b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a96b-103">Получает группы гибридных рабочих ролей Runbook.</span><span class="sxs-lookup"><span data-stu-id="1a96b-103">Gets hybrid runbook worker groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a96b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a96b-104">SYNTAX</span></span>

### <span data-ttu-id="1a96b-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a96b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a96b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1a96b-106">ByName</span></span>
```
Get-AzureRmAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a96b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a96b-107">DESCRIPTION</span></span>
<span data-ttu-id="1a96b-108">Командлет **Get-AzureRmAutomationHybridWorkerGroup** получает группы гибридных рабочих ролей Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="1a96b-108">The **Get-AzureRmAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="1a96b-109">Чтобы получить определенную группу, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="1a96b-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="1a96b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a96b-110">EXAMPLES</span></span>

### <span data-ttu-id="1a96b-111">Пример 1: получение всех групп гибридных рабочих ролей Runbook</span><span class="sxs-lookup"><span data-stu-id="1a96b-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="1a96b-112">Эта команда получает все группы гибридных рабочих ролей Runbook в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1a96b-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1a96b-113">Пример 2: получение единственной группы гибридной рабочей роли Runbook</span><span class="sxs-lookup"><span data-stu-id="1a96b-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="1a96b-114">Эта команда получает группу гибридной роли Runbook Worker с именем HybridRunbookWorkerGroup01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1a96b-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1a96b-115">Пример 3: получение сотрудников в гибридной группе Runbook Worker</span><span class="sxs-lookup"><span data-stu-id="1a96b-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="1a96b-116">Эта команда получает гибридные роли Runbook для гибридной группы Runbook Worker с именем HybridRunbookWorkerGroup01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1a96b-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1a96b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a96b-117">PARAMETERS</span></span>

### <span data-ttu-id="1a96b-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a96b-118">-AutomationAccountName</span></span>
<span data-ttu-id="1a96b-119">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1a96b-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="1a96b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a96b-120">-DefaultProfile</span></span>
<span data-ttu-id="1a96b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1a96b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a96b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1a96b-122">-Name</span></span>
<span data-ttu-id="1a96b-123">Указывает имя группы гибридной рабочей роли Runbook.</span><span class="sxs-lookup"><span data-stu-id="1a96b-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="1a96b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a96b-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a96b-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a96b-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1a96b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a96b-126">CommonParameters</span></span>
<span data-ttu-id="1a96b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a96b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a96b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a96b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a96b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a96b-129">INPUTS</span></span>

### <span data-ttu-id="1a96b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1a96b-130">System.String</span></span>
<span data-ttu-id="1a96b-131">Параметры: Name (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1a96b-131">Parameters: Name (ByValue)</span></span>

## <span data-ttu-id="1a96b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a96b-132">OUTPUTS</span></span>

### <span data-ttu-id="1a96b-133">Microsoft. Azure. Commands. Automation. Model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="1a96b-133">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="1a96b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a96b-134">NOTES</span></span>

## <span data-ttu-id="1a96b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a96b-135">RELATED LINKS</span></span>
