---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: eecce510632e7eef3fc61cf53127777b93c81e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562840"
---
# <span data-ttu-id="b60db-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b60db-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="b60db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b60db-102">SYNOPSIS</span></span>
<span data-ttu-id="b60db-103">Удаляет доверенный корневой сертификат из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b60db-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b60db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b60db-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayTrustedRootCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b60db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b60db-105">DESCRIPTION</span></span>
<span data-ttu-id="b60db-106">Командлет **Remove-AzureRmApplicationGatewayTrustedRootCertificate** Удаляет доверенный корневой сертификат из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b60db-106">The **Remove-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="b60db-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b60db-107">EXAMPLES</span></span>

### <span data-ttu-id="b60db-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b60db-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="b60db-109">Первая команда получает шлюз приложения и сохраняет его в переменной $gw.</span><span class="sxs-lookup"><span data-stu-id="b60db-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="b60db-110">Вторая команда удаляет доверенный корневой сертификат с именем myRootCA из шлюза приложений, хранящегося в $gw.</span><span class="sxs-lookup"><span data-stu-id="b60db-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="b60db-111">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="b60db-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="b60db-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b60db-112">PARAMETERS</span></span>

### <span data-ttu-id="b60db-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b60db-113">-ApplicationGateway</span></span>
<span data-ttu-id="b60db-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b60db-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b60db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60db-115">-DefaultProfile</span></span>
<span data-ttu-id="b60db-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b60db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b60db-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b60db-117">-Name</span></span>
<span data-ttu-id="b60db-118">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="b60db-118">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b60db-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b60db-119">-Confirm</span></span>
<span data-ttu-id="b60db-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b60db-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60db-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60db-121">-WhatIf</span></span>
<span data-ttu-id="b60db-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b60db-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b60db-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b60db-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60db-124">CommonParameters</span></span>
<span data-ttu-id="b60db-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b60db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60db-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b60db-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60db-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b60db-127">INPUTS</span></span>

### <span data-ttu-id="b60db-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b60db-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b60db-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b60db-129">OUTPUTS</span></span>

### <span data-ttu-id="b60db-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b60db-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b60db-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b60db-131">NOTES</span></span>

## <span data-ttu-id="b60db-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b60db-132">RELATED LINKS</span></span>
