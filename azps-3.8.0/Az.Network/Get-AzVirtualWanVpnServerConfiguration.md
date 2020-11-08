---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: de25e096be96e54d2a8aa18f24bf9915a2f16538
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073546"
---
# <span data-ttu-id="1a169-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a169-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="1a169-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a169-102">SYNOPSIS</span></span>
<span data-ttu-id="1a169-103">Возвращает список всех VpnServerConfigurations, связанных с этим VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="1a169-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="1a169-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a169-104">SYNTAX</span></span>

### <span data-ttu-id="1a169-105">ByVirtualWanName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a169-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a169-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="1a169-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a169-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="1a169-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a169-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a169-108">DESCRIPTION</span></span>
<span data-ttu-id="1a169-109">Командлет **Get-AzVirtualWanVpnServerConfiguration** вернет список всех VpnServerConfigurations, связанных с этим VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="1a169-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="1a169-110">Например, все VpnServerConfigurations, прикрепленные к любому P2SVpnGateways в разделе VirutalHubs этого VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="1a169-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="1a169-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a169-111">EXAMPLES</span></span>

### <span data-ttu-id="1a169-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a169-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="1a169-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a169-113">PARAMETERS</span></span>

### <span data-ttu-id="1a169-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a169-114">-DefaultProfile</span></span>
<span data-ttu-id="1a169-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a169-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a169-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1a169-116">-Name</span></span>
<span data-ttu-id="1a169-117">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a169-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a169-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a169-118">-ResourceGroupName</span></span>
<span data-ttu-id="1a169-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a169-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a169-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a169-120">-ResourceId</span></span>
<span data-ttu-id="1a169-121">Идентификатор ресурса Azure для виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="1a169-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a169-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="1a169-122">-VirtualWanObject</span></span>
<span data-ttu-id="1a169-123">Виртуальный объект глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="1a169-123">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a169-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a169-124">CommonParameters</span></span>
<span data-ttu-id="1a169-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a169-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a169-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a169-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a169-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a169-127">INPUTS</span></span>

### <span data-ttu-id="1a169-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1a169-128">System.String</span></span>
<span data-ttu-id="1a169-129">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1a169-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="1a169-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a169-130">OUTPUTS</span></span>

### <span data-ttu-id="1a169-131">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="1a169-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="1a169-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a169-132">NOTES</span></span>

## <span data-ttu-id="1a169-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a169-133">RELATED LINKS</span></span>
