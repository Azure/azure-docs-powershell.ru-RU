---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: d1230030f95d22d972aa537208b30f350ec9dbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566325"
---
# <span data-ttu-id="082d3-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="082d3-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="082d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="082d3-102">SYNOPSIS</span></span>
<span data-ttu-id="082d3-103">Удаление сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="082d3-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="082d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="082d3-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="082d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="082d3-105">DESCRIPTION</span></span>
<span data-ttu-id="082d3-106">Командлет **Remove-AzureRmAutomationCertificate** Удаляет сертификат из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="082d3-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="082d3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="082d3-107">EXAMPLES</span></span>

### <span data-ttu-id="082d3-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="082d3-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="082d3-109">Эта команда удаляет сертификат с именем Cert01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="082d3-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="082d3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="082d3-110">PARAMETERS</span></span>

### <span data-ttu-id="082d3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="082d3-111">-AutomationAccountName</span></span>
<span data-ttu-id="082d3-112">Указывает имя учетной записи автоматизации, для которой этот командлет удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="082d3-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="082d3-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="082d3-113">-Name</span></span>
<span data-ttu-id="082d3-114">Указывает имя сертификата, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="082d3-114">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="082d3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="082d3-115">-ResourceGroupName</span></span>
<span data-ttu-id="082d3-116">Указывает имя группы ресурсов, для которой этот командлет удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="082d3-116">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="082d3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="082d3-117">-Confirm</span></span>
<span data-ttu-id="082d3-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="082d3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="082d3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="082d3-119">-WhatIf</span></span>
<span data-ttu-id="082d3-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="082d3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="082d3-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="082d3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="082d3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082d3-122">-DefaultProfile</span></span>
<span data-ttu-id="082d3-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="082d3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="082d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082d3-124">CommonParameters</span></span>
<span data-ttu-id="082d3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="082d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082d3-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="082d3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082d3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="082d3-127">INPUTS</span></span>

## <span data-ttu-id="082d3-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="082d3-128">OUTPUTS</span></span>

## <span data-ttu-id="082d3-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="082d3-129">NOTES</span></span>

## <span data-ttu-id="082d3-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="082d3-130">RELATED LINKS</span></span>

[<span data-ttu-id="082d3-131">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="082d3-131">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="082d3-132">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="082d3-132">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="082d3-133">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="082d3-133">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


