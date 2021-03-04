---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: 256509a42b844b196728b89b30abcdb6c5b9b386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962739"
---
# <span data-ttu-id="91d3b-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="91d3b-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="91d3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="91d3b-103">Создает параметр политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="91d3b-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="91d3b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91d3b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91d3b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="91d3b-106">Политика **New-AzApplicationGatewayFirewallPolicySetting** создает параметры политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="91d3b-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="91d3b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91d3b-107">EXAMPLES</span></span>

### <span data-ttu-id="91d3b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="91d3b-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="91d3b-109">Команда создает параметр политики с состоянием $enabledState, режимом $enabledMode, RequestBodyCheck как false, FileUploadLimitInMb как $fileUploadLimitInMb и MaxRequestBodySizeInKb как $$maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="91d3b-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="91d3b-110">Новые политики хранятся в $condition.</span><span class="sxs-lookup"><span data-stu-id="91d3b-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="91d3b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91d3b-111">PARAMETERS</span></span>

### <span data-ttu-id="91d3b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d3b-112">-DefaultProfile</span></span>
<span data-ttu-id="91d3b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91d3b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91d3b-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="91d3b-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="91d3b-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span><span class="sxs-lookup"><span data-stu-id="91d3b-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="91d3b-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="91d3b-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="91d3b-117">Максимальный размер fileUpload (МБ).</span><span class="sxs-lookup"><span data-stu-id="91d3b-117">Maximum fileUpload size in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d3b-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="91d3b-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="91d3b-119">MaxRequestBodySizeInKb в параметрах политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="91d3b-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 128
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d3b-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="91d3b-120">-Mode</span></span>
<span data-ttu-id="91d3b-121">Режим брандмауэра в параметрах политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="91d3b-121">Firewall Mode in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: Detection
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d3b-122">-State</span><span class="sxs-lookup"><span data-stu-id="91d3b-122">-State</span></span>
<span data-ttu-id="91d3b-123">Переменная состояния в параметрах политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="91d3b-123">State variable in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d3b-124">CommonParameters</span></span>
<span data-ttu-id="91d3b-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91d3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d3b-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91d3b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d3b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91d3b-127">INPUTS</span></span>

### <span data-ttu-id="91d3b-128">Нет</span><span class="sxs-lookup"><span data-stu-id="91d3b-128">None</span></span>

## <span data-ttu-id="91d3b-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91d3b-129">OUTPUTS</span></span>

### <span data-ttu-id="91d3b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="91d3b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="91d3b-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91d3b-131">NOTES</span></span>

## <span data-ttu-id="91d3b-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91d3b-132">RELATED LINKS</span></span>
