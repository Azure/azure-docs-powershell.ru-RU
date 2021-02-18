---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241469"
---
# <span data-ttu-id="0ef67-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="0ef67-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="0ef67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ef67-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef67-103">Удалите службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="0ef67-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="0ef67-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ef67-104">SYNTAX</span></span>

### <span data-ttu-id="0ef67-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ef67-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ef67-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0ef67-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ef67-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ef67-107">DESCRIPTION</span></span>
<span data-ttu-id="0ef67-108">Удалите службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="0ef67-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="0ef67-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ef67-109">EXAMPLES</span></span>

### <span data-ttu-id="0ef67-110">Пример 1. Удаление служб Windows IoT по имени</span><span class="sxs-lookup"><span data-stu-id="0ef67-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="0ef67-111">Эта команда удаляет службы Windows IoT по имени.</span><span class="sxs-lookup"><span data-stu-id="0ef67-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="0ef67-112">Пример 2. Удаление служб Windows IoT по конвейеру</span><span class="sxs-lookup"><span data-stu-id="0ef67-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="0ef67-113">Эта команда удаляет службы Windows IoT по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="0ef67-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="0ef67-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ef67-114">PARAMETERS</span></span>

### <span data-ttu-id="0ef67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef67-115">-DefaultProfile</span></span>
<span data-ttu-id="0ef67-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ef67-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ef67-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ef67-117">-InputObject</span></span>
<span data-ttu-id="0ef67-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="0ef67-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0ef67-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0ef67-119">-Name</span></span>
<span data-ttu-id="0ef67-120">Имя службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="0ef67-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="0ef67-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef67-121">-ResourceGroupName</span></span>
<span data-ttu-id="0ef67-122">Имя группы ресурсов, которая содержит службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="0ef67-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="0ef67-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ef67-123">-SubscriptionId</span></span>
<span data-ttu-id="0ef67-124">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="0ef67-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="0ef67-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ef67-125">-Confirm</span></span>
<span data-ttu-id="0ef67-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0ef67-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ef67-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef67-127">-WhatIf</span></span>
<span data-ttu-id="0ef67-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ef67-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ef67-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0ef67-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ef67-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef67-130">CommonParameters</span></span>
<span data-ttu-id="0ef67-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef67-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef67-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ef67-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef67-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ef67-133">INPUTS</span></span>

### <span data-ttu-id="0ef67-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="0ef67-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="0ef67-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ef67-135">OUTPUTS</span></span>

### <span data-ttu-id="0ef67-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="0ef67-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="0ef67-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ef67-137">NOTES</span></span>

<span data-ttu-id="0ef67-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0ef67-138">ALIASES</span></span>

<span data-ttu-id="0ef67-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0ef67-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ef67-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="0ef67-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ef67-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ef67-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ef67-142">INPUTOBJECT <IWindowsIotServicesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="0ef67-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ef67-143">`[DeviceName <String>]`: Имя службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="0ef67-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="0ef67-144">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="0ef67-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ef67-145">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="0ef67-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="0ef67-146">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="0ef67-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="0ef67-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ef67-147">RELATED LINKS</span></span>

