---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505518"
---
# <span data-ttu-id="0773f-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="0773f-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="0773f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0773f-102">SYNOPSIS</span></span>
<span data-ttu-id="0773f-103">Создает частную группу зоны DNS в указанной закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="0773f-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="0773f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0773f-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0773f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0773f-105">DESCRIPTION</span></span>
<span data-ttu-id="0773f-106">С **помощью cmdlet New-AzPrivateDnsZoneGroup** можно создать новую частную группу зон DNS.</span><span class="sxs-lookup"><span data-stu-id="0773f-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="0773f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0773f-107">EXAMPLES</span></span>

### <span data-ttu-id="0773f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0773f-108">Example 1</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
PS C:\> New-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1" -PrivateDnsZoneConfig $config -Force
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="0773f-109">После создания закрытой конечной точки над примером создается группа зоны DNS в этой частной `test-pr-endpoint` конечной точке.</span><span class="sxs-lookup"><span data-stu-id="0773f-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="0773f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0773f-110">PARAMETERS</span></span>

### <span data-ttu-id="0773f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0773f-111">-AsJob</span></span>
<span data-ttu-id="0773f-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0773f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0773f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0773f-113">-DefaultProfile</span></span>
<span data-ttu-id="0773f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0773f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0773f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0773f-115">-Force</span></span>
<span data-ttu-id="0773f-116">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="0773f-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0773f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0773f-117">-Name</span></span>
<span data-ttu-id="0773f-118">Имя закрытой группы зон DNS.</span><span class="sxs-lookup"><span data-stu-id="0773f-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0773f-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="0773f-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="0773f-120">Набор личных конфигураций зоны DNS закрытой группы зон DNS.</span><span class="sxs-lookup"><span data-stu-id="0773f-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0773f-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="0773f-121">-PrivateEndpointName</span></span>
<span data-ttu-id="0773f-122">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="0773f-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="0773f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0773f-123">-ResourceGroupName</span></span>
<span data-ttu-id="0773f-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0773f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="0773f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0773f-125">-Confirm</span></span>
<span data-ttu-id="0773f-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0773f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0773f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0773f-127">-WhatIf</span></span>
<span data-ttu-id="0773f-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0773f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0773f-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0773f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0773f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0773f-130">CommonParameters</span></span>
<span data-ttu-id="0773f-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0773f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0773f-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0773f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0773f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0773f-133">INPUTS</span></span>

### <span data-ttu-id="0773f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0773f-134">System.String</span></span>

### <span data-ttu-id="0773f-135">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0773f-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0773f-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0773f-136">OUTPUTS</span></span>

### <span data-ttu-id="0773f-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="0773f-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="0773f-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0773f-138">NOTES</span></span>

## <span data-ttu-id="0773f-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0773f-139">RELATED LINKS</span></span>
