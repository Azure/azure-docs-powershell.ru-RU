---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 9ab4af1eefa6214d43eca84f65053eeecb12d912
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562932"
---
# <span data-ttu-id="29ed8-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="29ed8-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="29ed8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="29ed8-103">Позволяет пользователям легко загрузить пакет профиля VPN, созданный с помощью New-AzureRmVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="29ed8-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29ed8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29ed8-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29ed8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29ed8-105">DESCRIPTION</span></span>
<span data-ttu-id="29ed8-106">Get-AzureRmVpnClientConfiguration возвращает URL-адрес, с которого может быть загружен VPN-клиент.</span><span class="sxs-lookup"><span data-stu-id="29ed8-106">The Get-AzureRmVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="29ed8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29ed8-107">EXAMPLES</span></span>

### <span data-ttu-id="29ed8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="29ed8-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="29ed8-109">Возвращает URL-адрес для скачивания профиля VpnClient, который был ранее создан с помощью команды New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="29ed8-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="29ed8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29ed8-110">PARAMETERS</span></span>

### <span data-ttu-id="29ed8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ed8-111">-DefaultProfile</span></span>
<span data-ttu-id="29ed8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29ed8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29ed8-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="29ed8-113">-Name</span></span>
<span data-ttu-id="29ed8-114">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="29ed8-114">The resource name.</span></span>

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

### <span data-ttu-id="29ed8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ed8-115">-ResourceGroupName</span></span>
<span data-ttu-id="29ed8-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29ed8-116">The resource group name.</span></span>

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

### <span data-ttu-id="29ed8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29ed8-117">-Confirm</span></span>
<span data-ttu-id="29ed8-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="29ed8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29ed8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29ed8-119">-WhatIf</span></span>
<span data-ttu-id="29ed8-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="29ed8-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29ed8-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="29ed8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29ed8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ed8-122">CommonParameters</span></span>
<span data-ttu-id="29ed8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29ed8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ed8-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29ed8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ed8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29ed8-125">INPUTS</span></span>

### <span data-ttu-id="29ed8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="29ed8-126">System.String</span></span>

## <span data-ttu-id="29ed8-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29ed8-127">OUTPUTS</span></span>

### <span data-ttu-id="29ed8-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="29ed8-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="29ed8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="29ed8-129">NOTES</span></span>

## <span data-ttu-id="29ed8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29ed8-130">RELATED LINKS</span></span>
