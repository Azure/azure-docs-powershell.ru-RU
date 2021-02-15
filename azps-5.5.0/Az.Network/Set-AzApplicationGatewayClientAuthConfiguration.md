---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: def44c0925239aed345eed84b4f34690d2db8746
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100395696"
---
# <span data-ttu-id="369c6-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="369c6-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="369c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="369c6-102">SYNOPSIS</span></span>
<span data-ttu-id="369c6-103">Изменяет конфигурацию клиентской конфигурации объекта профиля SSL.</span><span class="sxs-lookup"><span data-stu-id="369c6-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="369c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="369c6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="369c6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="369c6-105">DESCRIPTION</span></span>
<span data-ttu-id="369c6-106">**Cmdlet Set-AzApplicationGatewayClientAuthConfiguration** изменяет конфигурацию клиентской конфигурации объекта профиля ssl.</span><span class="sxs-lookup"><span data-stu-id="369c6-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="369c6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="369c6-107">EXAMPLES</span></span>

### <span data-ttu-id="369c6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="369c6-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="369c6-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="369c6-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="369c6-110">Вторая команда получает профиль ssl под названием SslProfile01 для $AppGw и сохраняет параметры в $profile переменной.</span><span class="sxs-lookup"><span data-stu-id="369c6-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="369c6-111">Последняя команда изменяет конфигурацию клиентской конфигурации объекта профиля SSL, который хранится в $profile.</span><span class="sxs-lookup"><span data-stu-id="369c6-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="369c6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="369c6-112">PARAMETERS</span></span>

### <span data-ttu-id="369c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="369c6-113">-DefaultProfile</span></span>
<span data-ttu-id="369c6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="369c6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369c6-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="369c6-115">-SslProfile</span></span>
<span data-ttu-id="369c6-116">Профиль SSL</span><span class="sxs-lookup"><span data-stu-id="369c6-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="369c6-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="369c6-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="369c6-118">Проверьте имя выпуска сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="369c6-118">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="369c6-119">CommonParameters</span></span>
<span data-ttu-id="369c6-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="369c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="369c6-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="369c6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="369c6-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="369c6-122">INPUTS</span></span>

### <span data-ttu-id="369c6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="369c6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="369c6-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="369c6-124">OUTPUTS</span></span>

### <span data-ttu-id="369c6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="369c6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="369c6-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="369c6-126">NOTES</span></span>

## <span data-ttu-id="369c6-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="369c6-127">RELATED LINKS</span></span>


[<span data-ttu-id="369c6-128">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="369c6-128">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="369c6-129">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="369c6-129">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="369c6-130">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="369c6-130">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)
