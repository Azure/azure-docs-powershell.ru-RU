---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505700"
---
# <span data-ttu-id="a92fb-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="a92fb-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="a92fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a92fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a92fb-103">Удалите службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="a92fb-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="a92fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a92fb-104">SYNTAX</span></span>

### <span data-ttu-id="a92fb-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a92fb-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a92fb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a92fb-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a92fb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a92fb-107">DESCRIPTION</span></span>
<span data-ttu-id="a92fb-108">Удалите службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="a92fb-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="a92fb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a92fb-109">EXAMPLES</span></span>

### <span data-ttu-id="a92fb-110">Пример 1. Удаление служб Windows IoT по имени</span><span class="sxs-lookup"><span data-stu-id="a92fb-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="a92fb-111">Эта команда удаляет службы Windows IoT по имени.</span><span class="sxs-lookup"><span data-stu-id="a92fb-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="a92fb-112">Пример 2. Удаление служб Windows IoT по конвейеру</span><span class="sxs-lookup"><span data-stu-id="a92fb-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="a92fb-113">Эта команда удаляет службы Windows IoT по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="a92fb-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="a92fb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a92fb-114">PARAMETERS</span></span>

### <span data-ttu-id="a92fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92fb-115">-DefaultProfile</span></span>
<span data-ttu-id="a92fb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a92fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92fb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a92fb-117">-InputObject</span></span>
<span data-ttu-id="a92fb-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a92fb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a92fb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a92fb-119">-Name</span></span>
<span data-ttu-id="a92fb-120">Имя службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="a92fb-120">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="a92fb-122">Имя группы ресурсов, которая содержит службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="a92fb-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92fb-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a92fb-123">-SubscriptionId</span></span>
<span data-ttu-id="a92fb-124">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="a92fb-124">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92fb-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a92fb-125">-Confirm</span></span>
<span data-ttu-id="a92fb-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a92fb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a92fb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a92fb-127">-WhatIf</span></span>
<span data-ttu-id="a92fb-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a92fb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a92fb-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a92fb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a92fb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92fb-130">CommonParameters</span></span>
<span data-ttu-id="a92fb-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92fb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92fb-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a92fb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92fb-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a92fb-133">INPUTS</span></span>

### <span data-ttu-id="a92fb-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="a92fb-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="a92fb-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a92fb-135">OUTPUTS</span></span>

### <span data-ttu-id="a92fb-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="a92fb-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="a92fb-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a92fb-137">NOTES</span></span>

<span data-ttu-id="a92fb-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a92fb-138">ALIASES</span></span>

<span data-ttu-id="a92fb-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a92fb-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a92fb-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a92fb-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a92fb-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a92fb-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a92fb-142">INPUTOBJECT <IWindowsIotServicesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a92fb-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a92fb-143">`[DeviceName <String>]`: Имя службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="a92fb-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="a92fb-144">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="a92fb-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a92fb-145">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="a92fb-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="a92fb-146">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="a92fb-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="a92fb-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a92fb-147">RELATED LINKS</span></span>

