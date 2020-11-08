---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247794"
---
# <span data-ttu-id="eea91-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="eea91-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="eea91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eea91-102">SYNOPSIS</span></span>
<span data-ttu-id="eea91-103">Обновляет метаданные приложения центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="eea91-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="eea91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eea91-104">SYNTAX</span></span>

### <span data-ttu-id="eea91-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eea91-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eea91-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea91-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eea91-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea91-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eea91-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eea91-108">DESCRIPTION</span></span>
<span data-ttu-id="eea91-109">Обновите метаданные приложения центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="eea91-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="eea91-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eea91-110">EXAMPLES</span></span>

### <span data-ttu-id="eea91-111">Пример 1 обновление отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="eea91-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="eea91-112">Обновление отображаемого имени на существующем центре администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="eea91-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="eea91-113">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="eea91-113">Example Output:</span></span>

<span data-ttu-id="eea91-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: SKU: Microsoft. Azure.. IotCentral. Models. ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My New Custom Display Name: PSIotCentralAppSkuInfo Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX MyAppSubdomain: ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea91-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="eea91-115">Пример 2 обновления поддомена</span><span class="sxs-lookup"><span data-stu-id="eea91-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="eea91-116">Обновление отображаемого имени на существующем центре администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="eea91-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="eea91-117">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="eea91-117">Example Output:</span></span>

<span data-ttu-id="eea91-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: SKU: Microsoft. Azure.. IotCentral. Models..-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Display Name поддомен: New-XXXX-XXXX-XXXX- iotc-default@1.0.0 XXXXXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="eea91-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="eea91-119">Пример 3 обновление сведений о SKU приложения</span><span class="sxs-lookup"><span data-stu-id="eea91-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="eea91-120">Обновите SKU на существующем центре интернета Интернет.</span><span class="sxs-lookup"><span data-stu-id="eea91-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="eea91-121">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="eea91-121">Example Output:</span></span>

<span data-ttu-id="eea91-122">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: SKU: Microsoft. Azure., IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Display Name поддомен: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea91-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="eea91-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eea91-123">PARAMETERS</span></span>

### <span data-ttu-id="eea91-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eea91-124">-AsJob</span></span>
<span data-ttu-id="eea91-125">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="eea91-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="eea91-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea91-126">-DefaultProfile</span></span>
<span data-ttu-id="eea91-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eea91-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea91-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eea91-128">-DisplayName</span></span>
<span data-ttu-id="eea91-129">Настраиваемое отображаемое имя центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="eea91-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="eea91-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eea91-130">-InputObject</span></span>
<span data-ttu-id="eea91-131">Объект ввода центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="eea91-131">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="eea91-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eea91-132">-Name</span></span>
<span data-ttu-id="eea91-133">Имя ресурса центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="eea91-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="eea91-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea91-134">-ResourceGroupName</span></span>
<span data-ttu-id="eea91-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eea91-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="eea91-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea91-136">-ResourceId</span></span>
<span data-ttu-id="eea91-137">Идентификатор ресурса приложения центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="eea91-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="eea91-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="eea91-138">-Sku</span></span>
<span data-ttu-id="eea91-139">Ценовая категория для приложений центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="eea91-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="eea91-140">Значение по умолчанию — ST2.</span><span class="sxs-lookup"><span data-stu-id="eea91-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="eea91-141">-Поддомен</span><span class="sxs-lookup"><span data-stu-id="eea91-141">-Subdomain</span></span>
<span data-ttu-id="eea91-142">Поддомен центрального домена для приложения Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="eea91-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="eea91-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="eea91-143">-Tag</span></span>
<span data-ttu-id="eea91-144">Теги ресурсов центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="eea91-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="eea91-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eea91-145">-Confirm</span></span>
<span data-ttu-id="eea91-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eea91-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea91-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea91-147">-WhatIf</span></span>
<span data-ttu-id="eea91-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eea91-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea91-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eea91-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea91-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea91-150">CommonParameters</span></span>
<span data-ttu-id="eea91-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eea91-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea91-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eea91-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea91-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eea91-153">INPUTS</span></span>

### <span data-ttu-id="eea91-154">System. String</span><span class="sxs-lookup"><span data-stu-id="eea91-154">System.String</span></span>

### <span data-ttu-id="eea91-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="eea91-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="eea91-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eea91-156">OUTPUTS</span></span>

### <span data-ttu-id="eea91-157">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="eea91-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="eea91-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="eea91-158">NOTES</span></span>

## <span data-ttu-id="eea91-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eea91-159">RELATED LINKS</span></span>
