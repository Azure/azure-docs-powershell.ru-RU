---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242644"
---
# <span data-ttu-id="b742a-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="b742a-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="b742a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b742a-102">SYNOPSIS</span></span>
<span data-ttu-id="b742a-103">Получает список элементов управления источником автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="b742a-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="b742a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b742a-104">SYNTAX</span></span>

### <span data-ttu-id="b742a-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b742a-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b742a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b742a-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b742a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b742a-107">DESCRIPTION</span></span>
<span data-ttu-id="b742a-108">Командлет Get-AzAutomationSourceControl получает элементы управления источником автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b742a-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="b742a-109">Чтобы получить определенную систему управления версиями, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="b742a-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="b742a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b742a-110">EXAMPLES</span></span>

### <span data-ttu-id="b742a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b742a-111">Example 1</span></span>
<span data-ttu-id="b742a-112">Эта команда получает элемент управления источником автоматизации с именем VSTSNative в учетной записи с именем devAccount.</span><span class="sxs-lookup"><span data-stu-id="b742a-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="b742a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b742a-113">PARAMETERS</span></span>

### <span data-ttu-id="b742a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b742a-114">-AutomationAccountName</span></span>
<span data-ttu-id="b742a-115">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b742a-115">The automation account name.</span></span>

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

### <span data-ttu-id="b742a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b742a-116">-DefaultProfile</span></span>
<span data-ttu-id="b742a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b742a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b742a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b742a-118">-Name</span></span>
<span data-ttu-id="b742a-119">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b742a-119">The source control name.</span></span>

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

### <span data-ttu-id="b742a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b742a-120">-ResourceGroupName</span></span>
<span data-ttu-id="b742a-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b742a-121">The resource group name.</span></span>

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

### <span data-ttu-id="b742a-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="b742a-122">-SourceType</span></span>
<span data-ttu-id="b742a-123">Тип системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b742a-123">The source control type.</span></span>

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

### <span data-ttu-id="b742a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b742a-124">CommonParameters</span></span>
<span data-ttu-id="b742a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b742a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b742a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b742a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b742a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b742a-127">INPUTS</span></span>

### <span data-ttu-id="b742a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b742a-128">System.String</span></span>

## <span data-ttu-id="b742a-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b742a-129">OUTPUTS</span></span>

### <span data-ttu-id="b742a-130">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="b742a-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="b742a-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b742a-131">NOTES</span></span>

## <span data-ttu-id="b742a-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b742a-132">RELATED LINKS</span></span>
