---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: 49b4a02210105529dff2aae2b895d4059ced97f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009992"
---
# <span data-ttu-id="2a396-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2a396-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="2a396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a396-102">SYNOPSIS</span></span>
<span data-ttu-id="2a396-103">Удаляет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="2a396-103">Removes an Automation account.</span></span>

## <span data-ttu-id="2a396-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a396-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a396-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a396-105">DESCRIPTION</span></span>
<span data-ttu-id="2a396-106">При **этом из группы ресурсов** удаляется учетная запись автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="2a396-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="2a396-107">Дополнительные сведения об учетных записях автоматизации см. в New-AzAutomationAccount>.</span><span class="sxs-lookup"><span data-stu-id="2a396-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="2a396-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a396-108">EXAMPLES</span></span>

### <span data-ttu-id="2a396-109">Пример 1. Удаление учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="2a396-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2a396-110">Эта команда удаляет учетную запись автоматизации с именем ContosoAutomationAccount без запроса на проверку пользователем.</span><span class="sxs-lookup"><span data-stu-id="2a396-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="2a396-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a396-111">PARAMETERS</span></span>

### <span data-ttu-id="2a396-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a396-112">-DefaultProfile</span></span>
<span data-ttu-id="2a396-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2a396-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a396-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2a396-114">-Force</span></span>
<span data-ttu-id="2a396-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="2a396-115">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a396-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2a396-116">-Name</span></span>
<span data-ttu-id="2a396-117">Указывает имя учетной записи автоматизации, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a396-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a396-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a396-118">-ResourceGroupName</span></span>
<span data-ttu-id="2a396-119">Имя группы ресурсов, из которой этот cmdlet удаляет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="2a396-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="2a396-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a396-120">-Confirm</span></span>
<span data-ttu-id="2a396-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a396-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a396-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a396-122">-WhatIf</span></span>
<span data-ttu-id="2a396-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a396-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a396-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a396-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a396-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a396-125">CommonParameters</span></span>
<span data-ttu-id="2a396-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a396-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a396-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a396-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a396-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a396-128">INPUTS</span></span>

### <span data-ttu-id="2a396-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2a396-129">System.String</span></span>

## <span data-ttu-id="2a396-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a396-130">OUTPUTS</span></span>

### <span data-ttu-id="2a396-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2a396-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="2a396-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a396-132">NOTES</span></span>

## <span data-ttu-id="2a396-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a396-133">RELATED LINKS</span></span>

[<span data-ttu-id="2a396-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2a396-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="2a396-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2a396-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="2a396-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2a396-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


