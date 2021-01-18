---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518129"
---
# <span data-ttu-id="e52cb-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e52cb-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="e52cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e52cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e52cb-103">Получает политику брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="e52cb-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="e52cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e52cb-104">SYNTAX</span></span>

### <span data-ttu-id="e52cb-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e52cb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e52cb-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e52cb-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e52cb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e52cb-107">DESCRIPTION</span></span>
<span data-ttu-id="e52cb-108">С **помощью cmdlet Get-AzFirewallPolicy** можно получить один или несколько брандмауэров в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e52cb-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="e52cb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e52cb-109">EXAMPLES</span></span>

### <span data-ttu-id="e52cb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e52cb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="e52cb-111">В этом примере в группе ресурсов TestRg есть брандмауэр с именем firewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="e52cb-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="e52cb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e52cb-112">PARAMETERS</span></span>

### <span data-ttu-id="e52cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e52cb-113">-DefaultProfile</span></span>
<span data-ttu-id="e52cb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e52cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e52cb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e52cb-115">-Name</span></span>
<span data-ttu-id="e52cb-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e52cb-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e52cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e52cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="e52cb-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e52cb-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e52cb-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e52cb-119">-ResourceId</span></span>
<span data-ttu-id="e52cb-120">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="e52cb-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e52cb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e52cb-121">CommonParameters</span></span>
<span data-ttu-id="e52cb-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e52cb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e52cb-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e52cb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e52cb-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e52cb-124">INPUTS</span></span>

### <span data-ttu-id="e52cb-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e52cb-125">System.String</span></span>

## <span data-ttu-id="e52cb-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e52cb-126">OUTPUTS</span></span>

### <span data-ttu-id="e52cb-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e52cb-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="e52cb-128">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e52cb-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e52cb-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e52cb-129">NOTES</span></span>

## <span data-ttu-id="e52cb-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e52cb-130">RELATED LINKS</span></span>
