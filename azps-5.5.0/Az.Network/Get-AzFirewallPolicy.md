---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227932"
---
# <span data-ttu-id="35600-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="35600-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="35600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35600-102">SYNOPSIS</span></span>
<span data-ttu-id="35600-103">Получает политику брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="35600-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="35600-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35600-104">SYNTAX</span></span>

### <span data-ttu-id="35600-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35600-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35600-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35600-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35600-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35600-107">DESCRIPTION</span></span>
<span data-ttu-id="35600-108">С **помощью cmdlet Get-AzFirewallPolicy** можно получить один или несколько брандмауэров в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35600-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="35600-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35600-109">EXAMPLES</span></span>

### <span data-ttu-id="35600-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35600-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="35600-111">В этом примере в группе ресурсов TestRg есть брандмауэр с именем firewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="35600-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="35600-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35600-112">PARAMETERS</span></span>

### <span data-ttu-id="35600-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35600-113">-DefaultProfile</span></span>
<span data-ttu-id="35600-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35600-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35600-115">-Name</span><span class="sxs-lookup"><span data-stu-id="35600-115">-Name</span></span>
<span data-ttu-id="35600-116">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="35600-116">The resource name.</span></span>

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

### <span data-ttu-id="35600-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35600-117">-ResourceGroupName</span></span>
<span data-ttu-id="35600-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35600-118">The resource group name.</span></span>

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

### <span data-ttu-id="35600-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35600-119">-ResourceId</span></span>
<span data-ttu-id="35600-120">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="35600-120">The resource Id.</span></span>

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

### <span data-ttu-id="35600-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35600-121">CommonParameters</span></span>
<span data-ttu-id="35600-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35600-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35600-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35600-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35600-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35600-124">INPUTS</span></span>

### <span data-ttu-id="35600-125">System.String</span><span class="sxs-lookup"><span data-stu-id="35600-125">System.String</span></span>

## <span data-ttu-id="35600-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35600-126">OUTPUTS</span></span>

### <span data-ttu-id="35600-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="35600-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="35600-128">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="35600-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="35600-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35600-129">NOTES</span></span>

## <span data-ttu-id="35600-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35600-130">RELATED LINKS</span></span>
