---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397383"
---
# <span data-ttu-id="0d442-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d442-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="0d442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d442-102">SYNOPSIS</span></span>
<span data-ttu-id="0d442-103">Возвращает список всех gurations VpnServerConfigurations, связанных с этой виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="0d442-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="0d442-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0d442-104">SYNTAX</span></span>

### <span data-ttu-id="0d442-105">ByVirtualWanName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d442-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d442-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="0d442-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d442-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="0d442-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d442-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d442-108">DESCRIPTION</span></span>
<span data-ttu-id="0d442-109">Cmdlet **Get-AzVirtualWanVpnServerConfiguration** возвращает список всех буклетов VpnServerConfiguration, связанных с этой виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="0d442-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="0d442-110">Т. е. Все vpnServerConfigurations, которые прикреплены к любым P2SVpnGateways в VirutalHubs этой виртуальнойwan.</span><span class="sxs-lookup"><span data-stu-id="0d442-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="0d442-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0d442-111">EXAMPLES</span></span>

### <span data-ttu-id="0d442-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d442-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="0d442-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d442-113">PARAMETERS</span></span>

### <span data-ttu-id="0d442-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d442-114">-DefaultProfile</span></span>
<span data-ttu-id="0d442-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d442-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d442-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0d442-116">-Name</span></span>
<span data-ttu-id="0d442-117">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d442-117">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d442-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d442-118">-ResourceGroupName</span></span>
<span data-ttu-id="0d442-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d442-119">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d442-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d442-120">-ResourceId</span></span>
<span data-ttu-id="0d442-121">ИД ресурсов Azure для виртуальной wan.</span><span class="sxs-lookup"><span data-stu-id="0d442-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d442-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="0d442-122">-VirtualWanObject</span></span>
<span data-ttu-id="0d442-123">Объект виртуальной wan.</span><span class="sxs-lookup"><span data-stu-id="0d442-123">The virtual wan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d442-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d442-124">CommonParameters</span></span>
<span data-ttu-id="0d442-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d442-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d442-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d442-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d442-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d442-127">INPUTS</span></span>

### <span data-ttu-id="0d442-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0d442-128">System.String</span></span>
<span data-ttu-id="0d442-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0d442-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="0d442-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0d442-130">OUTPUTS</span></span>

### <span data-ttu-id="0d442-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="0d442-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="0d442-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0d442-132">NOTES</span></span>

## <span data-ttu-id="0d442-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d442-133">RELATED LINKS</span></span>
