---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912578"
---
# <span data-ttu-id="810fe-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="810fe-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="810fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="810fe-102">SYNOPSIS</span></span>
<span data-ttu-id="810fe-103">Создает и загружает профиль VPN на уровне VirtualWan-VpnServerConfiguration для настройки клиента точки на сайте.</span><span class="sxs-lookup"><span data-stu-id="810fe-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="810fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="810fe-104">SYNTAX</span></span>

### <span data-ttu-id="810fe-105">ByVirtualWanNameByVpnServerConfigurationObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="810fe-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="810fe-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="810fe-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="810fe-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="810fe-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="810fe-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="810fe-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="810fe-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="810fe-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="810fe-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="810fe-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="810fe-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="810fe-111">DESCRIPTION</span></span>
<span data-ttu-id="810fe-112">Командлет **Get-AzVirtualWanVpnServerConfigurationVpnProfile** позволяет создавать и скачивать профиль VPN на уровне VirtualWan-VpnServerConfiguration для настройки клиента точки на сайте.</span><span class="sxs-lookup"><span data-stu-id="810fe-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="810fe-113">Это необходимо для того, чтобы указать для подключения к сайту значение "клиент" для Azure P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="810fe-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="810fe-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="810fe-114">EXAMPLES</span></span>

### <span data-ttu-id="810fe-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="810fe-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="810fe-116">Эта команда создаст и возвращает URL-адрес SAS для клиента, чтобы скачать профиль VPN на уровне VirtualWan-VpnServerConfiguration для настройки клиента на сайте.</span><span class="sxs-lookup"><span data-stu-id="810fe-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="810fe-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="810fe-117">PARAMETERS</span></span>

### <span data-ttu-id="810fe-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="810fe-118">-AuthenticationMethod</span></span>
<span data-ttu-id="810fe-119">Способ проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="810fe-119">Authentication Method</span></span>

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

### <span data-ttu-id="810fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="810fe-120">-DefaultProfile</span></span>
<span data-ttu-id="810fe-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="810fe-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="810fe-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="810fe-122">-Name</span></span>
<span data-ttu-id="810fe-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="810fe-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="810fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="810fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="810fe-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="810fe-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="810fe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="810fe-126">-ResourceId</span></span>
<span data-ttu-id="810fe-127">Идентификатор ресурса Azure для виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="810fe-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="810fe-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="810fe-128">-VirtualWanObject</span></span>
<span data-ttu-id="810fe-129">Виртуальный объект глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="810fe-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="810fe-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="810fe-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="810fe-131">VpnServerConfiguration, с которым связан этот VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="810fe-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="810fe-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="810fe-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="810fe-133">Идентификатор объекта configuraiton VPN-сервера, с которым будет связана эта виртуальная Глобальная сеть.</span><span class="sxs-lookup"><span data-stu-id="810fe-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="810fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="810fe-134">CommonParameters</span></span>
<span data-ttu-id="810fe-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="810fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="810fe-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="810fe-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="810fe-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="810fe-137">INPUTS</span></span>

### <span data-ttu-id="810fe-138">System. String</span><span class="sxs-lookup"><span data-stu-id="810fe-138">System.String</span></span>
<span data-ttu-id="810fe-139">Microsoft. Azure. Commands. Network. Models. PSVirtualWan Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="810fe-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="810fe-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="810fe-140">OUTPUTS</span></span>

### <span data-ttu-id="810fe-141">Microsoft. Azure. Commands. Network. Models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="810fe-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="810fe-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="810fe-142">NOTES</span></span>

## <span data-ttu-id="810fe-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="810fe-143">RELATED LINKS</span></span>
