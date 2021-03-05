---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: c6aa2bb9bf3866e35ad59e59bdf5ded333fd2816
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011880"
---
# <span data-ttu-id="2723f-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="2723f-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="2723f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2723f-102">SYNOPSIS</span></span>
<span data-ttu-id="2723f-103">Создание новой переопределения подписи обнаружения политики обнаружения брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="2723f-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="2723f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2723f-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2723f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2723f-105">DESCRIPTION</span></span>
<span data-ttu-id="2723f-106">Для создания переопределения подписей брандмауэра Azure создается объект **New-AzFirewallPolicyIntrusionDetectionSignatureOverride.**</span><span class="sxs-lookup"><span data-stu-id="2723f-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="2723f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2723f-107">EXAMPLES</span></span>

### <span data-ttu-id="2723f-108">Пример 1: 1.</span><span class="sxs-lookup"><span data-stu-id="2723f-108">Example 1: 1.</span></span> <span data-ttu-id="2723f-109">Создание обнаружения назойки с переопределениями подписей</span><span class="sxs-lookup"><span data-stu-id="2723f-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="2723f-110">В этом примере обнаружение назойки с определенной подписью переопределяется в режиме запрета.</span><span class="sxs-lookup"><span data-stu-id="2723f-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="2723f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2723f-111">PARAMETERS</span></span>

### <span data-ttu-id="2723f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2723f-112">-DefaultProfile</span></span>
<span data-ttu-id="2723f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2723f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2723f-114">-Id</span><span class="sxs-lookup"><span data-stu-id="2723f-114">-Id</span></span>
<span data-ttu-id="2723f-115">"ИД подписи".</span><span class="sxs-lookup"><span data-stu-id="2723f-115">Signature id.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2723f-116">-Mode</span><span class="sxs-lookup"><span data-stu-id="2723f-116">-Mode</span></span>
<span data-ttu-id="2723f-117">Состояние подписи.</span><span class="sxs-lookup"><span data-stu-id="2723f-117">Signature state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2723f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2723f-118">-Confirm</span></span>
<span data-ttu-id="2723f-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2723f-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2723f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2723f-120">-WhatIf</span></span>
<span data-ttu-id="2723f-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2723f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2723f-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2723f-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2723f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2723f-123">CommonParameters</span></span>
<span data-ttu-id="2723f-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2723f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2723f-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2723f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2723f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2723f-126">INPUTS</span></span>

### <span data-ttu-id="2723f-127">Нет</span><span class="sxs-lookup"><span data-stu-id="2723f-127">None</span></span>

## <span data-ttu-id="2723f-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2723f-128">OUTPUTS</span></span>

### <span data-ttu-id="2723f-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="2723f-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="2723f-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2723f-130">NOTES</span></span>

## <span data-ttu-id="2723f-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2723f-131">RELATED LINKS</span></span>
