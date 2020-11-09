---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248831"
---
# <span data-ttu-id="827ae-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="827ae-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="827ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="827ae-102">SYNOPSIS</span></span>
<span data-ttu-id="827ae-103">Создание частной группы DNS зоны в указанной частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="827ae-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="827ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="827ae-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="827ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="827ae-105">DESCRIPTION</span></span>
<span data-ttu-id="827ae-106">С помощью командлета **New-AzPrivateDnsZoneGroup** вы можете создать новую группу зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="827ae-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="827ae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="827ae-107">EXAMPLES</span></span>

### <span data-ttu-id="827ae-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="827ae-108">Example 1</span></span>
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

<span data-ttu-id="827ae-109">После создания частной конечной точки `test-pr-endpoint` в приведенном выше примере группа зон DNS создается в этой частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="827ae-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="827ae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="827ae-110">PARAMETERS</span></span>

### <span data-ttu-id="827ae-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="827ae-111">-AsJob</span></span>
<span data-ttu-id="827ae-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="827ae-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="827ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827ae-113">-DefaultProfile</span></span>
<span data-ttu-id="827ae-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="827ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="827ae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="827ae-115">-Force</span></span>
<span data-ttu-id="827ae-116">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="827ae-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="827ae-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="827ae-117">-Name</span></span>
<span data-ttu-id="827ae-118">Имя частной группы зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="827ae-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="827ae-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="827ae-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="827ae-120">Набор частных конфигураций зон DNS для частной группы зон DNS.</span><span class="sxs-lookup"><span data-stu-id="827ae-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="827ae-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="827ae-121">-PrivateEndpointName</span></span>
<span data-ttu-id="827ae-122">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="827ae-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="827ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="827ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="827ae-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="827ae-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="827ae-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="827ae-125">-Confirm</span></span>
<span data-ttu-id="827ae-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="827ae-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="827ae-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="827ae-127">-WhatIf</span></span>
<span data-ttu-id="827ae-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="827ae-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="827ae-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="827ae-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="827ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827ae-130">CommonParameters</span></span>
<span data-ttu-id="827ae-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="827ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827ae-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="827ae-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827ae-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="827ae-133">INPUTS</span></span>

### <span data-ttu-id="827ae-134">System. String</span><span class="sxs-lookup"><span data-stu-id="827ae-134">System.String</span></span>

### <span data-ttu-id="827ae-135">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. командлеты. Network, Version = 2.5.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="827ae-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="827ae-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="827ae-136">OUTPUTS</span></span>

### <span data-ttu-id="827ae-137">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="827ae-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="827ae-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="827ae-138">NOTES</span></span>

## <span data-ttu-id="827ae-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="827ae-139">RELATED LINKS</span></span>