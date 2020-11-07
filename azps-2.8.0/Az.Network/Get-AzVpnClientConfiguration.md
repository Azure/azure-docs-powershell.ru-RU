---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: c91b42620d98cae3ecc5dcbd1f8a769c96675ade
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902269"
---
# <span data-ttu-id="5b903-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b903-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="5b903-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b903-102">SYNOPSIS</span></span>
<span data-ttu-id="5b903-103">Позволяет пользователям легко загрузить пакет профиля VPN, созданный с помощью New-AzVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="5b903-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="5b903-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b903-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b903-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b903-105">DESCRIPTION</span></span>
<span data-ttu-id="5b903-106">Get-AzVpnClientConfiguration возвращает URL-адрес, с которого может быть загружен VPN-клиент.</span><span class="sxs-lookup"><span data-stu-id="5b903-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="5b903-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b903-107">EXAMPLES</span></span>

### <span data-ttu-id="5b903-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b903-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="5b903-109">Возвращает URL-адрес для скачивания профиля VpnClient, который был ранее создан с помощью команды New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5b903-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="5b903-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b903-110">PARAMETERS</span></span>

### <span data-ttu-id="5b903-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b903-111">-DefaultProfile</span></span>
<span data-ttu-id="5b903-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b903-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b903-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b903-113">-Name</span></span>
<span data-ttu-id="5b903-114">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5b903-114">The resource name.</span></span>

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

### <span data-ttu-id="5b903-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b903-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b903-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b903-116">The resource group name.</span></span>

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

### <span data-ttu-id="5b903-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b903-117">-Confirm</span></span>
<span data-ttu-id="5b903-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b903-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b903-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b903-119">-WhatIf</span></span>
<span data-ttu-id="5b903-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5b903-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b903-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b903-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b903-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b903-122">CommonParameters</span></span>
<span data-ttu-id="5b903-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b903-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b903-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b903-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b903-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b903-125">INPUTS</span></span>

### <span data-ttu-id="5b903-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5b903-126">System.String</span></span>

## <span data-ttu-id="5b903-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b903-127">OUTPUTS</span></span>

### <span data-ttu-id="5b903-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="5b903-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="5b903-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b903-129">NOTES</span></span>

## <span data-ttu-id="5b903-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b903-130">RELATED LINKS</span></span>

[<span data-ttu-id="5b903-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b903-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
