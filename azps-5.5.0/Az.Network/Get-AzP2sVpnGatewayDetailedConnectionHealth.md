---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227841"
---
# <span data-ttu-id="77110-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="77110-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="77110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77110-102">SYNOPSIS</span></span>
<span data-ttu-id="77110-103">Получает подробные сведения о текущих точках подключения к сайтам из P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="77110-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="77110-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77110-104">SYNTAX</span></span>

### <span data-ttu-id="77110-105">ByP2SVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77110-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77110-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="77110-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77110-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="77110-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77110-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77110-108">DESCRIPTION</span></span>
<span data-ttu-id="77110-109">С помощью **cmdlet get-AzP2sVpnGatewayDetailedConnectionHealth** можно получить подробные сведения о текущих точках подключения к сайтам из P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="77110-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="77110-110">Клиенту необходимо пройти URL-адрес SAS, в который мы можем вложить эти подробные сведения о состоянии здоровья.</span><span class="sxs-lookup"><span data-stu-id="77110-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="77110-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77110-111">EXAMPLES</span></span>

### <span data-ttu-id="77110-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77110-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="77110-113">С помощью **cmdlet get-AzP2sVpnGatewayDetailedConnectionHealth** можно получить подробные сведения о текущих точках подключения к сайтам из P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="77110-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="77110-114">Клиент может скачать сведения о состоянии здоровья с url-адреса, который прошел через SAS.</span><span class="sxs-lookup"><span data-stu-id="77110-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="77110-115">При этом будут отсвечены сведения о каждой точке подключения к сайту с именами пользователей, ветвями, в которых были выделены IP-адреса и т. д.</span><span class="sxs-lookup"><span data-stu-id="77110-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="77110-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77110-116">PARAMETERS</span></span>

### <span data-ttu-id="77110-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77110-117">-DefaultProfile</span></span>
<span data-ttu-id="77110-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77110-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77110-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77110-119">-InputObject</span></span>
<span data-ttu-id="77110-120">Объект VPN-шлюза p2s, который нужно изменить</span><span class="sxs-lookup"><span data-stu-id="77110-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="77110-121">-Name</span><span class="sxs-lookup"><span data-stu-id="77110-121">-Name</span></span>
<span data-ttu-id="77110-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="77110-122">The resource name.</span></span>

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

### <span data-ttu-id="77110-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="77110-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="77110-124">Url-адрес OutputBlob Sas, на который будет записано vpn-подключение p2s.</span><span class="sxs-lookup"><span data-stu-id="77110-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="77110-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77110-125">-ResourceGroupName</span></span>
<span data-ttu-id="77110-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77110-126">The resource group name.</span></span>

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

### <span data-ttu-id="77110-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77110-127">-ResourceId</span></span>
<span data-ttu-id="77110-128">ИД ресурсов Azure для P2SVpnGateway, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="77110-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="77110-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="77110-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="77110-130">Список имен пользователей vpn P2S, которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="77110-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77110-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77110-131">CommonParameters</span></span>
<span data-ttu-id="77110-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77110-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77110-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77110-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77110-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77110-134">INPUTS</span></span>

### <span data-ttu-id="77110-135">System.String</span><span class="sxs-lookup"><span data-stu-id="77110-135">System.String</span></span>
<span data-ttu-id="77110-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="77110-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="77110-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77110-137">OUTPUTS</span></span>

### <span data-ttu-id="77110-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="77110-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="77110-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77110-139">NOTES</span></span>

## <span data-ttu-id="77110-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77110-140">RELATED LINKS</span></span>
