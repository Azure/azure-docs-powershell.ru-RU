---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327099"
---
# <span data-ttu-id="ac450-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="ac450-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="ac450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac450-102">SYNOPSIS</span></span>
<span data-ttu-id="ac450-103">Создает и возвращает URL-адрес SAS для скачивания профиля VPN, чтобы указать на конфигурацию клиента сайта, чтобы указать на подключение сайта к P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="ac450-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="ac450-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac450-104">SYNTAX</span></span>

### <span data-ttu-id="ac450-105">ByP2SVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac450-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac450-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ac450-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac450-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ac450-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac450-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac450-108">DESCRIPTION</span></span>
<span data-ttu-id="ac450-109">С помощью **cmdlet get-AzP2sVpnGatewayVpnProfile** можно создать и получить URL-адрес SAS, позволяющий скачать профиль VPN, чтобы навести указатель на конфигурацию клиента сайта, чтобы указать на подключение к сайту P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="ac450-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="ac450-110">Навести указатель на настройку клиента сайта с помощью этого профиля VPN, можно подключиться только к этому конкретному P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="ac450-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="ac450-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac450-111">EXAMPLES</span></span>

### <span data-ttu-id="ac450-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac450-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="ac450-113">С помощью **cmdlet get-AzP2sVpnGatewayVpnProfile** можно создать и получить URL-адрес SAS для клиента, чтобы скачать профиль VPN, чтобы навести указатель на конфигурацию клиента сайта, чтобы указать на подключение сайта к P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="ac450-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="ac450-114">В профиле ProfileUrl показан URL-адрес SAS, с помощью которой клиент может скачать vpn-профиль, чтобы указать на настройку клиента сайта.</span><span class="sxs-lookup"><span data-stu-id="ac450-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="ac450-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac450-115">PARAMETERS</span></span>

### <span data-ttu-id="ac450-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="ac450-116">-AuthenticationMethod</span></span>
<span data-ttu-id="ac450-117">Способ проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="ac450-117">Authentication Method</span></span>

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

### <span data-ttu-id="ac450-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac450-118">-DefaultProfile</span></span>
<span data-ttu-id="ac450-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac450-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac450-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac450-120">-InputObject</span></span>
<span data-ttu-id="ac450-121">Объект VPN-шлюза p2s, который нужно изменить</span><span class="sxs-lookup"><span data-stu-id="ac450-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="ac450-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ac450-122">-Name</span></span>
<span data-ttu-id="ac450-123">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="ac450-123">The resource name.</span></span>

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

### <span data-ttu-id="ac450-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac450-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac450-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac450-125">The resource group name.</span></span>

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

### <span data-ttu-id="ac450-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac450-126">-ResourceId</span></span>
<span data-ttu-id="ac450-127">ИД ресурсов Azure для P2SVpnGateway, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="ac450-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="ac450-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac450-128">CommonParameters</span></span>
<span data-ttu-id="ac450-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac450-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac450-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac450-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac450-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac450-131">INPUTS</span></span>

### <span data-ttu-id="ac450-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ac450-132">System.String</span></span>
<span data-ttu-id="ac450-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ac450-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="ac450-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac450-134">OUTPUTS</span></span>

### <span data-ttu-id="ac450-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="ac450-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="ac450-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac450-136">NOTES</span></span>

## <span data-ttu-id="ac450-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac450-137">RELATED LINKS</span></span>
