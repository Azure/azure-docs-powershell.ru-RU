---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244309"
---
# <span data-ttu-id="6554b-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="6554b-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="6554b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6554b-102">SYNOPSIS</span></span>
<span data-ttu-id="6554b-103">Изменение или изменение сайта виртуального устройства, подключенного к ресурсу сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="6554b-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6554b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6554b-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6554b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6554b-105">DESCRIPTION</span></span>
<span data-ttu-id="6554b-106">Команда Update-AzVirtualApplianceSite изменяет ресурс сайта виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="6554b-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="6554b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6554b-107">EXAMPLES</span></span>

### <span data-ttu-id="6554b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6554b-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="6554b-109">Измените префикс адреса ресурса сайта виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="6554b-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="6554b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6554b-110">PARAMETERS</span></span>

### <span data-ttu-id="6554b-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="6554b-111">-AddresssPrefix</span></span>
<span data-ttu-id="6554b-112">Префикс адреса сайта.</span><span class="sxs-lookup"><span data-stu-id="6554b-112">The address prefix for the site.</span></span>

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

### <span data-ttu-id="6554b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6554b-113">-AsJob</span></span>
<span data-ttu-id="6554b-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6554b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6554b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6554b-115">-DefaultProfile</span></span>
<span data-ttu-id="6554b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6554b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6554b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6554b-117">-Force</span></span>
<span data-ttu-id="6554b-118">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="6554b-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6554b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6554b-119">-Name</span></span>
<span data-ttu-id="6554b-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="6554b-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6554b-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="6554b-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="6554b-122">Сетевое устройство, к которому подключен этот сайт.</span><span class="sxs-lookup"><span data-stu-id="6554b-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="6554b-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="6554b-123">-O365Policy</span></span>
<span data-ttu-id="6554b-124">Политика помещения Office 365.</span><span class="sxs-lookup"><span data-stu-id="6554b-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6554b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6554b-125">-ResourceGroupName</span></span>
<span data-ttu-id="6554b-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6554b-126">The resource group name.</span></span>

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

### <span data-ttu-id="6554b-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="6554b-127">-Tag</span></span>
<span data-ttu-id="6554b-128">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6554b-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6554b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6554b-129">-Confirm</span></span>
<span data-ttu-id="6554b-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6554b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6554b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6554b-131">-WhatIf</span></span>
<span data-ttu-id="6554b-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6554b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6554b-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6554b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6554b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6554b-134">CommonParameters</span></span>
<span data-ttu-id="6554b-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6554b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6554b-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6554b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6554b-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6554b-137">INPUTS</span></span>

### <span data-ttu-id="6554b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6554b-138">System.String</span></span>

### <span data-ttu-id="6554b-139">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="6554b-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="6554b-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6554b-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6554b-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6554b-141">OUTPUTS</span></span>

### <span data-ttu-id="6554b-142">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="6554b-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="6554b-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="6554b-143">NOTES</span></span>

## <span data-ttu-id="6554b-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6554b-144">RELATED LINKS</span></span>
