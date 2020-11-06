---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
ms.openlocfilehash: 3e7affd09e8c24c1d3c1759e78ea09a0c849ff32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567312"
---
# <span data-ttu-id="6abf6-101">Get-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="6abf6-101">Get-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="6abf6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6abf6-102">SYNOPSIS</span></span>
<span data-ttu-id="6abf6-103">Получает список элементов управления источником автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6abf6-103">Gets a list of Azure Automation source controls.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6abf6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6abf6-104">SYNTAX</span></span>

### <span data-ttu-id="6abf6-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6abf6-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6abf6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6abf6-106">ByName</span></span>
```
Get-AzureRmAutomationSourceControl -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6abf6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6abf6-107">DESCRIPTION</span></span>
<span data-ttu-id="6abf6-108">Командлет Get-AzureRmAutomationSourceControl получает элементы управления источником автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6abf6-108">The Get-AzureRmAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="6abf6-109">Чтобы получить определенную систему управления версиями, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="6abf6-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="6abf6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6abf6-110">EXAMPLES</span></span>

### <span data-ttu-id="6abf6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6abf6-111">Example 1</span></span>
<span data-ttu-id="6abf6-112">Эта команда получает элемент управления источником автоматизации с именем VSTSNative в учетной записи с именем devAccount.</span><span class="sxs-lookup"><span data-stu-id="6abf6-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="6abf6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6abf6-113">PARAMETERS</span></span>

### <span data-ttu-id="6abf6-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6abf6-114">-AutomationAccountName</span></span>
<span data-ttu-id="6abf6-115">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6abf6-115">The automation account name.</span></span>

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

### <span data-ttu-id="6abf6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6abf6-116">-DefaultProfile</span></span>
<span data-ttu-id="6abf6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6abf6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6abf6-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6abf6-118">-Name</span></span>
<span data-ttu-id="6abf6-119">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6abf6-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6abf6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6abf6-120">-ResourceGroupName</span></span>
<span data-ttu-id="6abf6-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6abf6-121">The resource group name.</span></span>

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

### <span data-ttu-id="6abf6-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="6abf6-122">-SourceType</span></span>
<span data-ttu-id="6abf6-123">Тип системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="6abf6-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6abf6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6abf6-124">CommonParameters</span></span>
<span data-ttu-id="6abf6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6abf6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6abf6-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6abf6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6abf6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6abf6-127">INPUTS</span></span>

### <span data-ttu-id="6abf6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6abf6-128">System.String</span></span>

## <span data-ttu-id="6abf6-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6abf6-129">OUTPUTS</span></span>

### <span data-ttu-id="6abf6-130">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="6abf6-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="6abf6-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6abf6-131">NOTES</span></span>

## <span data-ttu-id="6abf6-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6abf6-132">RELATED LINKS</span></span>
