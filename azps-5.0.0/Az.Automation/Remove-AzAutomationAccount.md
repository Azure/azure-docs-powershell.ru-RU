---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315242"
---
# <span data-ttu-id="aea6f-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aea6f-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="aea6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aea6f-102">SYNOPSIS</span></span>
<span data-ttu-id="aea6f-103">Удаление учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="aea6f-103">Removes an Automation account.</span></span>

## <span data-ttu-id="aea6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aea6f-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aea6f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aea6f-105">DESCRIPTION</span></span>
<span data-ttu-id="aea6f-106">Командлет **Remove-AzAutomationAccount** удаляет учетную запись службы автоматизации Azure из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aea6f-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="aea6f-107">Дополнительные сведения об учетных записях автоматизации можно найти в командлете New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="aea6f-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="aea6f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aea6f-108">EXAMPLES</span></span>

### <span data-ttu-id="aea6f-109">Пример 1: Удаление учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="aea6f-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aea6f-110">Эта команда удаляет учетную запись автоматизации с именем ContosoAutomationAccount без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="aea6f-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="aea6f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aea6f-111">PARAMETERS</span></span>

### <span data-ttu-id="aea6f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea6f-112">-DefaultProfile</span></span>
<span data-ttu-id="aea6f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aea6f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aea6f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="aea6f-114">-Force</span></span>
<span data-ttu-id="aea6f-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="aea6f-115">ps_force</span></span>

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

### <span data-ttu-id="aea6f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aea6f-116">-Name</span></span>
<span data-ttu-id="aea6f-117">Указывает имя учетной записи автоматизации, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aea6f-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aea6f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea6f-118">-ResourceGroupName</span></span>
<span data-ttu-id="aea6f-119">Указывает имя группы ресурсов, из которой этот командлет удаляет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="aea6f-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="aea6f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aea6f-120">-Confirm</span></span>
<span data-ttu-id="aea6f-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aea6f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aea6f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aea6f-122">-WhatIf</span></span>
<span data-ttu-id="aea6f-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aea6f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aea6f-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aea6f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aea6f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea6f-125">CommonParameters</span></span>
<span data-ttu-id="aea6f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aea6f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea6f-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea6f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea6f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aea6f-128">INPUTS</span></span>

### <span data-ttu-id="aea6f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aea6f-129">System.String</span></span>

## <span data-ttu-id="aea6f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aea6f-130">OUTPUTS</span></span>

### <span data-ttu-id="aea6f-131">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aea6f-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="aea6f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="aea6f-132">NOTES</span></span>

## <span data-ttu-id="aea6f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aea6f-133">RELATED LINKS</span></span>

[<span data-ttu-id="aea6f-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aea6f-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="aea6f-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aea6f-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="aea6f-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aea6f-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


