---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225988"
---
# <span data-ttu-id="3421c-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="3421c-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="3421c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3421c-102">SYNOPSIS</span></span>
<span data-ttu-id="3421c-103">Позволяет пользователям легко скачать пакет профиля VPN, созданный с помощью New-AzVpnClientConfiguration командлета.</span><span class="sxs-lookup"><span data-stu-id="3421c-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="3421c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3421c-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3421c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3421c-105">DESCRIPTION</span></span>
<span data-ttu-id="3421c-106">Он Get-AzVpnClientConfiguration URL-адрес, с которых можно скачать VPN-клиент.</span><span class="sxs-lookup"><span data-stu-id="3421c-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="3421c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3421c-107">EXAMPLES</span></span>

### <span data-ttu-id="3421c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3421c-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="3421c-109">Url-адрес для скачивания профиля VpnClient, ранее сгенерированного с помощью команды New-AzVpnClientConfiguration клиента.</span><span class="sxs-lookup"><span data-stu-id="3421c-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="3421c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3421c-110">PARAMETERS</span></span>

### <span data-ttu-id="3421c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3421c-111">-DefaultProfile</span></span>
<span data-ttu-id="3421c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3421c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3421c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3421c-113">-Name</span></span>
<span data-ttu-id="3421c-114">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3421c-114">The resource name.</span></span>

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

### <span data-ttu-id="3421c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3421c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3421c-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3421c-116">The resource group name.</span></span>

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

### <span data-ttu-id="3421c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3421c-117">-Confirm</span></span>
<span data-ttu-id="3421c-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3421c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3421c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3421c-119">-WhatIf</span></span>
<span data-ttu-id="3421c-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3421c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3421c-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3421c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3421c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3421c-122">CommonParameters</span></span>
<span data-ttu-id="3421c-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3421c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3421c-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3421c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3421c-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3421c-125">INPUTS</span></span>

### <span data-ttu-id="3421c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="3421c-126">System.String</span></span>

## <span data-ttu-id="3421c-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3421c-127">OUTPUTS</span></span>

### <span data-ttu-id="3421c-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="3421c-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="3421c-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3421c-129">NOTES</span></span>

## <span data-ttu-id="3421c-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3421c-130">RELATED LINKS</span></span>

[<span data-ttu-id="3421c-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="3421c-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
