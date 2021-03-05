---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 27eecabc9bb144270b86a26e5128b9a0d63d346b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971587"
---
# <span data-ttu-id="67155-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="67155-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="67155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67155-102">SYNOPSIS</span></span>
<span data-ttu-id="67155-103">Обновляет метаданные службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="67155-104">Обычно для изменения свойства требуется извлечь метаданные и метаданные системы безопасности Windows IoT, а затем объединить их с измененными значениями в новом теле для обновления службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="67155-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67155-105">SYNTAX</span></span>

### <span data-ttu-id="67155-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67155-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="67155-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="67155-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="67155-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67155-108">DESCRIPTION</span></span>
<span data-ttu-id="67155-109">Обновляет метаданные службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="67155-110">Обычно для изменения свойства требуется извлечь метаданные и метаданные системы безопасности Windows IoT, а затем объединить их с измененными значениями в новом теле для обновления службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="67155-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67155-111">EXAMPLES</span></span>

### <span data-ttu-id="67155-112">Пример 1. Обновление служб Windows IoT по имени</span><span class="sxs-lookup"><span data-stu-id="67155-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="67155-113">Эта команда обновляет по имени службы Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="67155-114">Пример 2. Обновление служб Windows IoT по конвейеру</span><span class="sxs-lookup"><span data-stu-id="67155-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="67155-115">Эта команда обновляет службы Windows IoT по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="67155-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="67155-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67155-116">PARAMETERS</span></span>

### <span data-ttu-id="67155-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="67155-117">-AdminDomainName</span></span>
<span data-ttu-id="67155-118">Домен AAD службы устройств Windows IoT OEM</span><span class="sxs-lookup"><span data-stu-id="67155-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="67155-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="67155-119">-BillingDomainName</span></span>
<span data-ttu-id="67155-120">Домен AAD службы устройств Windows IoT ODM</span><span class="sxs-lookup"><span data-stu-id="67155-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="67155-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67155-121">-DefaultProfile</span></span>
<span data-ttu-id="67155-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67155-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67155-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="67155-123">-Etag</span></span>
<span data-ttu-id="67155-124">Поле Etag *не* требуется.</span><span class="sxs-lookup"><span data-stu-id="67155-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="67155-125">Если она представлена в теле ответа, она также должна быть представлена в качестве заголовка для обычного соглашения об ETag.</span><span class="sxs-lookup"><span data-stu-id="67155-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="67155-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="67155-126">-IfMatch</span></span>
<span data-ttu-id="67155-127">ETag of the Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="67155-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="67155-128">Не укажите для создания новой службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="67155-129">Требуется для обновления существующей службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="67155-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67155-130">-InputObject</span></span>
<span data-ttu-id="67155-131">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="67155-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67155-132">-Location</span><span class="sxs-lookup"><span data-stu-id="67155-132">-Location</span></span>
<span data-ttu-id="67155-133">Регион Azure, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="67155-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="67155-134">-Name</span><span class="sxs-lookup"><span data-stu-id="67155-134">-Name</span></span>
<span data-ttu-id="67155-135">Имя службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-135">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67155-136">-Note</span><span class="sxs-lookup"><span data-stu-id="67155-136">-Note</span></span>
<span data-ttu-id="67155-137">Заметки службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="67155-138">-Quantity</span><span class="sxs-lookup"><span data-stu-id="67155-138">-Quantity</span></span>
<span data-ttu-id="67155-139">Выделение устройств со службой windows IoT,</span><span class="sxs-lookup"><span data-stu-id="67155-139">Windows IoT Device Service device allocation,</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67155-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67155-140">-ResourceGroupName</span></span>
<span data-ttu-id="67155-141">Имя группы ресурсов, которая содержит службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67155-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67155-142">-SubscriptionId</span></span>
<span data-ttu-id="67155-143">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="67155-143">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67155-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="67155-144">-Tag</span></span>
<span data-ttu-id="67155-145">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67155-145">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67155-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67155-146">-Confirm</span></span>
<span data-ttu-id="67155-147">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67155-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67155-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67155-148">-WhatIf</span></span>
<span data-ttu-id="67155-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67155-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67155-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="67155-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67155-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67155-151">CommonParameters</span></span>
<span data-ttu-id="67155-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67155-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67155-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67155-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67155-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67155-154">INPUTS</span></span>

### <span data-ttu-id="67155-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="67155-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="67155-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67155-156">OUTPUTS</span></span>

### <span data-ttu-id="67155-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="67155-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="67155-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67155-158">NOTES</span></span>

<span data-ttu-id="67155-159">ALIASES</span><span class="sxs-lookup"><span data-stu-id="67155-159">ALIASES</span></span>

<span data-ttu-id="67155-160">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="67155-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67155-161">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="67155-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67155-162">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67155-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67155-163">INPUTOBJECT <IWindowsIotServicesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="67155-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67155-164">`[DeviceName <String>]`: Имя службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="67155-165">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="67155-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67155-166">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67155-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="67155-167">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="67155-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="67155-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67155-168">RELATED LINKS</span></span>

