---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: c917089d11f4fe0ffe9ec98df5f75dec2af91f82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734729"
---
# <span data-ttu-id="bb39a-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bb39a-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="bb39a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb39a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb39a-103">Удаление сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="bb39a-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb39a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb39a-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb39a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb39a-105">DESCRIPTION</span></span>
<span data-ttu-id="bb39a-106">Командлет **Remove-AzureRmAutomationCertificate** Удаляет сертификат из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bb39a-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="bb39a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb39a-107">EXAMPLES</span></span>

### <span data-ttu-id="bb39a-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="bb39a-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bb39a-109">Эта команда удаляет сертификат с именем Cert01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bb39a-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="bb39a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb39a-110">PARAMETERS</span></span>

### <span data-ttu-id="bb39a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bb39a-111">-AutomationAccountName</span></span>
<span data-ttu-id="bb39a-112">Указывает имя учетной записи автоматизации, для которой этот командлет удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="bb39a-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="bb39a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb39a-113">-DefaultProfile</span></span>
<span data-ttu-id="bb39a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bb39a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb39a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb39a-115">-Name</span></span>
<span data-ttu-id="bb39a-116">Указывает имя сертификата, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bb39a-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bb39a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb39a-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb39a-118">Указывает имя группы ресурсов, для которой этот командлет удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="bb39a-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="bb39a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb39a-119">-Confirm</span></span>
<span data-ttu-id="bb39a-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb39a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb39a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb39a-121">-WhatIf</span></span>
<span data-ttu-id="bb39a-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb39a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb39a-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb39a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb39a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb39a-124">CommonParameters</span></span>
<span data-ttu-id="bb39a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb39a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb39a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb39a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb39a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb39a-127">INPUTS</span></span>

### <span data-ttu-id="bb39a-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="bb39a-128">None</span></span>
<span data-ttu-id="bb39a-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bb39a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb39a-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb39a-130">OUTPUTS</span></span>

## <span data-ttu-id="bb39a-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb39a-131">NOTES</span></span>

## <span data-ttu-id="bb39a-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb39a-132">RELATED LINKS</span></span>

[<span data-ttu-id="bb39a-133">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bb39a-133">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="bb39a-134">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bb39a-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="bb39a-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bb39a-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


