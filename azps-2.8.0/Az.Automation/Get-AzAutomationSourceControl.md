---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: e960b1d68b57ef51ef51a6bd00365242e78f47a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727820"
---
# <span data-ttu-id="9e38c-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="9e38c-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="9e38c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e38c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e38c-103">Получает список элементов управления источником автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="9e38c-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="9e38c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e38c-104">SYNTAX</span></span>

### <span data-ttu-id="9e38c-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e38c-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e38c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9e38c-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e38c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e38c-107">DESCRIPTION</span></span>
<span data-ttu-id="9e38c-108">Командлет Get-AzAutomationSourceControl получает элементы управления источником автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9e38c-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="9e38c-109">Чтобы получить определенную систему управления версиями, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="9e38c-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="9e38c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e38c-110">EXAMPLES</span></span>

### <span data-ttu-id="9e38c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e38c-111">Example 1</span></span>
<span data-ttu-id="9e38c-112">Эта команда получает элемент управления источником автоматизации с именем VSTSNative в учетной записи с именем devAccount.</span><span class="sxs-lookup"><span data-stu-id="9e38c-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="9e38c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e38c-113">PARAMETERS</span></span>

### <span data-ttu-id="9e38c-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e38c-114">-AutomationAccountName</span></span>
<span data-ttu-id="9e38c-115">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9e38c-115">The automation account name.</span></span>

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

### <span data-ttu-id="9e38c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e38c-116">-DefaultProfile</span></span>
<span data-ttu-id="9e38c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e38c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e38c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e38c-118">-Name</span></span>
<span data-ttu-id="9e38c-119">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9e38c-119">The source control name.</span></span>

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

### <span data-ttu-id="9e38c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e38c-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e38c-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e38c-121">The resource group name.</span></span>

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

### <span data-ttu-id="9e38c-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="9e38c-122">-SourceType</span></span>
<span data-ttu-id="9e38c-123">Тип системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="9e38c-123">The source control type.</span></span>

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

### <span data-ttu-id="9e38c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e38c-124">CommonParameters</span></span>
<span data-ttu-id="9e38c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e38c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e38c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e38c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e38c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e38c-127">INPUTS</span></span>

### <span data-ttu-id="9e38c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9e38c-128">System.String</span></span>

## <span data-ttu-id="9e38c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e38c-129">OUTPUTS</span></span>

### <span data-ttu-id="9e38c-130">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="9e38c-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="9e38c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e38c-131">NOTES</span></span>

## <span data-ttu-id="9e38c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e38c-132">RELATED LINKS</span></span>
