---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241472"
---
# <span data-ttu-id="69444-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="69444-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="69444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69444-102">SYNOPSIS</span></span>
<span data-ttu-id="69444-103">Создайте или обновйте метаданные службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="69444-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="69444-104">Обычно свойство можно изменять, извлекая метаданные и метаданные системы безопасности Windows IoT, а затем объединяя их с измененными значениями в новом теле для обновления службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="69444-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="69444-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69444-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69444-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69444-106">DESCRIPTION</span></span>
<span data-ttu-id="69444-107">Создайте или обновйте метаданные службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="69444-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="69444-108">Обычно свойство можно изменять, извлекая метаданные и метаданные системы безопасности Windows IoT, а затем объединяя их с измененными значениями в новом теле для обновления службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="69444-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="69444-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69444-109">EXAMPLES</span></span>

### <span data-ttu-id="69444-110">Пример 1. Создание служб Windows IoT</span><span class="sxs-lookup"><span data-stu-id="69444-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="69444-111">Эта команда создает новые службы Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="69444-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="69444-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69444-112">PARAMETERS</span></span>

### <span data-ttu-id="69444-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="69444-113">-AdminDomainName</span></span>
<span data-ttu-id="69444-114">Домен AAD службы устройств Windows IoT OEM</span><span class="sxs-lookup"><span data-stu-id="69444-114">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="69444-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="69444-115">-BillingDomainName</span></span>
<span data-ttu-id="69444-116">Домен AAD службы устройств Windows IoT ODM</span><span class="sxs-lookup"><span data-stu-id="69444-116">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="69444-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69444-117">-DefaultProfile</span></span>
<span data-ttu-id="69444-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69444-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69444-119">-Etag</span><span class="sxs-lookup"><span data-stu-id="69444-119">-Etag</span></span>
<span data-ttu-id="69444-120">Поле Etag *не* требуется.</span><span class="sxs-lookup"><span data-stu-id="69444-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="69444-121">Если она представлена в теле ответа, она также должна быть представлена в качестве заголовка для обычного соглашения об ETag.</span><span class="sxs-lookup"><span data-stu-id="69444-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="69444-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="69444-122">-IfMatch</span></span>
<span data-ttu-id="69444-123">ETag of the Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="69444-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="69444-124">Не укажите для создания новой службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="69444-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="69444-125">Требуется для обновления существующей службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="69444-125">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="69444-126">-Location</span><span class="sxs-lookup"><span data-stu-id="69444-126">-Location</span></span>
<span data-ttu-id="69444-127">Регион Azure, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="69444-127">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="69444-128">-Name</span><span class="sxs-lookup"><span data-stu-id="69444-128">-Name</span></span>
<span data-ttu-id="69444-129">Имя службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="69444-129">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69444-130">-Note</span><span class="sxs-lookup"><span data-stu-id="69444-130">-Note</span></span>
<span data-ttu-id="69444-131">Заметки службы устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="69444-131">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="69444-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="69444-132">-Quantity</span></span>
<span data-ttu-id="69444-133">Выделение устройств со службой windows IoT,</span><span class="sxs-lookup"><span data-stu-id="69444-133">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="69444-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69444-134">-ResourceGroupName</span></span>
<span data-ttu-id="69444-135">Имя группы ресурсов, которая содержит службу устройств Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="69444-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69444-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69444-136">-SubscriptionId</span></span>
<span data-ttu-id="69444-137">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="69444-137">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69444-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="69444-138">-Tag</span></span>
<span data-ttu-id="69444-139">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69444-139">Resource tags.</span></span>

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

### <span data-ttu-id="69444-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69444-140">-Confirm</span></span>
<span data-ttu-id="69444-141">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="69444-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69444-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69444-142">-WhatIf</span></span>
<span data-ttu-id="69444-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69444-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69444-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="69444-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69444-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69444-145">CommonParameters</span></span>
<span data-ttu-id="69444-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69444-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69444-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69444-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69444-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69444-148">INPUTS</span></span>

## <span data-ttu-id="69444-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69444-149">OUTPUTS</span></span>

### <span data-ttu-id="69444-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="69444-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="69444-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69444-151">NOTES</span></span>

<span data-ttu-id="69444-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="69444-152">ALIASES</span></span>

## <span data-ttu-id="69444-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69444-153">RELATED LINKS</span></span>

