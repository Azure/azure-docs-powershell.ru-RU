---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074935"
---
# <span data-ttu-id="d921a-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d921a-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="d921a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d921a-102">SYNOPSIS</span></span>
<span data-ttu-id="d921a-103">Удаляет учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d921a-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="d921a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d921a-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d921a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d921a-105">DESCRIPTION</span></span>
<span data-ttu-id="d921a-106">Командлет **Remove-AzAutomationCredential** удаляет учетные данные из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d921a-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="d921a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d921a-107">EXAMPLES</span></span>

### <span data-ttu-id="d921a-108">Пример 1: удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="d921a-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d921a-109">Эта команда удаляет учетные данные с именем ContosoCredential в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d921a-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d921a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d921a-110">PARAMETERS</span></span>

### <span data-ttu-id="d921a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d921a-111">-AutomationAccountName</span></span>
<span data-ttu-id="d921a-112">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d921a-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="d921a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d921a-113">-DefaultProfile</span></span>
<span data-ttu-id="d921a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d921a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d921a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d921a-115">-Name</span></span>
<span data-ttu-id="d921a-116">Указывает имя учетных данных, которые удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d921a-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d921a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d921a-117">-ResourceGroupName</span></span>
<span data-ttu-id="d921a-118">Указывает имя группы ресурсов, для которой этот командлет удаляет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d921a-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="d921a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d921a-119">-Confirm</span></span>
<span data-ttu-id="d921a-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d921a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d921a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d921a-121">-WhatIf</span></span>
<span data-ttu-id="d921a-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d921a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d921a-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d921a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d921a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d921a-124">CommonParameters</span></span>
<span data-ttu-id="d921a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d921a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d921a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d921a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d921a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d921a-127">INPUTS</span></span>

### <span data-ttu-id="d921a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d921a-128">System.String</span></span>

## <span data-ttu-id="d921a-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d921a-129">OUTPUTS</span></span>

### <span data-ttu-id="d921a-130">System. void</span><span class="sxs-lookup"><span data-stu-id="d921a-130">System.Void</span></span>

## <span data-ttu-id="d921a-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d921a-131">NOTES</span></span>

## <span data-ttu-id="d921a-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d921a-132">RELATED LINKS</span></span>

[<span data-ttu-id="d921a-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d921a-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="d921a-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d921a-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="d921a-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d921a-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


