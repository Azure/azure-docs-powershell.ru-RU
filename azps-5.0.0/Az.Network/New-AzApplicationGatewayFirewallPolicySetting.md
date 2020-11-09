---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318026"
---
# <span data-ttu-id="f7ce3-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="f7ce3-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="f7ce3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ce3-103">Создание параметра политики для политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="f7ce3-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="f7ce3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7ce3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7ce3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ce3-106">**Новый параметр-AzApplicationGatewayFirewallPolicySetting** создает параметры политики для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f7ce3-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="f7ce3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7ce3-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ce3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7ce3-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="f7ce3-109">Команда создает параметр политики с состоянием как $enabledState, режимом как $enabledMode, RequestBodyCheck как false, FileUploadLimitInMb как $fileUploadLimitInMb и MaxRequestBodySizeInKb как $ $maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="f7ce3-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="f7ce3-110">Новый policySettings хранится в $condition.</span><span class="sxs-lookup"><span data-stu-id="f7ce3-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="f7ce3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7ce3-111">PARAMETERS</span></span>

### <span data-ttu-id="f7ce3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ce3-112">-DefaultProfile</span></span>
<span data-ttu-id="f7ce3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ce3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7ce3-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="f7ce3-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="f7ce3-115">RequestBodyCheck в параметрах политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f7ce3-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="f7ce3-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="f7ce3-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="f7ce3-117">Максимальный размер fileUpload (в МБ).</span><span class="sxs-lookup"><span data-stu-id="f7ce3-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="f7ce3-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="f7ce3-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="f7ce3-119">MaxRequestBodySizeInKb в параметрах политики политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f7ce3-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="f7ce3-120">Режим</span><span class="sxs-lookup"><span data-stu-id="f7ce3-120">-Mode</span></span>
<span data-ttu-id="f7ce3-121">Режим брандмауэра в параметрах политики политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f7ce3-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="f7ce3-122">-State</span><span class="sxs-lookup"><span data-stu-id="f7ce3-122">-State</span></span>
<span data-ttu-id="f7ce3-123">Переменная состояния в параметрах политики политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f7ce3-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="f7ce3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ce3-124">CommonParameters</span></span>
<span data-ttu-id="f7ce3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7ce3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ce3-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7ce3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ce3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7ce3-127">INPUTS</span></span>

### <span data-ttu-id="f7ce3-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="f7ce3-128">None</span></span>

## <span data-ttu-id="f7ce3-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7ce3-129">OUTPUTS</span></span>

### <span data-ttu-id="f7ce3-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="f7ce3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="f7ce3-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7ce3-131">NOTES</span></span>

## <span data-ttu-id="f7ce3-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7ce3-132">RELATED LINKS</span></span>
