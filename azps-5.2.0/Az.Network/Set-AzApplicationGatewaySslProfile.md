---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 1763dfab6815efd625ff43ee248664a3f7b36cb9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417703"
---
# <span data-ttu-id="96144-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="96144-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="96144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96144-102">SYNOPSIS</span></span>
<span data-ttu-id="96144-103">Обновляет SSL-профиль шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="96144-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="96144-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="96144-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96144-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96144-105">DESCRIPTION</span></span>
<span data-ttu-id="96144-106">**Cmdlet Set-AzApplicationGatewaySslProfile** обновляет профиль ssl для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="96144-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="96144-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="96144-107">EXAMPLES</span></span>

### <span data-ttu-id="96144-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96144-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="96144-109">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="96144-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="96144-110">Вторая команда обновляет ssl-профиль шлюза приложения в переменной $AppGw, чтобы обновить конфигурацию политики клиента до нового значения, храняого в $newclientconfig.</span><span class="sxs-lookup"><span data-stu-id="96144-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="96144-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96144-111">PARAMETERS</span></span>

### <span data-ttu-id="96144-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96144-112">-ApplicationGateway</span></span>
<span data-ttu-id="96144-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96144-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96144-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="96144-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="96144-115">Параметры конфигурации проверки подлинности клиента</span><span class="sxs-lookup"><span data-stu-id="96144-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96144-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96144-116">-DefaultProfile</span></span>
<span data-ttu-id="96144-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96144-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96144-118">-Name</span><span class="sxs-lookup"><span data-stu-id="96144-118">-Name</span></span>
<span data-ttu-id="96144-119">Имя профиля SSL</span><span class="sxs-lookup"><span data-stu-id="96144-119">The name of the SSL profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96144-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="96144-120">-SslPolicy</span></span>
<span data-ttu-id="96144-121">Политика SSL</span><span class="sxs-lookup"><span data-stu-id="96144-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96144-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="96144-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="96144-123">Цепочки сертификатов доверенных клиентов ЦС</span><span class="sxs-lookup"><span data-stu-id="96144-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96144-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96144-124">CommonParameters</span></span>
<span data-ttu-id="96144-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96144-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96144-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96144-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96144-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96144-127">INPUTS</span></span>

### <span data-ttu-id="96144-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96144-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96144-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96144-129">OUTPUTS</span></span>

### <span data-ttu-id="96144-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96144-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96144-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="96144-131">NOTES</span></span>

## <span data-ttu-id="96144-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96144-132">RELATED LINKS</span></span>

[<span data-ttu-id="96144-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="96144-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="96144-134">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="96144-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="96144-135">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="96144-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="96144-136">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="96144-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)