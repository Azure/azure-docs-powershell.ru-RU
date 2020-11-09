---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244115"
---
# <span data-ttu-id="64728-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="64728-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="64728-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64728-102">SYNOPSIS</span></span>
<span data-ttu-id="64728-103">Создание Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="64728-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="64728-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64728-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64728-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64728-105">DESCRIPTION</span></span>
<span data-ttu-id="64728-106">Командлет **New-AzSecurityPartnerProvider** создает Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="64728-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="64728-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64728-107">EXAMPLES</span></span>

### <span data-ttu-id="64728-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="64728-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="64728-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64728-109">PARAMETERS</span></span>

### <span data-ttu-id="64728-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64728-110">-AsJob</span></span>
<span data-ttu-id="64728-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="64728-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64728-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64728-112">-DefaultProfile</span></span>
<span data-ttu-id="64728-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64728-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64728-114">-Force</span><span class="sxs-lookup"><span data-stu-id="64728-114">-Force</span></span>
<span data-ttu-id="64728-115">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="64728-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64728-116">-Location</span><span class="sxs-lookup"><span data-stu-id="64728-116">-Location</span></span>
<span data-ttu-id="64728-117">поиска.</span><span class="sxs-lookup"><span data-stu-id="64728-117">location.</span></span>

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

### <span data-ttu-id="64728-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="64728-118">-Name</span></span>
<span data-ttu-id="64728-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="64728-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64728-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64728-120">-ResourceGroupName</span></span>
<span data-ttu-id="64728-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64728-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64728-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="64728-122">-SecurityProviderName</span></span>
<span data-ttu-id="64728-123">Имя поставщика услуг безопасности</span><span class="sxs-lookup"><span data-stu-id="64728-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64728-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="64728-124">-Tag</span></span>
<span data-ttu-id="64728-125">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64728-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64728-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="64728-126">-VirtualHub</span></span>
<span data-ttu-id="64728-127">Идентификатор виртуального концентратора, к которому присоединен поставщик партнера по безопасности</span><span class="sxs-lookup"><span data-stu-id="64728-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64728-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="64728-128">-VirtualHubId</span></span>
<span data-ttu-id="64728-129">Идентификатор VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="64728-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64728-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="64728-130">-VirtualHubName</span></span>
<span data-ttu-id="64728-131">Идентификатор VirtualHub, с которым должен быть связан этот VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="64728-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="64728-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64728-132">-Confirm</span></span>
<span data-ttu-id="64728-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64728-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64728-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64728-134">-WhatIf</span></span>
<span data-ttu-id="64728-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64728-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64728-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64728-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64728-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64728-137">CommonParameters</span></span>
<span data-ttu-id="64728-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64728-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64728-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64728-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64728-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64728-140">INPUTS</span></span>

### <span data-ttu-id="64728-141">System. String</span><span class="sxs-lookup"><span data-stu-id="64728-141">System.String</span></span>

### <span data-ttu-id="64728-142">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="64728-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="64728-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="64728-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="64728-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64728-144">OUTPUTS</span></span>

### <span data-ttu-id="64728-145">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="64728-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="64728-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="64728-146">NOTES</span></span>

## <span data-ttu-id="64728-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64728-147">RELATED LINKS</span></span>