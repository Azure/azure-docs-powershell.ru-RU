---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
ms.openlocfilehash: 4d6e95534cdadd694fa2ed87d43d3f7387ec9b20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913612"
---
# <span data-ttu-id="56abf-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="56abf-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="56abf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56abf-102">SYNOPSIS</span></span>
<span data-ttu-id="56abf-103">Позволяет пользователям легко загрузить пакет профиля VPN, созданный с помощью New-AzureRmVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="56abf-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56abf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56abf-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56abf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56abf-105">DESCRIPTION</span></span>
<span data-ttu-id="56abf-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="56abf-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="56abf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56abf-107">EXAMPLES</span></span>

### <span data-ttu-id="56abf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56abf-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="56abf-109">Возвращает URL-адрес для скачивания профиля VpnClient, который был ранее создан с помощью команды New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="56abf-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="56abf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56abf-110">PARAMETERS</span></span>

### <span data-ttu-id="56abf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56abf-111">-DefaultProfile</span></span>
<span data-ttu-id="56abf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56abf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56abf-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56abf-113">-Name</span></span>
<span data-ttu-id="56abf-114">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="56abf-114">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56abf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56abf-115">-ResourceGroupName</span></span>
<span data-ttu-id="56abf-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56abf-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56abf-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56abf-117">-Confirm</span></span>
<span data-ttu-id="56abf-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="56abf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56abf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56abf-119">-WhatIf</span></span>
<span data-ttu-id="56abf-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="56abf-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56abf-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="56abf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56abf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56abf-122">CommonParameters</span></span>
<span data-ttu-id="56abf-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56abf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56abf-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56abf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56abf-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56abf-125">INPUTS</span></span>

### <span data-ttu-id="56abf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="56abf-126">System.String</span></span>

## <span data-ttu-id="56abf-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56abf-127">OUTPUTS</span></span>

### <span data-ttu-id="56abf-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="56abf-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="56abf-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="56abf-129">NOTES</span></span>

## <span data-ttu-id="56abf-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56abf-130">RELATED LINKS</span></span>

