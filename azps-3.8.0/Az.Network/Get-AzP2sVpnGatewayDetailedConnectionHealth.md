---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064833"
---
# <span data-ttu-id="83226-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="83226-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="83226-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83226-102">SYNOPSIS</span></span>
<span data-ttu-id="83226-103">Получает подробные сведения о текущих точках на подключения к сайту из P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="83226-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="83226-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83226-104">SYNTAX</span></span>

### <span data-ttu-id="83226-105">ByP2SVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83226-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83226-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="83226-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83226-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="83226-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83226-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83226-108">DESCRIPTION</span></span>
<span data-ttu-id="83226-109">Командлет **Get-AzP2sVpnGatewayDetailedConnectionHealth** позволяет получить подробные сведения о текущей точке подключения к сайту из P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="83226-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="83226-110">Клиенту необходимо передать URL-адрес SAS, в который мы можем разместить подробные сведения о работоспособности.</span><span class="sxs-lookup"><span data-stu-id="83226-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="83226-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83226-111">EXAMPLES</span></span>

### <span data-ttu-id="83226-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="83226-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="83226-113">Командлет **Get-AzP2sVpnGatewayDetailedConnectionHealth** позволяет получить подробные сведения о текущей точке подключения к сайту из P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="83226-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="83226-114">Пользователь может загрузить сведения о работоспособности из скачанного URL-адреса SAS.</span><span class="sxs-lookup"><span data-stu-id="83226-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="83226-115">Будут показаны сведения о подключении к сайту с именами пользователей, байтами, байтами, выделенными IP-адресами и т. д.</span><span class="sxs-lookup"><span data-stu-id="83226-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="83226-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83226-116">PARAMETERS</span></span>

### <span data-ttu-id="83226-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83226-117">-DefaultProfile</span></span>
<span data-ttu-id="83226-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83226-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83226-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83226-119">-InputObject</span></span>
<span data-ttu-id="83226-120">Объект шлюза VPN P2S, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="83226-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="83226-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="83226-121">-Name</span></span>
<span data-ttu-id="83226-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="83226-122">The resource name.</span></span>

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

### <span data-ttu-id="83226-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="83226-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="83226-124">URL-адрес SAS OutputBlob, на который будет записываться проверка работоспособности VPN-соединения P2S.</span><span class="sxs-lookup"><span data-stu-id="83226-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="83226-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83226-125">-ResourceGroupName</span></span>
<span data-ttu-id="83226-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83226-126">The resource group name.</span></span>

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

### <span data-ttu-id="83226-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83226-127">-ResourceId</span></span>
<span data-ttu-id="83226-128">Идентификатор ресурса Azure P2SVpnGateway, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="83226-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="83226-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="83226-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="83226-130">Список имен P2S VPN-пользователей, которые нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="83226-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="83226-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83226-131">CommonParameters</span></span>
<span data-ttu-id="83226-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83226-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83226-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83226-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83226-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83226-134">INPUTS</span></span>

### <span data-ttu-id="83226-135">System. String</span><span class="sxs-lookup"><span data-stu-id="83226-135">System.String</span></span>
<span data-ttu-id="83226-136">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="83226-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="83226-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83226-137">OUTPUTS</span></span>

### <span data-ttu-id="83226-138">Microsoft. Azure. Commands. Network. Models. PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="83226-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="83226-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="83226-139">NOTES</span></span>

## <span data-ttu-id="83226-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83226-140">RELATED LINKS</span></span>
