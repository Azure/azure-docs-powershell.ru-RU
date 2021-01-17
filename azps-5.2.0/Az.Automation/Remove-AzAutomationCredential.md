---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418391"
---
# <span data-ttu-id="1d6f7-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1d6f7-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="1d6f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d6f7-102">SYNOPSIS</span></span>
<span data-ttu-id="1d6f7-103">Удаляет учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1d6f7-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="1d6f7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d6f7-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d6f7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d6f7-105">DESCRIPTION</span></span>
<span data-ttu-id="1d6f7-106">Для **этого из автоматизации** Azure удаляются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1d6f7-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="1d6f7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d6f7-107">EXAMPLES</span></span>

### <span data-ttu-id="1d6f7-108">Пример 1. Удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="1d6f7-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1d6f7-109">Эта команда удаляет учетные данные ContosoCredential в учетной записи автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1d6f7-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="1d6f7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d6f7-110">PARAMETERS</span></span>

### <span data-ttu-id="1d6f7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d6f7-111">-AutomationAccountName</span></span>
<span data-ttu-id="1d6f7-112">Указывает имя учетной записи автоматизации, из которой этот cmdlet удаляет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1d6f7-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="1d6f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d6f7-113">-DefaultProfile</span></span>
<span data-ttu-id="1d6f7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1d6f7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d6f7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1d6f7-115">-Name</span></span>
<span data-ttu-id="1d6f7-116">Указывает имя учетных данных, которые этот cmdlet удаляет.</span><span class="sxs-lookup"><span data-stu-id="1d6f7-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1d6f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d6f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d6f7-118">Имя группы ресурсов, для которой этот cmdlet удаляет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1d6f7-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="1d6f7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d6f7-119">-Confirm</span></span>
<span data-ttu-id="1d6f7-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d6f7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d6f7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d6f7-121">-WhatIf</span></span>
<span data-ttu-id="1d6f7-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d6f7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d6f7-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1d6f7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d6f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d6f7-124">CommonParameters</span></span>
<span data-ttu-id="1d6f7-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d6f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d6f7-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d6f7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d6f7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d6f7-127">INPUTS</span></span>

### <span data-ttu-id="1d6f7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1d6f7-128">System.String</span></span>

## <span data-ttu-id="1d6f7-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d6f7-129">OUTPUTS</span></span>

### <span data-ttu-id="1d6f7-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="1d6f7-130">System.Void</span></span>

## <span data-ttu-id="1d6f7-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d6f7-131">NOTES</span></span>

## <span data-ttu-id="1d6f7-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d6f7-132">RELATED LINKS</span></span>

[<span data-ttu-id="1d6f7-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1d6f7-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="1d6f7-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1d6f7-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="1d6f7-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1d6f7-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


