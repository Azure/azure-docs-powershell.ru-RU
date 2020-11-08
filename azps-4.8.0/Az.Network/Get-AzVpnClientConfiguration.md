---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078919"
---
# <span data-ttu-id="1df22-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="1df22-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="1df22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1df22-102">SYNOPSIS</span></span>
<span data-ttu-id="1df22-103">Позволяет пользователям легко загрузить пакет профиля VPN, созданный с помощью New-AzVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="1df22-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="1df22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1df22-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1df22-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1df22-105">DESCRIPTION</span></span>
<span data-ttu-id="1df22-106">Get-AzVpnClientConfiguration возвращает URL-адрес, с которого может быть загружен VPN-клиент.</span><span class="sxs-lookup"><span data-stu-id="1df22-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="1df22-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1df22-107">EXAMPLES</span></span>

### <span data-ttu-id="1df22-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1df22-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="1df22-109">Возвращает URL-адрес для скачивания профиля VpnClient, который был ранее создан с помощью команды New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1df22-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="1df22-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1df22-110">PARAMETERS</span></span>

### <span data-ttu-id="1df22-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df22-111">-DefaultProfile</span></span>
<span data-ttu-id="1df22-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1df22-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1df22-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1df22-113">-Name</span></span>
<span data-ttu-id="1df22-114">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1df22-114">The resource name.</span></span>

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

### <span data-ttu-id="1df22-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df22-115">-ResourceGroupName</span></span>
<span data-ttu-id="1df22-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1df22-116">The resource group name.</span></span>

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

### <span data-ttu-id="1df22-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1df22-117">-Confirm</span></span>
<span data-ttu-id="1df22-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1df22-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1df22-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1df22-119">-WhatIf</span></span>
<span data-ttu-id="1df22-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1df22-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1df22-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1df22-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1df22-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df22-122">CommonParameters</span></span>
<span data-ttu-id="1df22-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1df22-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df22-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1df22-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df22-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1df22-125">INPUTS</span></span>

### <span data-ttu-id="1df22-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1df22-126">System.String</span></span>

## <span data-ttu-id="1df22-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1df22-127">OUTPUTS</span></span>

### <span data-ttu-id="1df22-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="1df22-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="1df22-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="1df22-129">NOTES</span></span>

## <span data-ttu-id="1df22-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1df22-130">RELATED LINKS</span></span>

[<span data-ttu-id="1df22-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="1df22-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
