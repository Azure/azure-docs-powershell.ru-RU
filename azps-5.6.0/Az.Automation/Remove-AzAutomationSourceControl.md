---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: b4e60e4bbc7196736c0e49c2b294cf6cb984e7b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009859"
---
# <span data-ttu-id="e5b75-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="e5b75-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="e5b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5b75-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b75-103">Удаляет исходный контроль автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b75-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="e5b75-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5b75-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5b75-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5b75-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b75-106">Новый Remove-AzAutomationSourceControl удаляет исходный контроль из автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b75-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="e5b75-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5b75-107">EXAMPLES</span></span>

### <span data-ttu-id="e5b75-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5b75-108">Example 1</span></span>
<span data-ttu-id="e5b75-109">Эта команда удаляет исходный контроль автоматизации с именем VSTSNative в учетной записи devAccount.</span><span class="sxs-lookup"><span data-stu-id="e5b75-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="e5b75-110">Эта команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="e5b75-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="e5b75-111">Поэтому запрос на подтверждение не будет.</span><span class="sxs-lookup"><span data-stu-id="e5b75-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="e5b75-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5b75-112">PARAMETERS</span></span>

### <span data-ttu-id="e5b75-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e5b75-113">-AutomationAccountName</span></span>
<span data-ttu-id="e5b75-114">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e5b75-114">The automation account name.</span></span>

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

### <span data-ttu-id="e5b75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b75-115">-DefaultProfile</span></span>
<span data-ttu-id="e5b75-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b75-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5b75-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e5b75-117">-Name</span></span>
<span data-ttu-id="e5b75-118">Имя источника.</span><span class="sxs-lookup"><span data-stu-id="e5b75-118">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b75-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5b75-119">-PassThru</span></span>
<span data-ttu-id="e5b75-120">PassThru возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e5b75-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5b75-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e5b75-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b75-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5b75-122">-ResourceGroupName</span></span>
<span data-ttu-id="e5b75-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5b75-123">The resource group name.</span></span>

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

### <span data-ttu-id="e5b75-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5b75-124">-Confirm</span></span>
<span data-ttu-id="e5b75-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b75-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b75-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5b75-126">-WhatIf</span></span>
<span data-ttu-id="e5b75-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b75-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5b75-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e5b75-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b75-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b75-129">CommonParameters</span></span>
<span data-ttu-id="e5b75-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b75-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b75-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5b75-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b75-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5b75-132">INPUTS</span></span>

### <span data-ttu-id="e5b75-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e5b75-133">System.String</span></span>

## <span data-ttu-id="e5b75-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5b75-134">OUTPUTS</span></span>

### <span data-ttu-id="e5b75-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="e5b75-135">System.Void</span></span>

### <span data-ttu-id="e5b75-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5b75-136">System.Boolean</span></span>

## <span data-ttu-id="e5b75-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5b75-137">NOTES</span></span>

## <span data-ttu-id="e5b75-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5b75-138">RELATED LINKS</span></span>
