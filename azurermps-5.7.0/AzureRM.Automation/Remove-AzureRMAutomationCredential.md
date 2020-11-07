---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 11b6772325c3e5170c697b21d25092fd96f3e2e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734725"
---
# <span data-ttu-id="30278-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="30278-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="30278-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30278-102">SYNOPSIS</span></span>
<span data-ttu-id="30278-103">Удаляет учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="30278-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30278-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30278-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30278-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30278-105">DESCRIPTION</span></span>
<span data-ttu-id="30278-106">Командлет **Remove-AzureRmAutomationCredential** удаляет учетные данные из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="30278-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="30278-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30278-107">EXAMPLES</span></span>

### <span data-ttu-id="30278-108">Пример 1: удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="30278-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="30278-109">Эта команда удаляет учетные данные с именем ContosoCredential в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="30278-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="30278-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30278-110">PARAMETERS</span></span>

### <span data-ttu-id="30278-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="30278-111">-AutomationAccountName</span></span>
<span data-ttu-id="30278-112">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="30278-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30278-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30278-113">-DefaultProfile</span></span>
<span data-ttu-id="30278-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="30278-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30278-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30278-115">-Name</span></span>
<span data-ttu-id="30278-116">Указывает имя учетных данных, которые удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="30278-116">Specifies the name of the credential that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30278-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30278-117">-ResourceGroupName</span></span>
<span data-ttu-id="30278-118">Указывает имя группы ресурсов, для которой этот командлет удаляет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="30278-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30278-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30278-119">-Confirm</span></span>
<span data-ttu-id="30278-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30278-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30278-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30278-121">-WhatIf</span></span>
<span data-ttu-id="30278-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30278-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30278-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30278-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30278-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30278-124">CommonParameters</span></span>
<span data-ttu-id="30278-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30278-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30278-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30278-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30278-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30278-127">INPUTS</span></span>

### <span data-ttu-id="30278-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="30278-128">None</span></span>
<span data-ttu-id="30278-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="30278-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30278-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30278-130">OUTPUTS</span></span>

## <span data-ttu-id="30278-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="30278-131">NOTES</span></span>

## <span data-ttu-id="30278-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30278-132">RELATED LINKS</span></span>

[<span data-ttu-id="30278-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="30278-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="30278-134">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="30278-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="30278-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="30278-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


