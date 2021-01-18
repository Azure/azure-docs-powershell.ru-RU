---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518833"
---
# <span data-ttu-id="f45af-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f45af-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="f45af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f45af-102">SYNOPSIS</span></span>
<span data-ttu-id="f45af-103">Получить Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f45af-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="f45af-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f45af-104">SYNTAX</span></span>

### <span data-ttu-id="f45af-105">SecurityPartnerProviderNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f45af-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f45af-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f45af-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f45af-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f45af-107">DESCRIPTION</span></span>
<span data-ttu-id="f45af-108">**Cmdlet Get-AzSecurityPartnerProvider** получает Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f45af-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="f45af-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f45af-109">EXAMPLES</span></span>

### <span data-ttu-id="f45af-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f45af-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="f45af-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f45af-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="f45af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f45af-112">PARAMETERS</span></span>

### <span data-ttu-id="f45af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45af-113">-DefaultProfile</span></span>
<span data-ttu-id="f45af-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f45af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f45af-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f45af-115">-Name</span></span>
<span data-ttu-id="f45af-116">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="f45af-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f45af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f45af-117">-ResourceGroupName</span></span>
<span data-ttu-id="f45af-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f45af-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f45af-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f45af-119">-ResourceId</span></span>
<span data-ttu-id="f45af-120">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="f45af-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f45af-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45af-121">CommonParameters</span></span>
<span data-ttu-id="f45af-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f45af-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45af-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f45af-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45af-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f45af-124">INPUTS</span></span>

### <span data-ttu-id="f45af-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f45af-125">System.String</span></span>

## <span data-ttu-id="f45af-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f45af-126">OUTPUTS</span></span>

### <span data-ttu-id="f45af-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f45af-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="f45af-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f45af-128">NOTES</span></span>

## <span data-ttu-id="f45af-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f45af-129">RELATED LINKS</span></span>
