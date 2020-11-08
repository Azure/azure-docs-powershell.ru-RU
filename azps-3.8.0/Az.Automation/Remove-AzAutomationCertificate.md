---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074939"
---
# <span data-ttu-id="ef97e-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ef97e-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="ef97e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef97e-102">SYNOPSIS</span></span>
<span data-ttu-id="ef97e-103">Удаление сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ef97e-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="ef97e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef97e-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef97e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef97e-105">DESCRIPTION</span></span>
<span data-ttu-id="ef97e-106">Командлет **Remove-AzAutomationCertificate** Удаляет сертификат из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ef97e-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="ef97e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef97e-107">EXAMPLES</span></span>

### <span data-ttu-id="ef97e-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="ef97e-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ef97e-109">Эта команда удаляет сертификат с именем Cert01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ef97e-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ef97e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef97e-110">PARAMETERS</span></span>

### <span data-ttu-id="ef97e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ef97e-111">-AutomationAccountName</span></span>
<span data-ttu-id="ef97e-112">Указывает имя учетной записи автоматизации, для которой этот командлет удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="ef97e-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="ef97e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef97e-113">-DefaultProfile</span></span>
<span data-ttu-id="ef97e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ef97e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef97e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef97e-115">-Name</span></span>
<span data-ttu-id="ef97e-116">Указывает имя сертификата, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ef97e-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ef97e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef97e-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef97e-118">Указывает имя группы ресурсов, для которой этот командлет удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="ef97e-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="ef97e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef97e-119">-Confirm</span></span>
<span data-ttu-id="ef97e-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef97e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef97e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef97e-121">-WhatIf</span></span>
<span data-ttu-id="ef97e-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef97e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef97e-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef97e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef97e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef97e-124">CommonParameters</span></span>
<span data-ttu-id="ef97e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef97e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef97e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef97e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef97e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef97e-127">INPUTS</span></span>

### <span data-ttu-id="ef97e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ef97e-128">System.String</span></span>

## <span data-ttu-id="ef97e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef97e-129">OUTPUTS</span></span>

### <span data-ttu-id="ef97e-130">System. void</span><span class="sxs-lookup"><span data-stu-id="ef97e-130">System.Void</span></span>

## <span data-ttu-id="ef97e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef97e-131">NOTES</span></span>

## <span data-ttu-id="ef97e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef97e-132">RELATED LINKS</span></span>

[<span data-ttu-id="ef97e-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ef97e-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="ef97e-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ef97e-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="ef97e-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ef97e-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


