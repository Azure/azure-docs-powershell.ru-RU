---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509946"
---
# <span data-ttu-id="17efc-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="17efc-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="17efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17efc-102">SYNOPSIS</span></span>
<span data-ttu-id="17efc-103">Удаляет сертификат автоматизации.</span><span class="sxs-lookup"><span data-stu-id="17efc-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="17efc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="17efc-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17efc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17efc-105">DESCRIPTION</span></span>
<span data-ttu-id="17efc-106">При **этом сертификат удаляется** из автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="17efc-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="17efc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="17efc-107">EXAMPLES</span></span>

### <span data-ttu-id="17efc-108">Пример 1. Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="17efc-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="17efc-109">Эта команда удаляет сертификат с именем Cert01 в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="17efc-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="17efc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17efc-110">PARAMETERS</span></span>

### <span data-ttu-id="17efc-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17efc-111">-AutomationAccountName</span></span>
<span data-ttu-id="17efc-112">Указывает имя учетной записи автоматизации, для которой этот cmdlet удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="17efc-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="17efc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17efc-113">-DefaultProfile</span></span>
<span data-ttu-id="17efc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="17efc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17efc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="17efc-115">-Name</span></span>
<span data-ttu-id="17efc-116">Указывает имя сертификата, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17efc-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="17efc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17efc-117">-ResourceGroupName</span></span>
<span data-ttu-id="17efc-118">Имя группы ресурсов, для которой этот cmdlet удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="17efc-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="17efc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17efc-119">-Confirm</span></span>
<span data-ttu-id="17efc-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="17efc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17efc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17efc-121">-WhatIf</span></span>
<span data-ttu-id="17efc-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17efc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17efc-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="17efc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17efc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17efc-124">CommonParameters</span></span>
<span data-ttu-id="17efc-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17efc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17efc-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17efc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17efc-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17efc-127">INPUTS</span></span>

### <span data-ttu-id="17efc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="17efc-128">System.String</span></span>

## <span data-ttu-id="17efc-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17efc-129">OUTPUTS</span></span>

### <span data-ttu-id="17efc-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="17efc-130">System.Void</span></span>

## <span data-ttu-id="17efc-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="17efc-131">NOTES</span></span>

## <span data-ttu-id="17efc-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17efc-132">RELATED LINKS</span></span>

[<span data-ttu-id="17efc-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="17efc-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="17efc-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="17efc-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="17efc-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="17efc-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


