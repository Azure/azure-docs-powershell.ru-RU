---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: e3dd0d475a2a2c34dfa7912bf9ced4ef958295c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561203"
---
# <span data-ttu-id="98f27-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="98f27-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="98f27-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98f27-102">SYNOPSIS</span></span>
<span data-ttu-id="98f27-103">Удаление учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="98f27-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98f27-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98f27-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98f27-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98f27-105">DESCRIPTION</span></span>
<span data-ttu-id="98f27-106">Командлет **Remove-AzureRmAutomationAccount** удаляет учетную запись службы автоматизации Azure из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98f27-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="98f27-107">Дополнительные сведения об учетных записях автоматизации можно найти в командлете New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="98f27-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="98f27-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98f27-108">EXAMPLES</span></span>

### <span data-ttu-id="98f27-109">Пример 1: Удаление учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="98f27-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="98f27-110">Эта команда удаляет учетную запись автоматизации с именем ContosoAutomationAccount без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="98f27-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="98f27-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98f27-111">PARAMETERS</span></span>

### <span data-ttu-id="98f27-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f27-112">-DefaultProfile</span></span>
<span data-ttu-id="98f27-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="98f27-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f27-114">-Force</span><span class="sxs-lookup"><span data-stu-id="98f27-114">-Force</span></span>
<span data-ttu-id="98f27-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="98f27-115">ps_force</span></span>

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

### <span data-ttu-id="98f27-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98f27-116">-Name</span></span>
<span data-ttu-id="98f27-117">Указывает имя учетной записи автоматизации, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="98f27-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="98f27-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f27-118">-ResourceGroupName</span></span>
<span data-ttu-id="98f27-119">Указывает имя группы ресурсов, из которой этот командлет удаляет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="98f27-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="98f27-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98f27-120">-Confirm</span></span>
<span data-ttu-id="98f27-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98f27-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f27-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f27-122">-WhatIf</span></span>
<span data-ttu-id="98f27-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="98f27-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f27-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="98f27-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f27-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f27-125">CommonParameters</span></span>
<span data-ttu-id="98f27-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98f27-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f27-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f27-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f27-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98f27-128">INPUTS</span></span>

### <span data-ttu-id="98f27-129">System. String</span><span class="sxs-lookup"><span data-stu-id="98f27-129">System.String</span></span>

## <span data-ttu-id="98f27-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98f27-130">OUTPUTS</span></span>

### <span data-ttu-id="98f27-131">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="98f27-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="98f27-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="98f27-132">NOTES</span></span>

## <span data-ttu-id="98f27-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98f27-133">RELATED LINKS</span></span>

[<span data-ttu-id="98f27-134">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="98f27-134">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="98f27-135">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="98f27-135">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="98f27-136">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="98f27-136">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


