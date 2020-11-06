---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
ms.openlocfilehash: ac0513b7d411c2c95864aa6f619e80d2373a3554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564215"
---
# <span data-ttu-id="7a7ec-101">Remove-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="7a7ec-101">Remove-AzureRmVpnSite</span></span>

## <span data-ttu-id="7a7ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7ec-103">Удаление ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-103">Removes an Azure VpnSite resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a7ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a7ec-104">SYNTAX</span></span>

### <span data-ttu-id="7a7ec-105">ByVpnSiteName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a7ec-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a7ec-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="7a7ec-106">ByVpnSiteObject</span></span>
```
Remove-AzureRmVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a7ec-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="7a7ec-107">ByVpnSiteResourceId</span></span>
```
Remove-AzureRmVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a7ec-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a7ec-108">DESCRIPTION</span></span>
<span data-ttu-id="7a7ec-109">Удаление ресурса Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="7a7ec-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a7ec-110">EXAMPLES</span></span>

### <span data-ttu-id="7a7ec-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a7ec-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="7a7ec-112">В приведенном выше примере будет создана группа ресурсов, Виртуальная глобальная сеть в Запад США в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="7a7ec-113">Затем он создает VpnSite для представления ветви клиента и связывает ее с виртуальной глобальной сетью.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="7a7ec-114">После создания сайта немедленно удаляется с помощью команды Remove-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-114">Once the site is created, it is immediately removed using the Remove-AzureRmVpnSite command.</span></span>

### <span data-ttu-id="7a7ec-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7a7ec-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzureRmVpnSite
```

<span data-ttu-id="7a7ec-116">То же, что и в примере 1, но удаление происходит при использовании вывода из команды Get-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-116">Same as example 1 but here the removal happens using the piped output from Get-AzureRmVpnSite.</span></span>

## <span data-ttu-id="7a7ec-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a7ec-117">PARAMETERS</span></span>

### <span data-ttu-id="7a7ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7ec-118">-DefaultProfile</span></span>
<span data-ttu-id="7a7ec-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7ec-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7a7ec-120">-Force</span></span>
<span data-ttu-id="7a7ec-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7a7ec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a7ec-122">-InputObject</span></span>
<span data-ttu-id="7a7ec-123">Объект vpnSite, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="7a7ec-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a7ec-124">-Name</span></span>
<span data-ttu-id="7a7ec-125">Имя vpnSite.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="7a7ec-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a7ec-126">-PassThru</span></span>
<span data-ttu-id="7a7ec-127">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="7a7ec-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7a7ec-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7ec-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a7ec-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-130">The resource group name.</span></span>

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

### <span data-ttu-id="7a7ec-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a7ec-131">-ResourceId</span></span>
<span data-ttu-id="7a7ec-132">Идентификатор ресурса Azure для vpnSite, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="7a7ec-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a7ec-133">-Confirm</span></span>
<span data-ttu-id="7a7ec-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a7ec-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a7ec-135">-WhatIf</span></span>
<span data-ttu-id="7a7ec-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a7ec-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a7ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7ec-138">CommonParameters</span></span>
<span data-ttu-id="7a7ec-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7ec-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a7ec-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7ec-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a7ec-141">INPUTS</span></span>

### <span data-ttu-id="7a7ec-142">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="7a7ec-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="7a7ec-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7a7ec-143">System.String</span></span>

## <span data-ttu-id="7a7ec-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a7ec-144">OUTPUTS</span></span>

### <span data-ttu-id="7a7ec-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a7ec-145">System.Boolean</span></span>

## <span data-ttu-id="7a7ec-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a7ec-146">NOTES</span></span>

## <span data-ttu-id="7a7ec-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a7ec-147">RELATED LINKS</span></span>
