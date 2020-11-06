---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 2c98cde73610a7a72b237bbe268f527fefaf71a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566322"
---
# <span data-ttu-id="19cdc-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="19cdc-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="19cdc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="19cdc-103">Удаляет учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="19cdc-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19cdc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19cdc-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19cdc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19cdc-105">DESCRIPTION</span></span>
<span data-ttu-id="19cdc-106">Командлет **Remove-AzureRmAutomationCredential** удаляет учетные данные из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="19cdc-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="19cdc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19cdc-107">EXAMPLES</span></span>

### <span data-ttu-id="19cdc-108">Пример 1: удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="19cdc-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="19cdc-109">Эта команда удаляет учетные данные с именем ContosoCredential в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="19cdc-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="19cdc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19cdc-110">PARAMETERS</span></span>

### <span data-ttu-id="19cdc-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19cdc-111">-AutomationAccountName</span></span>
<span data-ttu-id="19cdc-112">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="19cdc-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="19cdc-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19cdc-113">-Name</span></span>
<span data-ttu-id="19cdc-114">Указывает имя учетных данных, которые удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="19cdc-114">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="19cdc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19cdc-115">-ResourceGroupName</span></span>
<span data-ttu-id="19cdc-116">Указывает имя группы ресурсов, для которой этот командлет удаляет учетные данные.</span><span class="sxs-lookup"><span data-stu-id="19cdc-116">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="19cdc-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19cdc-117">-Confirm</span></span>
<span data-ttu-id="19cdc-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19cdc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19cdc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19cdc-119">-WhatIf</span></span>
<span data-ttu-id="19cdc-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19cdc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19cdc-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19cdc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19cdc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19cdc-122">-DefaultProfile</span></span>
<span data-ttu-id="19cdc-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19cdc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19cdc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cdc-124">CommonParameters</span></span>
<span data-ttu-id="19cdc-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19cdc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cdc-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19cdc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cdc-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19cdc-127">INPUTS</span></span>

## <span data-ttu-id="19cdc-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19cdc-128">OUTPUTS</span></span>

## <span data-ttu-id="19cdc-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="19cdc-129">NOTES</span></span>

## <span data-ttu-id="19cdc-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19cdc-130">RELATED LINKS</span></span>

[<span data-ttu-id="19cdc-131">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="19cdc-131">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="19cdc-132">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="19cdc-132">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="19cdc-133">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="19cdc-133">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


