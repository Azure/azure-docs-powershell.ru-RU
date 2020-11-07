---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 63b044c4a9736aca72e9713cd8ec5833e7b056ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909833"
---
# <span data-ttu-id="b62e3-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="b62e3-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="b62e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b62e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b62e3-103">Позволяет пользователям легко загрузить пакет профиля VPN, созданный с помощью New-AzVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="b62e3-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="b62e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b62e3-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b62e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b62e3-105">DESCRIPTION</span></span>
<span data-ttu-id="b62e3-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="b62e3-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="b62e3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b62e3-107">EXAMPLES</span></span>

### <span data-ttu-id="b62e3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b62e3-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="b62e3-109">Возвращает URL-адрес для скачивания профиля VpnClient, который был ранее создан с помощью команды New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b62e3-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="b62e3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b62e3-110">PARAMETERS</span></span>

### <span data-ttu-id="b62e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62e3-111">-DefaultProfile</span></span>
<span data-ttu-id="b62e3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b62e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="b62e3-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b62e3-113">-Name</span></span>
<span data-ttu-id="b62e3-114">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b62e3-114">The resource name.</span></span>

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

### <span data-ttu-id="b62e3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b62e3-115">-ResourceGroupName</span></span>
<span data-ttu-id="b62e3-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b62e3-116">The resource group name.</span></span>

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

### <span data-ttu-id="b62e3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b62e3-117">-Confirm</span></span>
<span data-ttu-id="b62e3-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b62e3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b62e3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b62e3-119">-WhatIf</span></span>
<span data-ttu-id="b62e3-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b62e3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b62e3-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b62e3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b62e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62e3-122">CommonParameters</span></span>
<span data-ttu-id="b62e3-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b62e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62e3-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b62e3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62e3-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b62e3-125">INPUTS</span></span>

### <span data-ttu-id="b62e3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b62e3-126">System.String</span></span>

## <span data-ttu-id="b62e3-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b62e3-127">OUTPUTS</span></span>

### <span data-ttu-id="b62e3-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="b62e3-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="b62e3-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b62e3-129">NOTES</span></span>

## <span data-ttu-id="b62e3-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b62e3-130">RELATED LINKS</span></span>

