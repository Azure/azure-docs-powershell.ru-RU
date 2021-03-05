---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 51e828245c62ddfcbaa925b3a22a916fd9148ada
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010931"
---
# <span data-ttu-id="765e3-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="765e3-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="765e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="765e3-102">SYNOPSIS</span></span>
<span data-ttu-id="765e3-103">Получите метаданные службы устройств Windows IoT, не связанные с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="765e3-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="765e3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="765e3-104">SYNTAX</span></span>

### <span data-ttu-id="765e3-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="765e3-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="765e3-106">Получить</span><span class="sxs-lookup"><span data-stu-id="765e3-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="765e3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="765e3-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="765e3-108">Список</span><span class="sxs-lookup"><span data-stu-id="765e3-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="765e3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="765e3-109">DESCRIPTION</span></span>
<span data-ttu-id="765e3-110">Получите метаданные службы устройств Windows IoT, не связанные с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="765e3-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="765e3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="765e3-111">EXAMPLES</span></span>

### <span data-ttu-id="765e3-112">Пример 1. Все службы Windows IoT по подписке</span><span class="sxs-lookup"><span data-stu-id="765e3-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="765e3-113">Эта команда получает все службы Windows IoT в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="765e3-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="765e3-114">Пример 2. Получить все службы Windows IoT в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="765e3-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="765e3-115">Эта команда получает все службы Windows IoT в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="765e3-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="765e3-116">Пример 3. Получить службу Windows IoT по имени</span><span class="sxs-lookup"><span data-stu-id="765e3-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="765e3-117">Эта команда получает службу Windows IoT по имени.</span><span class="sxs-lookup"><span data-stu-id="765e3-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="765e3-118">Пример 4. Получить службу Windows IoT по объектам</span><span class="sxs-lookup"><span data-stu-id="765e3-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="765e3-119">Эта команда получает службу Windows IoT по объектам.</span><span class="sxs-lookup"><span data-stu-id="765e3-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="765e3-120">Пример 4. Получить службу Windows IoT по конвейеру</span><span class="sxs-lookup"><span data-stu-id="765e3-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="765e3-121">Эта команда получает службу Windows IoT по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="765e3-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="765e3-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="765e3-122">PARAMETERS</span></span>

### <span data-ttu-id="765e3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="765e3-123">-DefaultProfile</span></span>
<span data-ttu-id="765e3-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="765e3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="765e3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="765e3-125">-InputObject</span></span>
<span data-ttu-id="765e3-126">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="765e3-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="765e3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="765e3-127">-Name</span></span>
<span data-ttu-id="765e3-128">Имя службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="765e3-128">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765e3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="765e3-129">-ResourceGroupName</span></span>
<span data-ttu-id="765e3-130">Имя группы ресурсов, которая содержит службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="765e3-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765e3-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="765e3-131">-SubscriptionId</span></span>
<span data-ttu-id="765e3-132">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="765e3-132">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765e3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="765e3-133">CommonParameters</span></span>
<span data-ttu-id="765e3-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="765e3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="765e3-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="765e3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="765e3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="765e3-136">INPUTS</span></span>

### <span data-ttu-id="765e3-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="765e3-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="765e3-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="765e3-138">OUTPUTS</span></span>

### <span data-ttu-id="765e3-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="765e3-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="765e3-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="765e3-140">NOTES</span></span>

<span data-ttu-id="765e3-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="765e3-141">ALIASES</span></span>

<span data-ttu-id="765e3-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="765e3-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="765e3-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="765e3-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="765e3-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="765e3-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="765e3-145">INPUTOBJECT <IWindowsIotServicesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="765e3-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="765e3-146">`[DeviceName <String>]`: Имя службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="765e3-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="765e3-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="765e3-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="765e3-148">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="765e3-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="765e3-149">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="765e3-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="765e3-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="765e3-150">RELATED LINKS</span></span>

