---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 9b9ab59496ff52be2dc8ca538ea044ec34c34970
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248819"
---
# <span data-ttu-id="76794-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="76794-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="76794-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76794-102">SYNOPSIS</span></span>
<span data-ttu-id="76794-103">Удаление ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="76794-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="76794-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76794-104">SYNTAX</span></span>

### <span data-ttu-id="76794-105">ByVpnSiteName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76794-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76794-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="76794-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76794-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="76794-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76794-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76794-108">DESCRIPTION</span></span>
<span data-ttu-id="76794-109">Удаление ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="76794-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="76794-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76794-110">EXAMPLES</span></span>

### <span data-ttu-id="76794-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76794-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="76794-112">В приведенном выше примере будет создана группа ресурсов, Виртуальная глобальная сеть в Запад США в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="76794-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="76794-113">Затем он создает VpnSite для представления ветви клиента и связывает ее с виртуальной глобальной сетью.</span><span class="sxs-lookup"><span data-stu-id="76794-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="76794-114">После создания сайта немедленно удаляется с помощью команды Remove-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="76794-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="76794-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="76794-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="76794-116">То же, что и в примере 1, но удаление происходит при использовании вывода из команды Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="76794-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="76794-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76794-117">PARAMETERS</span></span>

### <span data-ttu-id="76794-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76794-118">-DefaultProfile</span></span>
<span data-ttu-id="76794-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76794-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76794-120">-Force</span><span class="sxs-lookup"><span data-stu-id="76794-120">-Force</span></span>
<span data-ttu-id="76794-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="76794-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76794-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76794-122">-InputObject</span></span>
<span data-ttu-id="76794-123">Объект vpnSite, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="76794-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76794-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76794-124">-Name</span></span>
<span data-ttu-id="76794-125">Имя vpnSite.</span><span class="sxs-lookup"><span data-stu-id="76794-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76794-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76794-126">-PassThru</span></span>
<span data-ttu-id="76794-127">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="76794-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="76794-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="76794-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76794-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76794-129">-ResourceGroupName</span></span>
<span data-ttu-id="76794-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76794-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76794-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76794-131">-ResourceId</span></span>
<span data-ttu-id="76794-132">Идентификатор ресурса Azure для vpnSite, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="76794-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76794-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76794-133">-Confirm</span></span>
<span data-ttu-id="76794-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76794-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76794-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76794-135">-WhatIf</span></span>
<span data-ttu-id="76794-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76794-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76794-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76794-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76794-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76794-138">CommonParameters</span></span>
<span data-ttu-id="76794-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76794-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76794-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76794-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76794-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76794-141">INPUTS</span></span>

### <span data-ttu-id="76794-142">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="76794-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="76794-143">System. String</span><span class="sxs-lookup"><span data-stu-id="76794-143">System.String</span></span>

## <span data-ttu-id="76794-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76794-144">OUTPUTS</span></span>

### <span data-ttu-id="76794-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76794-145">System.Boolean</span></span>

## <span data-ttu-id="76794-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="76794-146">NOTES</span></span>

## <span data-ttu-id="76794-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76794-147">RELATED LINKS</span></span>

[<span data-ttu-id="76794-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="76794-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="76794-149">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="76794-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="76794-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="76794-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
