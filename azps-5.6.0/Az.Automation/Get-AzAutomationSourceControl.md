---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 051eee1c191662e6ca4eb56e34088af651ea69f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014163"
---
# <span data-ttu-id="873b6-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="873b6-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="873b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="873b6-102">SYNOPSIS</span></span>
<span data-ttu-id="873b6-103">Получает список исходных элементов управления автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="873b6-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="873b6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="873b6-104">SYNTAX</span></span>

### <span data-ttu-id="873b6-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="873b6-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="873b6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="873b6-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="873b6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="873b6-107">DESCRIPTION</span></span>
<span data-ttu-id="873b6-108">Этот Get-AzAutomationSourceControl получает исходные элементы управления автоматизации.</span><span class="sxs-lookup"><span data-stu-id="873b6-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="873b6-109">Чтобы получить определенный исходный контроль, укажите его имя.</span><span class="sxs-lookup"><span data-stu-id="873b6-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="873b6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="873b6-110">EXAMPLES</span></span>

### <span data-ttu-id="873b6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="873b6-111">Example 1</span></span>
<span data-ttu-id="873b6-112">Эта команда получает источник автоматизации с именем VSTSNative в учетной записи devAccount.</span><span class="sxs-lookup"><span data-stu-id="873b6-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="873b6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="873b6-113">PARAMETERS</span></span>

### <span data-ttu-id="873b6-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="873b6-114">-AutomationAccountName</span></span>
<span data-ttu-id="873b6-115">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="873b6-115">The automation account name.</span></span>

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

### <span data-ttu-id="873b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="873b6-116">-DefaultProfile</span></span>
<span data-ttu-id="873b6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="873b6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="873b6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="873b6-118">-Name</span></span>
<span data-ttu-id="873b6-119">Имя источника.</span><span class="sxs-lookup"><span data-stu-id="873b6-119">The source control name.</span></span>

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

### <span data-ttu-id="873b6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="873b6-120">-ResourceGroupName</span></span>
<span data-ttu-id="873b6-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="873b6-121">The resource group name.</span></span>

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

### <span data-ttu-id="873b6-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="873b6-122">-SourceType</span></span>
<span data-ttu-id="873b6-123">Тип управления "Источник".</span><span class="sxs-lookup"><span data-stu-id="873b6-123">The source control type.</span></span>

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

### <span data-ttu-id="873b6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="873b6-124">CommonParameters</span></span>
<span data-ttu-id="873b6-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="873b6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="873b6-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="873b6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="873b6-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="873b6-127">INPUTS</span></span>

### <span data-ttu-id="873b6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="873b6-128">System.String</span></span>

## <span data-ttu-id="873b6-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="873b6-129">OUTPUTS</span></span>

### <span data-ttu-id="873b6-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="873b6-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="873b6-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="873b6-131">NOTES</span></span>

## <span data-ttu-id="873b6-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="873b6-132">RELATED LINKS</span></span>
