---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237009"
---
# <span data-ttu-id="0a039-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0a039-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="0a039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a039-102">SYNOPSIS</span></span>
<span data-ttu-id="0a039-103">Возвращает ресурс CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0a039-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="0a039-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a039-104">SYNTAX</span></span>

### <span data-ttu-id="0a039-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a039-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a039-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a039-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a039-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a039-107">DESCRIPTION</span></span>
<span data-ttu-id="0a039-108">С учетом набора входных параметров cmdlet **Get-AzCustomIpPrefix** получает один или несколько customIpPrefixes.</span><span class="sxs-lookup"><span data-stu-id="0a039-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="0a039-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a039-109">EXAMPLES</span></span>

### <span data-ttu-id="0a039-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a039-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="0a039-111">Эта команда получает ресурс CustomIpPrefix с именем myCustomIpPrefix в группе ресурсов myRg</span><span class="sxs-lookup"><span data-stu-id="0a039-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="0a039-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a039-112">PARAMETERS</span></span>

### <span data-ttu-id="0a039-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a039-113">-DefaultProfile</span></span>
<span data-ttu-id="0a039-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a039-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a039-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0a039-115">-Name</span></span>
<span data-ttu-id="0a039-116">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a039-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a039-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a039-117">-ResourceGroupName</span></span>
<span data-ttu-id="0a039-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a039-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a039-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a039-119">-ResourceId</span></span>
<span data-ttu-id="0a039-120">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a039-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a039-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a039-121">CommonParameters</span></span>
<span data-ttu-id="0a039-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a039-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a039-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a039-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a039-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a039-124">INPUTS</span></span>

### <span data-ttu-id="0a039-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0a039-125">System.String</span></span>

## <span data-ttu-id="0a039-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a039-126">OUTPUTS</span></span>

### <span data-ttu-id="0a039-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0a039-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="0a039-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a039-128">NOTES</span></span>

## <span data-ttu-id="0a039-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a039-129">RELATED LINKS</span></span>

[<span data-ttu-id="0a039-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0a039-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="0a039-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0a039-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="0a039-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0a039-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)