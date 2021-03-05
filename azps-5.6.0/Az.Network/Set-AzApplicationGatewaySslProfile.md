---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 549b339fa6145209127cbb8f222bd08cd0c5957f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985732"
---
# <span data-ttu-id="d45b8-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d45b8-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="d45b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d45b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d45b8-103">Обновляет SSL-профиль шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d45b8-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="d45b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d45b8-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d45b8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d45b8-105">DESCRIPTION</span></span>
<span data-ttu-id="d45b8-106">**Cmdlet Set-AzApplicationGatewaySslProfile** обновляет профиль ssl для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d45b8-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="d45b8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d45b8-107">EXAMPLES</span></span>

### <span data-ttu-id="d45b8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d45b8-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="d45b8-109">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="d45b8-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="d45b8-110">Вторая команда обновляет ssl-профиль шлюза приложения в переменной $AppGw, чтобы обновить конфигурацию политики клиента до нового значения, храняого в $newclientconfig.</span><span class="sxs-lookup"><span data-stu-id="d45b8-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="d45b8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d45b8-111">PARAMETERS</span></span>

### <span data-ttu-id="d45b8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45b8-112">-ApplicationGateway</span></span>
<span data-ttu-id="d45b8-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45b8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d45b8-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="d45b8-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="d45b8-115">Параметры конфигурации проверки подлинности клиента</span><span class="sxs-lookup"><span data-stu-id="d45b8-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="d45b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45b8-116">-DefaultProfile</span></span>
<span data-ttu-id="d45b8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d45b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d45b8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d45b8-118">-Name</span></span>
<span data-ttu-id="d45b8-119">Имя профиля SSL</span><span class="sxs-lookup"><span data-stu-id="d45b8-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="d45b8-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="d45b8-120">-SslPolicy</span></span>
<span data-ttu-id="d45b8-121">Политика SSL</span><span class="sxs-lookup"><span data-stu-id="d45b8-121">SSL policy</span></span>

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

### <span data-ttu-id="d45b8-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="d45b8-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="d45b8-123">Цепочки сертификатов доверенных клиентов ЦС</span><span class="sxs-lookup"><span data-stu-id="d45b8-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="d45b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45b8-124">CommonParameters</span></span>
<span data-ttu-id="d45b8-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d45b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45b8-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d45b8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45b8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d45b8-127">INPUTS</span></span>

### <span data-ttu-id="d45b8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45b8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d45b8-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d45b8-129">OUTPUTS</span></span>

### <span data-ttu-id="d45b8-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45b8-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d45b8-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d45b8-131">NOTES</span></span>

## <span data-ttu-id="d45b8-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d45b8-132">RELATED LINKS</span></span>

[<span data-ttu-id="d45b8-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d45b8-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d45b8-134">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d45b8-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d45b8-135">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d45b8-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d45b8-136">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d45b8-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)