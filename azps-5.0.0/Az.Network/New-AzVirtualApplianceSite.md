---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319220"
---
# <span data-ttu-id="4e89a-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4e89a-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="4e89a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e89a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e89a-103">Создание сайта, подключенного к сетевому виртуальному устройству.</span><span class="sxs-lookup"><span data-stu-id="4e89a-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="4e89a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e89a-104">SYNTAX</span></span>

### <span data-ttu-id="4e89a-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e89a-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e89a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e89a-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e89a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e89a-107">DESCRIPTION</span></span>
<span data-ttu-id="4e89a-108">Команда New-AzVirtualApplianceSite создает сайт виртуального устройства, подключенный к ресурсу виртуального сетевого устройства.</span><span class="sxs-lookup"><span data-stu-id="4e89a-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="4e89a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e89a-109">EXAMPLES</span></span>

### <span data-ttu-id="4e89a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e89a-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="4e89a-111">Создайте новый сайт виртуального устройства в группе ресурсов: testrg.</span><span class="sxs-lookup"><span data-stu-id="4e89a-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="4e89a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e89a-112">PARAMETERS</span></span>

### <span data-ttu-id="4e89a-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4e89a-113">-AddressPrefix</span></span>
<span data-ttu-id="4e89a-114">Префикс адреса сайта.</span><span class="sxs-lookup"><span data-stu-id="4e89a-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="4e89a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e89a-115">-AsJob</span></span>
<span data-ttu-id="4e89a-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4e89a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e89a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e89a-117">-DefaultProfile</span></span>
<span data-ttu-id="4e89a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e89a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e89a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4e89a-119">-Force</span></span>
<span data-ttu-id="4e89a-120">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="4e89a-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4e89a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e89a-121">-Name</span></span>
<span data-ttu-id="4e89a-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e89a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e89a-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="4e89a-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="4e89a-124">Сетевое устройство, к которому подключен этот сайт.</span><span class="sxs-lookup"><span data-stu-id="4e89a-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="4e89a-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="4e89a-125">-O365Policy</span></span>
<span data-ttu-id="4e89a-126">Политика помещения Office 365.</span><span class="sxs-lookup"><span data-stu-id="4e89a-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e89a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e89a-127">-ResourceGroupName</span></span>
<span data-ttu-id="4e89a-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e89a-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e89a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e89a-129">-ResourceId</span></span>
<span data-ttu-id="4e89a-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e89a-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e89a-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="4e89a-131">-Tag</span></span>
<span data-ttu-id="4e89a-132">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e89a-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4e89a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e89a-133">-Confirm</span></span>
<span data-ttu-id="4e89a-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e89a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e89a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e89a-135">-WhatIf</span></span>
<span data-ttu-id="4e89a-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e89a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e89a-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e89a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e89a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e89a-138">CommonParameters</span></span>
<span data-ttu-id="4e89a-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e89a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e89a-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e89a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e89a-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e89a-141">INPUTS</span></span>

### <span data-ttu-id="4e89a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4e89a-142">System.String</span></span>

### <span data-ttu-id="4e89a-143">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="4e89a-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="4e89a-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4e89a-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4e89a-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e89a-145">OUTPUTS</span></span>

### <span data-ttu-id="4e89a-146">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4e89a-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="4e89a-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e89a-147">NOTES</span></span>

## <span data-ttu-id="4e89a-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e89a-148">RELATED LINKS</span></span>
