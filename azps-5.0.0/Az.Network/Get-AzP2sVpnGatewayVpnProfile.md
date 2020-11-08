---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249383"
---
# <span data-ttu-id="c4d6d-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="c4d6d-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="c4d6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d6d-103">Генерирует и возвращает URL-адрес SAS для клиента, чтобы скачать профиль VPN для "Установка клиента сайта", чтобы он указывал на подключение к сайту P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="c4d6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4d6d-104">SYNTAX</span></span>

### <span data-ttu-id="c4d6d-105">ByP2SVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4d6d-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4d6d-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c4d6d-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4d6d-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c4d6d-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4d6d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4d6d-108">DESCRIPTION</span></span>
<span data-ttu-id="c4d6d-109">Командлет **Get-AzP2sVpnGatewayVpnProfile** позволяет создавать и получать URL-адрес SAS для заказчиков для загрузки профиля VPN, чтобы указать для него подключение к сайту на сайте P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="c4d6d-110">Настройка клиента сайта с помощью этого профиля VPN может подключаться только к этому конкретному P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="c4d6d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4d6d-111">EXAMPLES</span></span>

### <span data-ttu-id="c4d6d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4d6d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="c4d6d-113">Командлет **Get-AzP2sVpnGatewayVpnProfile** позволяет создавать и получать URL-адрес SAS для заказчиков для загрузки профиля VPN, чтобы указать для него подключение к сайту на сайте P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="c4d6d-114">В ProfileUrl показан URL-адрес SAS, с которого клиент может скачать профиль VPN для установки клиента на сайт.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="c4d6d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4d6d-115">PARAMETERS</span></span>

### <span data-ttu-id="c4d6d-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="c4d6d-116">-AuthenticationMethod</span></span>
<span data-ttu-id="c4d6d-117">Способ проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="c4d6d-117">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d6d-118">-DefaultProfile</span></span>
<span data-ttu-id="c4d6d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4d6d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4d6d-120">-InputObject</span></span>
<span data-ttu-id="c4d6d-121">Объект шлюза VPN P2S, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d6d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c4d6d-122">-Name</span></span>
<span data-ttu-id="c4d6d-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d6d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d6d-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4d6d-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d6d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4d6d-126">-ResourceId</span></span>
<span data-ttu-id="c4d6d-127">Идентификатор ресурса Azure P2SVpnGateway, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d6d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d6d-128">CommonParameters</span></span>
<span data-ttu-id="c4d6d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4d6d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d6d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d6d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d6d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4d6d-131">INPUTS</span></span>

### <span data-ttu-id="c4d6d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c4d6d-132">System.String</span></span>
<span data-ttu-id="c4d6d-133">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c4d6d-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="c4d6d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4d6d-134">OUTPUTS</span></span>

### <span data-ttu-id="c4d6d-135">Microsoft. Azure. Commands. Network. Models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="c4d6d-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="c4d6d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4d6d-136">NOTES</span></span>

## <span data-ttu-id="c4d6d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4d6d-137">RELATED LINKS</span></span>
