---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235225"
---
# <span data-ttu-id="a74e0-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="a74e0-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="a74e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a74e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a74e0-103">Получает список исходных элементов управления автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="a74e0-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="a74e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a74e0-104">SYNTAX</span></span>

### <span data-ttu-id="a74e0-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a74e0-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a74e0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a74e0-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a74e0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a74e0-107">DESCRIPTION</span></span>
<span data-ttu-id="a74e0-108">Этот Get-AzAutomationSourceControl получает исходные элементы управления автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a74e0-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="a74e0-109">Чтобы получить определенный исходный контроль, укажите его имя.</span><span class="sxs-lookup"><span data-stu-id="a74e0-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="a74e0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a74e0-110">EXAMPLES</span></span>

### <span data-ttu-id="a74e0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a74e0-111">Example 1</span></span>
<span data-ttu-id="a74e0-112">Эта команда получает источник автоматизации с именем VSTSNative в учетной записи devAccount.</span><span class="sxs-lookup"><span data-stu-id="a74e0-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="a74e0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a74e0-113">PARAMETERS</span></span>

### <span data-ttu-id="a74e0-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a74e0-114">-AutomationAccountName</span></span>
<span data-ttu-id="a74e0-115">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a74e0-115">The automation account name.</span></span>

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

### <span data-ttu-id="a74e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74e0-116">-DefaultProfile</span></span>
<span data-ttu-id="a74e0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a74e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a74e0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a74e0-118">-Name</span></span>
<span data-ttu-id="a74e0-119">Имя источника.</span><span class="sxs-lookup"><span data-stu-id="a74e0-119">The source control name.</span></span>

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

### <span data-ttu-id="a74e0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a74e0-120">-ResourceGroupName</span></span>
<span data-ttu-id="a74e0-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a74e0-121">The resource group name.</span></span>

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

### <span data-ttu-id="a74e0-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="a74e0-122">-SourceType</span></span>
<span data-ttu-id="a74e0-123">Исходный тип управления.</span><span class="sxs-lookup"><span data-stu-id="a74e0-123">The source control type.</span></span>

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

### <span data-ttu-id="a74e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74e0-124">CommonParameters</span></span>
<span data-ttu-id="a74e0-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a74e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74e0-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a74e0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74e0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a74e0-127">INPUTS</span></span>

### <span data-ttu-id="a74e0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a74e0-128">System.String</span></span>

## <span data-ttu-id="a74e0-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a74e0-129">OUTPUTS</span></span>

### <span data-ttu-id="a74e0-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="a74e0-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="a74e0-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a74e0-131">NOTES</span></span>

## <span data-ttu-id="a74e0-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a74e0-132">RELATED LINKS</span></span>
