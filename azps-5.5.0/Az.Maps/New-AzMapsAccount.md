---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221513"
---
# <span data-ttu-id="95cc3-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="95cc3-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="95cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="95cc3-103">Создает учетную запись Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="95cc3-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="95cc3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95cc3-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95cc3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="95cc3-106">С New-AzMapsAccount создается учетная запись Azure Maps с указанным SKU.</span><span class="sxs-lookup"><span data-stu-id="95cc3-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="95cc3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95cc3-107">EXAMPLES</span></span>

### <span data-ttu-id="95cc3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95cc3-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="95cc3-109">Создает новую учетную запись Azure Maps с именем MyAccount в группе ресурсов MyResourceGroup с SKU S0 и тегом.</span><span class="sxs-lookup"><span data-stu-id="95cc3-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="95cc3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95cc3-110">PARAMETERS</span></span>

### <span data-ttu-id="95cc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95cc3-111">-DefaultProfile</span></span>
<span data-ttu-id="95cc3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95cc3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95cc3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="95cc3-113">-Force</span></span>
<span data-ttu-id="95cc3-114">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="95cc3-114">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95cc3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="95cc3-115">-Name</span></span>
<span data-ttu-id="95cc3-116">Имя учетной записи Карты.</span><span class="sxs-lookup"><span data-stu-id="95cc3-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95cc3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95cc3-117">-ResourceGroupName</span></span>
<span data-ttu-id="95cc3-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95cc3-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95cc3-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="95cc3-119">-SkuName</span></span>
<span data-ttu-id="95cc3-120">Имя SKU учетной записи Карты.</span><span class="sxs-lookup"><span data-stu-id="95cc3-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95cc3-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="95cc3-121">-Tag</span></span>
<span data-ttu-id="95cc3-122">Теги учетной записи Карты.</span><span class="sxs-lookup"><span data-stu-id="95cc3-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95cc3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95cc3-123">-Confirm</span></span>
<span data-ttu-id="95cc3-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="95cc3-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95cc3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95cc3-125">-WhatIf</span></span>
<span data-ttu-id="95cc3-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95cc3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95cc3-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="95cc3-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95cc3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95cc3-128">CommonParameters</span></span>
<span data-ttu-id="95cc3-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95cc3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95cc3-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95cc3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95cc3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95cc3-131">INPUTS</span></span>

### <span data-ttu-id="95cc3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="95cc3-132">System.String</span></span>

## <span data-ttu-id="95cc3-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95cc3-133">OUTPUTS</span></span>

### <span data-ttu-id="95cc3-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="95cc3-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="95cc3-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95cc3-135">NOTES</span></span>

## <span data-ttu-id="95cc3-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95cc3-136">RELATED LINKS</span></span>
