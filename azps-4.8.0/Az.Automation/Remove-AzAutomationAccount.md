---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243724"
---
# <span data-ttu-id="5c949-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5c949-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="5c949-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c949-102">SYNOPSIS</span></span>
<span data-ttu-id="5c949-103">Удаление учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5c949-103">Removes an Automation account.</span></span>

## <span data-ttu-id="5c949-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c949-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c949-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c949-105">DESCRIPTION</span></span>
<span data-ttu-id="5c949-106">Командлет **Remove-AzAutomationAccount** удаляет учетную запись службы автоматизации Azure из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c949-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="5c949-107">Дополнительные сведения об учетных записях автоматизации можно найти в командлете New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="5c949-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="5c949-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c949-108">EXAMPLES</span></span>

### <span data-ttu-id="5c949-109">Пример 1: Удаление учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="5c949-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5c949-110">Эта команда удаляет учетную запись автоматизации с именем ContosoAutomationAccount без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5c949-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="5c949-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c949-111">PARAMETERS</span></span>

### <span data-ttu-id="5c949-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c949-112">-DefaultProfile</span></span>
<span data-ttu-id="5c949-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5c949-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c949-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5c949-114">-Force</span></span>
<span data-ttu-id="5c949-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="5c949-115">ps_force</span></span>

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

### <span data-ttu-id="5c949-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5c949-116">-Name</span></span>
<span data-ttu-id="5c949-117">Указывает имя учетной записи автоматизации, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5c949-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5c949-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c949-118">-ResourceGroupName</span></span>
<span data-ttu-id="5c949-119">Указывает имя группы ресурсов, из которой этот командлет удаляет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5c949-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="5c949-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c949-120">-Confirm</span></span>
<span data-ttu-id="5c949-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5c949-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c949-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c949-122">-WhatIf</span></span>
<span data-ttu-id="5c949-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5c949-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c949-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5c949-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c949-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c949-125">CommonParameters</span></span>
<span data-ttu-id="5c949-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c949-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c949-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c949-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c949-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c949-128">INPUTS</span></span>

### <span data-ttu-id="5c949-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5c949-129">System.String</span></span>

## <span data-ttu-id="5c949-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c949-130">OUTPUTS</span></span>

### <span data-ttu-id="5c949-131">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5c949-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="5c949-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c949-132">NOTES</span></span>

## <span data-ttu-id="5c949-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c949-133">RELATED LINKS</span></span>

[<span data-ttu-id="5c949-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5c949-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="5c949-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5c949-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="5c949-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5c949-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


