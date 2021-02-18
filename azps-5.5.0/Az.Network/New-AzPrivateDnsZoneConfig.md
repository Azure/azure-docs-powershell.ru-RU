---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218476"
---
# <span data-ttu-id="97e80-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="97e80-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="97e80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e80-102">SYNOPSIS</span></span>
<span data-ttu-id="97e80-103">Создает конфигурацию зоны DNS для закрытой группы зон DNS.</span><span class="sxs-lookup"><span data-stu-id="97e80-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="97e80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97e80-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97e80-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97e80-105">DESCRIPTION</span></span>
<span data-ttu-id="97e80-106">С **помощью cmdlet New-AzPrivateDnsZoneConfig** можно создать новый объект конфигурации зоны DNS, который будет установлен в группе зон DNS.</span><span class="sxs-lookup"><span data-stu-id="97e80-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="97e80-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97e80-107">EXAMPLES</span></span>

### <span data-ttu-id="97e80-108">Создает конфигурацию зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="97e80-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="97e80-109">В примере выше создается зона DNS, а затем создается конфигурация зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="97e80-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="97e80-110">`New-AzPrivateDnsZone` Командлет доказуется модулем Az.PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="97e80-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="97e80-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97e80-111">PARAMETERS</span></span>

### <span data-ttu-id="97e80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e80-112">-DefaultProfile</span></span>
<span data-ttu-id="97e80-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97e80-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97e80-114">-Name</span><span class="sxs-lookup"><span data-stu-id="97e80-114">-Name</span></span>
<span data-ttu-id="97e80-115">Имя ресурса, уникального в составе группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97e80-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="97e80-116">Это имя может использоваться для доступа к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="97e80-116">This name can be used to access the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e80-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="97e80-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="97e80-118">ИД ресурса частной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="97e80-118">The resource id of the private dns zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e80-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e80-119">CommonParameters</span></span>
<span data-ttu-id="97e80-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97e80-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e80-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97e80-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e80-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97e80-122">INPUTS</span></span>

### <span data-ttu-id="97e80-123">Нет</span><span class="sxs-lookup"><span data-stu-id="97e80-123">None</span></span>

## <span data-ttu-id="97e80-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97e80-124">OUTPUTS</span></span>

### <span data-ttu-id="97e80-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="97e80-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="97e80-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97e80-126">NOTES</span></span>

## <span data-ttu-id="97e80-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97e80-127">RELATED LINKS</span></span>
