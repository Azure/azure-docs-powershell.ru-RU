---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417959"
---
# <span data-ttu-id="658d6-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="658d6-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="658d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="658d6-102">SYNOPSIS</span></span>
<span data-ttu-id="658d6-103">Позволяет пользователям легко скачать пакет профиля VPN, созданный с помощью New-AzVpnClientConfiguration командлета.</span><span class="sxs-lookup"><span data-stu-id="658d6-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="658d6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="658d6-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="658d6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="658d6-105">DESCRIPTION</span></span>
<span data-ttu-id="658d6-106">Он Get-AzVpnClientConfiguration URL-адрес, с которых можно скачать VPN-клиент.</span><span class="sxs-lookup"><span data-stu-id="658d6-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="658d6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="658d6-107">EXAMPLES</span></span>

### <span data-ttu-id="658d6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="658d6-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="658d6-109">Url-адрес для скачивания профиля VpnClient, ранее сгенерированного с помощью команды New-AzVpnClientConfiguration клиента.</span><span class="sxs-lookup"><span data-stu-id="658d6-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="658d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="658d6-110">PARAMETERS</span></span>

### <span data-ttu-id="658d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658d6-111">-DefaultProfile</span></span>
<span data-ttu-id="658d6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="658d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="658d6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="658d6-113">-Name</span></span>
<span data-ttu-id="658d6-114">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="658d6-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="658d6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="658d6-115">-ResourceGroupName</span></span>
<span data-ttu-id="658d6-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="658d6-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="658d6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="658d6-117">-Confirm</span></span>
<span data-ttu-id="658d6-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="658d6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658d6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="658d6-119">-WhatIf</span></span>
<span data-ttu-id="658d6-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="658d6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="658d6-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="658d6-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658d6-122">CommonParameters</span></span>
<span data-ttu-id="658d6-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="658d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658d6-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="658d6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658d6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="658d6-125">INPUTS</span></span>

### <span data-ttu-id="658d6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="658d6-126">System.String</span></span>

## <span data-ttu-id="658d6-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="658d6-127">OUTPUTS</span></span>

### <span data-ttu-id="658d6-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="658d6-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="658d6-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="658d6-129">NOTES</span></span>

## <span data-ttu-id="658d6-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="658d6-130">RELATED LINKS</span></span>

[<span data-ttu-id="658d6-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="658d6-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
