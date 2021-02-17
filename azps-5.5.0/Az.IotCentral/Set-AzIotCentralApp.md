---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219841"
---
# <span data-ttu-id="76223-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="76223-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="76223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76223-102">SYNOPSIS</span></span>
<span data-ttu-id="76223-103">Обновляет метаданные центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="76223-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="76223-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76223-104">SYNTAX</span></span>

### <span data-ttu-id="76223-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76223-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76223-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76223-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76223-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="76223-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76223-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76223-108">DESCRIPTION</span></span>
<span data-ttu-id="76223-109">Обновите метаданные центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="76223-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="76223-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76223-110">EXAMPLES</span></span>

### <span data-ttu-id="76223-111">Пример 1. Отображаемая версия</span><span class="sxs-lookup"><span data-stu-id="76223-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="76223-112">Обновив отображаемую имя в существующем центральном приложении IoT.</span><span class="sxs-lookup"><span data-stu-id="76223-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="76223-113">Пример выходных данных:</span><span class="sxs-lookup"><span data-stu-id="76223-113">Example Output:</span></span>

<span data-ttu-id="76223-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXX X-XXXX-XXXX-XXXXXXXXXX DisplayName : My New Custom Display Name Subdomain : MyAppSubdomain Template iotc-default@1.0.0 : SubscriptionId : XXXXXXX-XXXX-XXXX-XXXXX-XXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76223-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="76223-115">Пример 2: обновление поддомена</span><span class="sxs-lookup"><span data-stu-id="76223-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="76223-116">Обновив отображаемую имя в существующем центральном приложении IoT.</span><span class="sxs-lookup"><span data-stu-id="76223-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="76223-117">Пример выходных данных:</span><span class="sxs-lookup"><span data-stu-id="76223-117">Example Output:</span></span>

<span data-ttu-id="76223-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName : Display Name Subdomain : new-subdomain template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76223-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="76223-119">Пример 3. Обновление SKU приложения</span><span class="sxs-lookup"><span data-stu-id="76223-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="76223-120">Обновим SKU в существующем центральном приложении IoT.</span><span class="sxs-lookup"><span data-stu-id="76223-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="76223-121">Пример выходных данных:</span><span class="sxs-lookup"><span data-stu-id="76223-121">Example Output:</span></span>

<span data-ttu-id="76223-122">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX DisplayName : Display Name Subdomain : MyAppSubdomain Template iotc-default@1.0.0 : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76223-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="76223-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76223-123">PARAMETERS</span></span>

### <span data-ttu-id="76223-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76223-124">-AsJob</span></span>
<span data-ttu-id="76223-125">Запуск cmdlet в качестве задания в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="76223-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="76223-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76223-126">-DefaultProfile</span></span>
<span data-ttu-id="76223-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76223-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76223-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="76223-128">-DisplayName</span></span>
<span data-ttu-id="76223-129">Пользовательское отображаемого имени центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="76223-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="76223-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76223-130">-InputObject</span></span>
<span data-ttu-id="76223-131">Объект ввода Iot Central Application.</span><span class="sxs-lookup"><span data-stu-id="76223-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76223-132">-Name</span><span class="sxs-lookup"><span data-stu-id="76223-132">-Name</span></span>
<span data-ttu-id="76223-133">Имя центрального ресурса приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="76223-133">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76223-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76223-134">-ResourceGroupName</span></span>
<span data-ttu-id="76223-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76223-135">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76223-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76223-136">-ResourceId</span></span>
<span data-ttu-id="76223-137">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="76223-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="76223-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="76223-138">-Sku</span></span>
<span data-ttu-id="76223-139">Уровень цен для центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="76223-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="76223-140">Значение по умолчанию — ST2.</span><span class="sxs-lookup"><span data-stu-id="76223-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="76223-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="76223-141">-Subdomain</span></span>
<span data-ttu-id="76223-142">Поддомен центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="76223-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="76223-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="76223-143">-Tag</span></span>
<span data-ttu-id="76223-144">Теги ресурсов центрального приложения.</span><span class="sxs-lookup"><span data-stu-id="76223-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="76223-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76223-145">-Confirm</span></span>
<span data-ttu-id="76223-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="76223-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76223-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76223-147">-WhatIf</span></span>
<span data-ttu-id="76223-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76223-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76223-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="76223-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76223-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76223-150">CommonParameters</span></span>
<span data-ttu-id="76223-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76223-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76223-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76223-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76223-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76223-153">INPUTS</span></span>

### <span data-ttu-id="76223-154">System.String</span><span class="sxs-lookup"><span data-stu-id="76223-154">System.String</span></span>

### <span data-ttu-id="76223-155">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="76223-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="76223-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76223-156">OUTPUTS</span></span>

### <span data-ttu-id="76223-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="76223-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="76223-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76223-158">NOTES</span></span>

## <span data-ttu-id="76223-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76223-159">RELATED LINKS</span></span>
